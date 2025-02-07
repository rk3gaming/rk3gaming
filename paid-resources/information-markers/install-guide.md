# Install Guide

**Dependencies**

* [\[ox\_lib\]](https://overextended.dev/ox_lib)\


**Install Steps**

* Install Dependencies.
* Add `n_cim` your resource folder.
* Add `start n_cim` into your server.cfg (Must be started after the Dependencies.)
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
start n_cim

add_ace resource.ox_lib command.add_ace allow
add_ace resource.ox_lib command.remove_ace allow
add_ace resource.ox_lib command.add_principal allow
add_ace resource.ox_lib command.remove_principal allow
```

After that locate the `cim.sql` file in the `n_cim` folder and run it in `heidiSQL.`
