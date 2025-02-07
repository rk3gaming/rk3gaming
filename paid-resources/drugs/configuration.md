# Configuration



{% tabs %}
{% tab title="Config" %}
```
Config = {}

Config.Framework = "esx" -- esx or qb. oxcore coming soon.

Config.Messages = true -- Set to true to send a message to the player after using a drug.

Config.PoliceCommand = "drugtest" -- A command police can use to drug test players, test will only come back postive if the player has active drug effects.
Config.RequiredItem = "none" -- Item Config.Jobs must have to use the Config.PoliceCommand set to none if you dont want them to have to have a item.
Config.Jobs = { 'police', 'ambulance', 'sheriff' } -- Disclaimer, Config.Jobs can only test players if their within a radius of 10. 

-- Duration = How long it takes to use said drug, every 1000 = 1 second.
-- Dict = https://forge.plebmasters.de/animations or https://wiki.rage.mp/index.php?title=Scenarios 1 List = Animations, 2 = Scenarios
-- Models = https://forge.plebmasters.de/objects
-- Pos and Rot your on your own, that is posistion for the animations and props, have fun!
-- Effect Names = https://docs.altv.mp/gta/articles/references/animpost-fx.html
-- Effect Last = The amount of time drugs last for, goes by minutes.
-- Healh and Armour, if you want drugs to give health and armour set it to your desired amount, if not turn it to 0
-- Message if you have Config.Messages = true, thats the message players get when using drugs

-- I would use props if I were you, heres some good choices...
-- Free Props: https://store.dccustomz.com/product/6379840
-- Paid Props: https://mpworx.tebex.io/package/5669668

Config.Drugs = {
    ['percocet'] = {
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
            health = 5,  
            armour = 3  
        },
        message = "As you take the medication, the world feels a little softer. The tension in your body subsides, replaced by a pleasant warmth. Remember to roleplay these effects." 
    }
}

-- This system is used so you can have bottles, weed packs, that when used it gives another item and removes the bottle/pack
-- Example say you have a percocet_bottle and use it, it removes the percocet_bottle and gives you 5 percocets in exchange. Dont know why i added this feature but im sure yall will find a use for it.
-- Giveitem = What item it gives when the bottle/pack is used and removed
-- Amount = the amount of the item you set in giveItem it gives.

Config.WeedPacks = {
    ['weed_pack'] = {
        giveItem = 'weed',
        amount = 5,
    },
}

Config.PillBottles = {
    ['percocet_bottle'] = {
        giveItem = 'percocet', 
        amount = 5, 
    },
}

```
{% endtab %}

{% tab title="Strings" %}
```
Config.Messages = {
    error_item_not_found = "Error: You don't have this item.",
    error_invalid_drug_name = "Error: Invalid drug name.",
    error_no_pills = "Error: You don't have any %s",
    error_no_weed = "Error: You don't have any %s",
    usage_message = "Usage: /%s [playerId]",
    invalid_player_id = "[ ! ]: Invalid player ID.",
    player_too_far = "[ ! ]: The player is too far away to test.",
    drug_test_negative = "[Drug Test]: The test for %s came back NEGATIVE.",
    drug_test_positive = "[Drug Test]: The test for %s came back POSITIVE for drug: %s",
}

```
{% endtab %}
{% endtabs %}
