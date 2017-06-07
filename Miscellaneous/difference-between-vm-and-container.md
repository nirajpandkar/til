# Difference between Virtual Machine and Container

### Virtual Machine 
* Runs completely different OS(Guest OS) which goes through all the processes of bootstrapping, loading kernel etc.
* Gets its own set of resources allocated to it, and does minimal sharing. 
* Therefore is much heavier(resource wise).
* More isolation and security.

### Container
* Works with the concept of namespaces. Each container runs in its own namespace. Processes in different namespaces cannot communicate with each other which provides a kind of virtualization.
* Less isolation and security.
* Containers share the same kernel and resources like network and disk.
* Therefore lightweight and fast.

For more information and low level explanation refer to this [answer](https://stackoverflow.com/a/34757096/4411757).