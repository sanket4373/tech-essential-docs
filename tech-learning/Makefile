help:
	@echo ""
	@echo "Usage: make COMMAND"
	@echo ""
	@echo "A Makefile for building and deploying a static site"
	@echo ""
	@echo "Commands:"
	@echo "pull        Pull the latest Mkdocs image"
	@echo "build       Build the documentation site"
	@echo "serve       Start the live docs server"
	@echo "clean       Remove stale files"
	@echo "publish     Deploy to GitHub Pages"
	@echo ""

pull: 
	docker pull squidfunk/mkdocs-material

build: 
	docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build

clean:
	docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build --clean

serve:
	docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material

publish: 
	docker run --rm -it -v ~/.ssh:/root/.ssh -v ${PWD}:/docs squidfunk/mkdocs-material gh-deploy
