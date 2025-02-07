# Install Guide

**Dependencies**

* [\[ox\_lib\]](https://overextended.dev/ox_lib)
* Supported Frameworks
  * ESX
    * ox\_inventory
  * QB-Core
    * qb-Inventory
    * ox\_inventory



**Install Steps**

* Install Dependencies.
* Add `lsc_drugs` your resource folder.
* Add `start lsc_drugs` into your server.cfg (Must be started after the Dependencies.)
* make sure `ox_lib` ace permissions are in `server.cfg.`

```
add_ace resource.ox_lib command.add_ace allow
add_ace resource.ox_lib command.remove_ace allow
add_ace resource.ox_lib command.add_principal allow
add_ace resource.ox_lib command.remove_principal allow
```

Your server.cfg should look similar to this when finished

```
start ox_lib
start framework
start lsc_drugs

add_ace resource.ox_lib command.add_ace allow
add_ace resource.ox_lib command.remove_ace allow
add_ace resource.ox_lib command.add_principal allow
add_ace resource.ox_lib command.remove_principal allow
```
