# ucrm-ros-pac-man
PHP-based RouterOS Packet Manager for UCRM API

This is a RouterOS packet manager for the Ubiquiti CRM using the RouterOS API PHP Class by Denis Basta with a lot of custom PHP code. Please feel free to use this to your heart's content. Just please reference me if you change it instead of claiming it as your own.

# NOTE: Your RouterOS Packet Manager must have API port 8728 enabled in IP>Services. If it's not port 8728, the plugin will error out.

# Files Included

# main.php
This file calls the src/exec.php app to execute the function mtikUpdate(). mtikUpdate() will be explained later.

# manifest.json
The basic manifest for a Ubiquiti CRM Plugin. Includes optional fields for having a redundant packet manager in your network.

# src/routeros_api_class.php
This is Denis Basta's vanilla RouterOS API Class.

# src/ucrmInfo.php
This is what contains all of the variables and connection information for the UCRM, including the config options set for the plugin. Also has the function ucrmConnect() which is the cURL query to the UCRM. Utilizes either SSL or not.

# src/exec.php
This is the bread and butter of the plugin. This is what translates all of the UCRM info and puts it into the Mikrotik device. It will also check to see if all of the information from the client is still accurate and if not, it will update it. Calls ucrmInfo.php and routeros_api_class.php

###########

Thank you for using my plugin!
