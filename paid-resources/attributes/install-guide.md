# Install Guide

**Dependencies**

* [\[ox\_lib\]](https://overextended.dev/ox_lib)
* Supported Frameworks
  * ESX
  * QB-Core



**Install Steps**

* Install Dependencies.
* Add `lsc_attributes` your resource folder.
* Add `start lsc_attributes` into your server.cfg (Must be started after the Dependencies.)
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
start lsc_attributes

add_ace resource.ox_lib command.add_ace allow
add_ace resource.ox_lib command.remove_ace allow
add_ace resource.ox_lib command.add_principal allow
add_ace resource.ox_lib command.remove_principal allow
```

After that go to HeidiSQL and install `"sql.sql"` in the `lsc_attributes` folder.
