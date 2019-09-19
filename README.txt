## Problem Statement 
```Imagine you are building a system to assign unique numbers to each resource that you manage. You want the ids to be guaranteed unique i.e. no UUIDs.  Since these ids are globally unique, each id can only be given out at most once. The ids are 64 bits long.

Your service is composed of a set of nodes, each running one process serving ids.  A caller will connect to one of the nodes and ask it for a globally unique id.  There are a fixed number of nodes in the system, up to 1024.  Each node has a numeric id, 0 <= id <= 1023. Each node knows its id at startup and that id never changes for the node.

Your task is to implement get_id.  When a caller requests a new id, the node it connects to calls its internal get_id function to get a new, globally unique id.     ```



#create a virual environment
> virtualenv socialgraph
> source socialgraph/bin/activate
> pip install -r requirements.txt
> python test.py

# we are creating a graph with 100,000 nodes and searching for the connection between user 1 and user 2
# the code in test.py is self explantory on how to add users and add friends
# We are doing a BFS from the source and from the destination and merging the paths when there is a collision.
# let's say that each user has k connections and the distance between them is l, then the time complexity would be O(k^(l/2)) + O(k^(l/2)) = O(k^(l/2))
# if we had done one bfs then the complexity would have been O(k^(l))
 


