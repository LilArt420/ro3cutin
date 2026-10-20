# RO3 Cut In

💬 RO3 Cut-ins
Talk to NPCs the way Ragnarok Online 3 does ✨ One pop-up in the middle of the screen, the speaker as a floating head beside it, and your choices right underneath 🗨️

🌟 What It Changes
🪟 An RO3-style dialogue box: it hangs from the middle of the screen, with a name plate for the speaker and the choices under it. It's drawn in CSS, so it stays sharp at any UI scale 🔍
🙂 Floating heads: the speaker appears beside the box as a 240×240 head-and-shoulders portrait, on the side the script asks for, lined up with the bottom of the box.
🎨 RO3 portraits for the NPCs they match: the Kafra employees, Kafra and Zonda Teleportation, the Prontera, Payon and Morroc soldiers, and Raffam Oranpere of the Sword Clan.
✂️ Every other cut-in becomes a matching head: official cut-ins are cropped to head and shoulders on the fly, with RO3's soft fade at the bottom and the magenta halo cleaned off 🧽
🧑‍🤝‍🧑 Heads for mod NPCs: 107 NPC names from popular mods (standart-npc, arpg-equipments, eden-rework-2021, gear-exchange, cash-shop-extended, random-headgear-box, affix-forge and more) get one of 67 heads, each picked to match the NPC's own sprite 👀 The character's own official art comes first, then someone who looks the same.
🏰 Instance art stays as it was: instance NPCs (Royal Nightmare, Black Sun, Old Glast Heim and the rest) keep their cut-ins at the original size and position, with only the new box and the pop-in.
📜 No scrollbars: long text scrolls with the wheel, and a soft fade shows there's more above or below.
🌈 Readable colours: script colours picked for the old white box are lifted so they read on the dark one.
🎭 RO3 Portraits

Stock cut-in	RO3 portrait	Who
💁 kafra_01, 02, 03 (+ angry, blush)	Kafra 01, 02, 03	the Kafra employees, matched by look
💁 kafra_05, kafra_06 (+ angry, blush)	Kafra 04 (glasses), Kafra 05 (blonde twin tails)	
🌀 kafra_09, kafra_do01	Kafra 04, Kafra 01	the pink-haired Kafra with glasses, Kafra Teleportation
🌀 zonda_01, zonda_do01	Zonda	Zonda staff, Zonda Teleportation
💂 prt_soldier, pay_soldier, moc_soldier	the RO3 town soldiers	Prontera, Payon and Morroc guards
⚔️ laperm01–04	Laperm (idle, happy, serious)	Raffam Oranpere, Sword Clan
⚙️ Settings
In Settings → Mods → ro3-cutins → Settings…:

Setting	Default	What it does
💬 RO3 dialogue style	on	the RO3 pop-up: box in the middle, name plate, choices under it
✨ Cut-in pop-up	on	heads rise in with a gold ring flash, crossfade between expressions and fade out when the talk ends
💾 Installing
In Ragnarok Offline: Settings → Mods → Find Mods → ro3-cutins → Install. Works in both eras, on app 1.6.0 and up. When a new release is out, the Mods tab shows Update available 🔔

🔧 Optional client patch (apply-ro3-dialogue.py, re-run after every app update):
🎥 right-drag rotates the camera while a dialogue has the map frozen
🏷️ cut-ins carry their file name, so instance art is recognised by name. Without the patch, it's recognised by the instance map only.

🛠️ How It's Built
📦 tools/extract_cutins.py: pulls the npcdialog_img_* portraits out of RO3's Unity bundles, through the NpcDialog_Icon atlas.
🧩 tools/build_mod.py: pairs each stock cut-in name with its RO3 portrait and writes the mod.
🙂 tools/mod_heads.py: maps mod NPC names to heads. tools/npc_sprites.py draws each NPC's sprite beside its head, to check the match 👀
✂️ tools/head_crop.py: the head-and-shoulders crop, the same rules the plugin uses at runtime.

🚀 Releases
✅ Every pull request would run validate.yml: mod.json, every .yml with rapidyaml, the release zip's layout, and the app's own manifest reader.
🏷️ Publishing a GitHub Release tagged v<version> would build ro3-cutins-v<version>.zip with release.yml and attach it.
🔮 Coming Up
🖼️ HD portraits: RO3 streams its large npcdialog_rimg_* art from its servers. Once it's been played after the 2026-10-23 maintenance, the bigger art gets re-extracted and swapped in (heads stay 240×240).

🙏 Credits
💬 Lil Art: the mod, the pop-up and the head matching
🎨 Gravity Co., Ltd.: the art, from Ragnarok Online 3 (Genesis) and Ragnarok Online

📜 License
🧑‍💻 The plugin code (client/index.js), the name tables (client/heads.json, client/instance-cutins.json) and the tools would be GPL-3.0.
🚫 The pictures are not ours to license: the RO3 portraits and the RO3 arrow are Gravity's Ragnarok Online 3 art, and the other heads are crops of Gravity's Ragnarok Online cut-ins. They're for personal use only, which is why this mod isn't released 🔒
