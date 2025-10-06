✨ Highlights

Character Management

Lookup by CharName (PS_GameData.dbo.Chars)

Fast edits: Hair/Face/Size/Sex, Level/Mode, Stat/Skill Points, STR/DEX/REC/INT/WIS/LUC, Kills/Deaths/Wins/Defeats

Clear All Fields button

Every change is logged (see Logs tab)

Account Management

Lookup by UserID (PS_UserData.dbo.Users_Master)

Edit Password (plain + MD5), Admin (bool), Status, Points

NEW: AdminLevel (0–255) with its own Apply + included in Apply All

Statistics

Lightweight inventory viewer: RowID | ItemID | ItemName for the selected character

Selecting a row auto-fills the RowID in Item Management

Item Management (Quick Edit)

Edit by RowID (PS_GameData.dbo.CharItems)

Fields Gem1..Gem6 + Apply Gems

Craftname + Apply Craftname

Apply All (Gems + Craftname)

Load pulls current values from DB

Tools / Options

Light/Dark Theme toggle

Polished UI (readable buttons, spacing, focus states)

Logs

AdminPanel.Logs (RichTextBox): every edit is timestamped

Clear Logs button

Commands List

/char on/off
/attack on/off
/amove "Charname"
/bmove x z map
/cmove mapid
/warning charname "message"
/watch
/cwatch
/silence charname on/off
/stop charname on/off
/mmake mobid
/nmake npcid
/notice "message"
/gmnotice
/cure charname
/autocure charname
/quiry charname
/kick charname

🧩 Databases & Tables

PS_GameData: dbo.Chars, dbo.CharItems (+ PS_GameDefs.dbo.Items for names)

PS_UserData: dbo.Users_Master

Required permissions: SELECT/UPDATE on these tables.

🚀 Getting Started

Launch Admin Panel → SQL connection window

Windows or SQL Server auth

Server (e.g., localhost, .\SQLEXPRESS)

Databases: PS_GameData & PS_UserData

Character Management: type CharName → OK

Statistics: type CharName → Load (view RowID/ItemID/Name)

Item Management: paste RowID, Load, edit Gems/Craftname, Apply

Craftname format example: 01020304050607080920
01..09 = STR/DEX/REC/INT/WIS/LUC/HP/MP/SP (0–40)
20 = enchant tag (20 or 70)

🧯 Safety & Logs

Every edit writes a line to Logs (timestamp + details).

Strongly recommended: backup DB before use on production.

The panel only touches the tables listed above.

⚖️ Credits

© [Dev]Dovakhiin 2025 — Free for the Shaiya community.
Please keep credits. 💙
