# Stopping/destroying vagrant instance

This command will tell you the state of all active Vagrant environments on the system for the currently logged in user.
```
$ vagrant global-status
```
This command stops the running machine Vagrant is managing and destroys all resources that were created during the machine creation process.
```
$ vagrant destroy [name|id]
```
This command shuts down the running machine Vagrant is managing.
```
$ vagrant halt [name|id]
```

### References

* [Halt](https://www.vagrantup.com/docs/cli/halt.html)
* [Destroy](https://www.vagrantup.com/docs/cli/destroy.html)
