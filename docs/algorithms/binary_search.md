## BINARY SEARCH

In Binary search algorithm its input is a sorted list of elements. If an element you’re looking for is in that list, binary search returns the position where it’s located. Otherwise, binary search returns null. In general, for any list of n, binary search will take log2 n steps to run in the worst case, whereas simple search will take n steps.

examples:

- Suppose you’re searching for a person in the phone book (what an old-fashioned sentence!). Their name starts with K. You could start at the beginning and keep flipping pages until you get to the Ks. But you’re more likely to start at a page in the middle, because you know the Ks are going to be near the middle of the phone book. 

- Or suppose you’re searching for a word in a dictionary, and it starts with O. Again, you’ll start near the middle. 

- Now suppose you log on to Facebook. When you do, Facebook has to verify that you have an account on the site. So, it needs to search for your username in its database. Suppose your username is karlmageddon. Facebook could start from the As and search for your name—but it makes more sense for it to begin somewhere in the middle.

This is a search problem. And all these cases use the same algorithm to solve the problem: binary search.


