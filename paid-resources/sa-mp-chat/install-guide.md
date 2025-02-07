# Install Guide

**Dependencies**

* [\[ox\_lib\]](https://overextended.dev/ox_lib)
* Supported Frameworks
  * ESX
  * QB-Core
  * Ox\_Core (soon)

**Install Steps**

* Install Dependencies.
* Add `lsc_cmds and chat` your resource folder.
* Add `start chat first then lsc_cmds` into your server.cfg (Must be started after the Dependencies.)
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
start chat
start lsc_cmds

add_ace resource.ox_lib command.add_ace allow
add_ace resource.ox_lib command.remove_ace allow
add_ace resource.ox_lib command.add_principal allow
add_ace resource.ox_lib command.remove_principal allow
```

Make sure you also follow [these steps](https://rk0-1.gitbook.io/lsc-development/paid-resources/sa-mp-chat/common-errors/chat-theme) if you have issues with the chat theme.
