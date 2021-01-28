
- A routine which allocates the reosurce, same routing MUST deallocate the resources also after use. (resource can be File, Network connection, socket etc.)

### Pro Tip

Nest Allocations

The basic pattern for resource allocation can be extended for routines that need more than one resource at a time. There are just two more suggestions:

    Deallocate resources in the opposite order to that in which you allocate them. That way you won’t orphan resources if one resource contains references to another.

    When allocating the same set of resources in different places in your code, always allocate them in the same order. This will reduce the possibility of deadlock. (If process A claims resource1 and is about to claim resource2, while process B has claimed resource2 and is trying to get resource1, the two processes will wait forever.)

It doesn’t matter what kind of resources we’re using—transactions, network connections, memory, files, threads, windows—the basic pattern applies: whoever allocates a resource should be responsible for deallocating it. However, in some languages we can develop the concept further.
