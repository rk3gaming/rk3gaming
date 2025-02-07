# Configuration

```lua
Config = {}

Config.Framework = "esx" -- esx / qb 

Config.Warning = true -- Should player's be alerted with Config.Message if they don't have their attributes set?
Config.Message = "[ ! ]: Your attribute(s) have not been set. Please use /attributes to configure them." -- Message player's get when their attributes aren't set and Config.Warning is true

Config.Commands = {
    OpenAttributes = 'attributes', -- Command to open the attributes menu
    ClearAttributes = 'resetattributes', -- Command to clear attributes
    Examine = 'examine', -- Command to examine a player's attributes
}

Config.AliasCommands = {
    OpenAttributes = 'attr', -- Command to open the attributes menu
    ClearAttributes = 'resetattr', -- Command to clear attributes
    Examine = 'ex', -- Command to examine a player's attributes
}

Config.Locales = { -- Do not remove %s it will mess up the script.
    errorMessage = "[ ! ]: %s has not set their attributes yet.",
    descriptionHeader = "|_____Description of %s_____|",
    ageRange = "Age Range: %s",
    details = "Details: %s",
    clothing = "Clothing: %s",
    tattoos = "Tattoos: %s",
    invalidPlayerId = "Error: Please provide a valid player ID."
}

Config.OxLocales = { -- The locale's for the /attributes context menu
    Title = 'Set Attributes',
    ageLabel = 'Age',
    ageDescription = 'Enter your age',
    descriptionLabel = 'Description',
    descriptionDescription = 'Enter a brief description',
    clothingLabel = 'Clothing',
    clothingDescription = 'Enter your clothing details (Optional)',
    tattoosLabel = 'Tattoos',
    tattoosDescription = 'Enter your tattoos details (Optional)'
}

Config.Colors = {
   errorColor = {255, 99, 71}, -- The color for error's and Config.Message
   descriptionColor = {61, 150, 74}, -- Color for descriptionHeader 
   attributesColor = {235, 225, 116}, -- Colors for Age Range, Details, Clothing, Tattoos when using /examine
}

```
