# Configuration



{% tabs %}
{% tab title="Config.Lua" %}
```lua
Config = {}

Config.Preferences = {
    framework = "esx", -- esx = es_extended, qb = qb-core,
    notify = "ox", -- ox = ox_lib, vms = vms_notify [Set your own notify in lsc_cmds/client/editable.lua!]
    locale = "en" -- en = english, es = spanish, fr = french. add your own in Config/Locales.lua
}

Config.UseGlobalOOC = true -- Do you want to use global ooc? If turned to false /ooc will not be registered as a commmand
Config.UseReportSystem = true -- Turn this to True if you want to use the built in report system. Turn it to False if you have your own report system
Config.UseInvalidCommand = true -- Do you want players to be alerted with the the notify when a invalid command is typed?

-- You can add more group's based off your liking!
Config.Groups = {
    { name = "admin", label = "Administrator" },
    { name = "tester", label = "Tester" },
    { name = "superadmin", label = "Superadmin" }
}

Config.Prefixes = {
    Advertisement = {
        message = '[Advertisement] (IC): ', -- The prefix for advertisement messages.
        color = '#37cdd1' -- The color advertisement messages will be in.
    },
    Error = {
        message = '[ERROR]: ', -- The prefix for error messages.
        color = '#da4e4e' -- The color error messages will be in.
    },
    Server = {
        message = '[SERVER]: ', -- The prefix for server messages.
        color = {255, 99, 71} -- The color server messages will be in.
    },
}

Config.BusinessAdvertisement = {
    amount = "500", -- amount it cost to use /bad or /ad
    cooldown = "30", -- cooldown on /bad and /ad in minutes
}

-- jobs allowed to use /bad, /ad etc.
Config.AdJobs = {
   'police',
   'burgershot'
}

--- Misc Config Settings
Config.MaxPlayers = 128 -- Set the amount of player slots your server has here. Used in /online & /players!
```
{% endtab %}

