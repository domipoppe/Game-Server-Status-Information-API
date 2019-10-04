
# PHP API: Game Server Information / Status API

# Currently supported games

 - Mount & Blade: Warband ("game" Parameter: warband)
 - Team Fortress 2 ("game" Parameter: tf2)
 - Mordhau ("game" Parameter: mordhau)
 - Minecraft ("game" Parameter: minecraft

# Upcoming games

- none suggested. If you want a game create an issue.

# Usage/Endpoint

Endpoint: https://api.dominic-poppe.dev/gameserver_information/v1/

https://api.dominic-poppe.dev/gameserver_information/v1/get_information

**Route: get_information**

**Request Type: POST**

**POST Parameters:**
- game (See in top of the currently supported games what parameter you must insert for game)
- serverip (Simply your server IP)
- port (Simply your port)

**Response:**
If the request was valid the header is: 201
UTF-8 JSON:

    { 
    "CurPlayers": "0", 
    "MaxPlayers": "60", 
    "Status": "Online", 
    "Map Name": "Floodplain (Day)", 
    "Server Name": "Jailbreak_Reborn", 
    "Server Build": "1157", 
    "Server Mod": "Napoleonic Wars" 
    }

**Error Handling:**
If there is an error in your call, the API will tell you the issue in a JSON response "error".
If an error appears the header is: 400
Following error messages might appear:

 - The server is not online
 - All parameters: 'game' & 'serverip' & 'port' must have a value!
 - The game XXX is not known - please check our documentation for games this API currently supports
 - get_information expects 'game'/'serverip'/'port'

#

Make sure the port you insert is the correct one, the API is working 100% sure.
I do not store any data of you. The API is free to use for everyone.
If you cause too much requests/traffic I might blacklist the IP.

**I want a game added!**

Post an issue.

**I found an issue**

Post an issue.

**Will you release the sources?**

Maybe, if I added a couple of games.
