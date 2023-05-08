## WHMCS
WHMCS Module for the [Pterodactyl Panel](https://github.com/pterodactyl/panel/).

## Configuration support
Please use the [Pterodactyl Discord](https://discord.gg/pterodactyl) for configuration related support instead of GitHub issues.

## NOTE!
This module requires the panel to be on version 0.7.3 and above, if you need one for lower than 0.7.x versions check out [death-droid's module](https://github.com/death-droid/Pterodactyl-WHMCS).

## Installation
[Video Tutorial](https://www.youtube.com/watch?v=wURpRD9vfj4)  

1. Download/Git clone this repository.  
2. Move the ``pterodactyl/`` folder into ``<path to whmcs>/modules/servers/``.
3. Create API Credentials with these permissions: ![Image](https://owo.sh/fa1eee.png)
4. In WHMCS navigate to Setup > Products/Services > Servers
5. Create new server, fill the name with anything you want, hostname as the url to the panel either as an IP or domain. For example: ``123.123.123.123`` or ``my.pterodactyl.panel``
6. Change Server Type to Pterodactyl, leave username empty, fill the password field with your generated API Key.
7. Tick the "Secure" option if your panel is using SSL.
8. Confirm that everything works by clicking the Test Connection button -> Save Changes.
9. Go back to the Servers screen and press Create New Group, name it anything you want and choose the created server and press the Add button, Save Changes.
10. Navigate to Setup > Products/Services > Products/Services
11. Create your desired product (and product group if you haven't already) with the type of Other and product name of anything -> Continue.
12. Click the Module Settings tab, choose for Module Name Pterodactyl and for the Server Group the group you created in step 8.
13. Fill all non-optional fields, and you are good to go!

## Migrating from death-droid's module
Migrating is simple, delete death-droid's module and then upload this one instead of it.  
Then do the steps 3-6 in Installation instructions above and resetup all products.  

## Overwriting values through configurable options
Overwriting values can be done through either Configurable Options or Custom Fields.  

Their name should be exactly what you want to overwrite.  
dedicated_ip => Will overwrite dedicated_ip if its ticked or not.  
Valid options: ``server_name, memory, swap, io, cpu, disk, nest_id, egg_id, pack_id, location_id, dedicated_ip, port_range, image, startup, databases, allocations, oom_disabled, username``

This also works for any name of environment variable:  
Player Slots => Will overwrite the environment variable named "Player Slots" to its value.  

Useful trick: You can use the | seperator to change the display name of the variable like this:  
dedicated_ip|Dedicated IP => Will be displayed as "Dedicated IP" but will work correctly.  

## How to enable module debug log
1. In WHMCS navigate to Utilities > Logs > Module Log
2. Click the Enable Debug Logging button.
3. Do the action that failed again and you will have required logs to debug the issue. All 404 errors can be ignored.
4. Remember to Disable Debug Logging if you are using this in production, as it's not recommended to have it enabled.

## Credits
[Dane](https://github.com/DaneEveritt) and [everyone else](https://github.com/Pterodactyl/Panel/graphs/contributors) involved in development of the Pterodactyl Panel.  
[death-droid](https://github.com/death-droid) for the original WHMCS module.  
[Crident](https://crident.com) for providing me a dev environment to test the module on and the installation video.  

## Hosting Options
[Web Hosting](https://hostmf.com.br)  [VPS Windows](https://hostmf.com.br/vps-windows)  [VPS Linux](https://hostmf.com.br/vps-linux)