{% tab title="Locales.lua" %}
```lua
Locales = {}

Locales['en'] = {
    access_denied_title = "Access Denied",
    access_denied_desc = "You do not have permission to this command.",
    invalid_target_title = "Invalid Target",
    invalid_target_desc = "The specified player ID is not online.",
    invalid_command_desc = "You have entered an invalid command.",
    report_submitted_desc = "Your report has been sent to all online admins.",
    admin_duty_title = "Admin Duty",
    admin_duty_on_desc = "You are now on admin duty.",
    admin_duty_off_desc = "You are now off admin duty.",
    report_cooldown_title = "Cooldown",
    report_cooldown_desc = "You must wait %d seconds before sending another report.",
    report_error_title = "Error",
    report_error_desc = "Report not found or already handled.",
    report_accepted_title = "Report Accepted",
    report_accepted_desc = "You accepted report #%d.",
    report_accepted_notify = "Your report #%d has been accepted by %s.",
    report_close_error_title = "Error",
    report_close_error_desc = "Report not found or already closed.",
    report_closed_title = "Report Closed",
    report_closed_desc = "You closed report #%d.",
    report_closed_notify = "Your report #%d has been closed by %s.",
    togs_title = "Togs",
    togs_say_enabled = "Say Mode Enabled",
    togs_ooc_enabled = "OOC Mode Enabled",
    global_ooc_title = "Global OOC",
    global_ooc_enabled = "You have enabled Global OOC messages.",
    global_ooc_disabled = "You have disabled Global OOC messages.",
    ad_cooldown_title = "Cooldown Active",
    ad_cooldown_desc = "You must wait %d minutes before sending another advertisement.",
    ad_not_enough_money_title = "Not Enough Money",
    ad_not_enough_money_desc = "You need at least $%d to place an advertisement.",
    ad_sent_title = "Advertisement Sent",
    ad_sent_desc = "Your ad has been posted for $%d."
}

Locales['fr'] = {
    access_denied_title = "Accès Refusé",
    access_denied_desc = "Vous n'avez pas l'autorisation d'utiliser cette commande.",
    invalid_target_title = "Cible Invalide",
    invalid_target_desc = "L'ID du joueur spécifié n'est pas en ligne.",
    invalid_command_desc = "Vous avez entré une commande invalide.",
    report_submitted_desc = "Votre rapport a été envoyé à tous les administrateurs en ligne.",
    admin_duty_title = "Fonction d'Administrateur",
    admin_duty_on_desc = "Vous êtes maintenant en fonction d'administrateur.",
    admin_duty_off_desc = "Vous n'êtes plus en fonction d'administrateur.",
    report_cooldown_title = "Temps de Recharge",
    report_cooldown_desc = "Vous devez attendre %d secondes avant d'envoyer un autre rapport.",
    report_error_title = "Erreur",
    report_error_desc = "Rapport introuvable ou déjà traité.",
    report_accepted_title = "Rapport Accepté",
    report_accepted_desc = "Vous avez accepté le rapport #%d.",
    report_accepted_notify = "Votre rapport #%d a été accepté par %s.",
    report_close_error_title = "Erreur",
    report_close_error_desc = "Rapport introuvable ou déjà fermé.",
    report_closed_title = "Rapport Fermé",
    report_closed_desc = "Vous avez fermé le rapport #%d.",
    report_closed_notify = "Votre rapport #%d a été fermé par %s.",
    togs_title = "Togs",
    togs_say_enabled = "Mode Say Activé",
    togs_ooc_enabled = "Mode OOC Activé",
    global_ooc_title = "OOC Global",
    global_ooc_enabled = "Vous avez activé les messages OOC globaux.",
    global_ooc_disabled = "Vous avez désactivé les messages OOC globaux.",
    ad_cooldown_title = "Recharge Active",
    ad_cooldown_desc = "Vous devez attendre %d minutes avant d'envoyer une autre annonce.",
    ad_not_enough_money_title = "Pas Assez d'Argent",
    ad_not_enough_money_desc = "Vous avez besoin d'au moins $%d pour placer une annonce.",
    ad_sent_title = "Annonce Envoyée",
    ad_sent_desc = "Votre annonce a été publiée pour $%d."
}

Locales['es'] = {
    access_denied_title = "Acceso Denegado",
    access_denied_desc = "No tienes permiso para este comando.",
    invalid_target_title = "Objetivo Inválido",
    invalid_target_desc = "El ID del jugador especificado no está en línea.",
    invalid_command_desc = "Has introducido un comando inválido.",
    report_submitted_desc = "Tu informe ha sido enviado a todos los administradores en línea.",
    admin_duty_title = "Función de Administrador",
    admin_duty_on_desc = "Ahora estás en función de administrador.",
    admin_duty_off_desc = "Ya no estás en función de administrador.",
    report_cooldown_title = "Tiempo de Recarga",
    report_cooldown_desc = "Debes esperar %d segundos antes de enviar otro informe.",
    report_error_title = "Error",
    report_error_desc = "Informe no encontrado o ya gestionado.",
    report_accepted_title = "Informe Aceptado",
    report_accepted_desc = "Has aceptado el informe #%d.",
    report_accepted_notify = "Tu informe #%d ha sido aceptado por %s.",
    report_close_error_title = "Error",
    report_close_error_desc = "Informe no encontrado o ya cerrado.",
    report_closed_title = "Informe Cerrado",
    report_closed_desc = "Has cerrado el informe #%d.",
    report_closed_notify = "Tu informe #%d ha sido cerrado por %s.",
    togs_title = "Togs",
    togs_say_enabled = "Modo Say Activado",
    togs_ooc_enabled = "Modo OOC Activado",
    global_ooc_title = "OOC Global",
    global_ooc_enabled = "Has activado los mensajes OOC globales.",
    global_ooc_disabled = "Has desactivado los mensajes OOC globales.",
    ad_cooldown_title = "Recarga Activa",
    ad_cooldown_desc = "Debes esperar %d minutos antes de enviar otro anuncio.",
    ad_not_enough_money_title = "Dinero Insuficiente",
    ad_not_enough_money_desc = "Necesitas al menos $%d para publicar un anuncio.",
    ad_sent_title = "Anuncio Enviado",
    ad_sent_desc = "Tu anuncio ha sido publicado por $%d."
}

```
{% endtab %}
{% endtabs %}
