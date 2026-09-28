Check out our discord for help with modding: https://discord.gg/CxV8ftGfBZ

With the current implementation of modding support you can overwrite all JSON game data.
* Add new Adventures, Persons, Buildings, Resources, Buffs, Abilities, Visitors, Innovations, Tooltips, and FlavorTexts.
* Modify any of the above.

For reference, the actual game data is here:
https://castle-digger.com/game-data/

# Disclaimer

> ⚠️ Mods might break your save game. Export a backup of your save before adding mods.

# Try an example mod
1. Click on one of the JSON files above: `mega-quarters.json` or `phteven.json`.
2. Click the **Raw** button (top right of the file view) and copy the URL from your browser's address bar.
3. Open your save game on castle-digger.com -> settings -> mods.
4. Paste the URL and add it to the list.
5. Reload the game.

`mega-quarters.json` turns all Quarters into Mega-Quarters.
`phteven.json` adds a new person called Phteven, whom you must unlock.

Open settings -> mods for confirmation that the mods were loaded.

# Troubleshooting
* Open the URL in your browser. You should see only JSON text, no web page.
* If the mod isn't listed in `settings -> mods`, reload the game and check the URL again.
* If you want to purge all mods from your save, open the browser console and enter this: `window.ModUrls = []; Save();`. Then reload. This removes all mods; it does not magically repair a broken save.

# Hosting your own mod
The URL must point to the JSON file itself, not to a web page showing it. GitHub raw links (`raw.githubusercontent.com/...`) and Gists work well. Most file sharing services (Dropbox, Google Drive, etc.) will not work, because they don't allow websites to load their files directly. If unsure, use GitHub.

Technical background: the server must send CORS headers and `Content-Type: application/json`. This only applies to the mod file itself, not to images referenced inside it.

# Where can I host my mod?
The file must be reachable as a plain JSON file. GitHub (raw links), GitHub Gist (raw links) and your own web server work. Most file sharing services (Dropbox, Google Drive, WeTransfer, etc.) will not work, because they don't allow websites to load their files directly. If you're unsure, use GitHub.
