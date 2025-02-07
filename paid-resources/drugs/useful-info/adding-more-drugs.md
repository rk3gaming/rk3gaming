---
description: >-
  To add more drugs it pretty simple. First you need to go to configs/cfg.lua
  and understand what each setting is for.
---

# Adding more drugs

**Config Settings**

\['   '] = The name of the item you want to turn into a drug.

Duration = How long it takes to use said drug, every 1000 = 1 second.

Dict = animation it plays you can find a list of animations [here](https://forge.plebmasters.de/animations).

Models = prop that is apart of the animation. You can find a list of props[ here](https://forge.plebmasters.de/objects).

Pos and Rot your on your own, that is posistion for the animations and props, have fun!

Effect Names = The effect that plays when the drug is taken. You can find a list of effects [here.](https://docs.altv.mp/gta/articles/references/animpost-fx.html)

Effect Last = The amount of time drugs last for, goes by minutes.&#x20;

Health and Armour, if you want drugs to give health and armour set it to your desired amount, if not turn it to 0

Message if you have Config.Messages = true, thats the message players get when using drugs



**Example**

```
Config.Drugs = {
    ['perc'] = {
        duration = 6000, 
        anim = {
            dict = 'mp_player_intdrink',
            clip = 'loop_bottle'
        },
        prop = {
            model = `prop_cs_pills`,
            pos = vec3(0.03, 0.03, 0.02),
            rot = vec3(0.0, 0.0, -1.5)
        },
        effect = {
            name = "DrugsMichaelAliensFight", 
            EffectLast = 1,
            health = 0,  
            armour = 0  
        },
        message = "As you take the medication, the world feels a little softer. The tension in your body subsides, replaced by a pleasant warmth. Remember to roleplay these effects." 
    },
}
```



Now after you create the item in the cfg.lua you need to create it as a inventory item. As of now lsc\_drugs supports qb-inventory and ox\_inventory.. Posted below is a example of how you'd create the item "perc"



**qb-inventory**

qb-core/shared/items.lua

```
["perc"] = {
    ["name"] = "perc",
    ["label"] = "Percocet",
    ["weight"] = 50, 
    ["type"] = "item",
    ["image"] = "perc.png", 
    ["unique"] = false,
    ["useable"] = true,
    ["description"] = "A pain-relieving medication. Use responsibly.",
}
```



**ox\_inventory**

ox\_inventory/data/items.lua

<pre><code>["adderall"] = {
<strong>   label = "Adderall",
</strong><strong>   description = 'A pain-relieving medication. Use responsibly.'
</strong><strong>   weight = 50,
</strong>   stack = true,
   close = true,
},
</code></pre>
