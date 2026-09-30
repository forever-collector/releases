# Saga

**Every character has a story. Saga writes it down while you play.**

This repository holds the downloads for **Saga** and **Saga Companion**, addons for **World of Warcraft: Forever** and **Retail**, and for **SagaUploader**, the optional program that puts your ledger on [sagaledger.com](https://sagaledger.com).

- **Saga** records your own character's journey in your SavedVariables: sessions, levels, skills, reputation, loot, deaths, gold, and on Retail your gear, Mythic+ keys, boss encounters and PvP matches. It has no network access and sends nothing.
- **Saga Companion** shows that record in game: a ledger window (`/saga ledger`), a recap of your last session at login, a pace strip and a minimap button. On Retail its **Vs Top** tab compares your gear with what the top 100 players of your spec wear. It only reads.

The addons work fully on their own. The website is optional.

## Install the addons

The easiest way to install and update is with the **CurseForge app**: [Saga on CurseForge](https://www.curseforge.com/wow/addons/saga).

**With WowUp:** choose **Get Addons**, then **Install from URL**, then paste `https://github.com/saga-addon/saga`.

**By hand:** download [`saga.zip`](https://github.com/saga-addon/saga/releases/latest/download/saga.zip) and unzip it into your game's AddOns folder:

- Forever: `World of Warcraft\_classic_beta_\Interface\AddOns`
- Retail: `World of Warcraft\_retail_\Interface\AddOns`

You should end up with `AddOns\Saga` and `AddOns\SagaCompanion`. The same zip works in both games.

<details>
<summary>WowUp says "Failed to install" when updating</summary>

This is a known WowUp bug with addons hosted on GitHub ([WowUp#1520](https://github.com/WowUp/WowUp/issues/1520)). Installing from CurseForge avoids it. To keep using the GitHub URL, give WowUp a free read-only token:

1. On GitHub, open **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token** ([direct link](https://github.com/settings/personal-access-tokens/new)).
2. Name it `WowUp` and set **Repository access** to **Public repositories (read-only)**. It needs no permissions.
3. In WowUp, paste it into **Options → Addons → GitHub Personal Access Token**.

</details>

## Put your ledger on the website (optional)

[sagaledger.com](https://sagaledger.com) turns what the addon recorded into your ledger on the web. There you can:

- follow each character over time
- compare characters with friends and guilds
- get Discord posts for your milestones
- share a picture of your week

The uploader is also what brings the latest top-player gear into the in-game **Vs Top** tab.

1. Download [`SagaUploader.exe`](https://github.com/saga-addon/saga/releases/latest/download/SagaUploader.exe) (Windows) and run it.
2. Choose **Connect with Battle.net**. It shows a code and opens your browser.
3. Sign in, check the code matches, and choose **Connect this PC**. There's nothing to copy or paste.

You can also create an upload key on [sagaledger.com/key](https://sagaledger.com/key) and paste it into the same window.

After that it runs as an icon by the clock and uploads every time you log out, starting with Windows unless you untick that box. Right-click the icon for **Upload now**, **Change upload key** and **Quit**.

The uploader is signed (Joshua Fritzjunker, through Microsoft's Artifact Signing) and updates itself. It only installs a new version whose download matches the checksum published with its release. Because it's new, Windows SmartScreen may still show "Windows protected your PC" the first time. If it does, choose **More info**, then **Run anyway**. It keeps its settings and a log in `%APPDATA%\Saga`.

The uploader never changes your saved data while the game is running.

## Privacy

- The addons never touch the network. Nothing leaves your PC unless you run the uploader.
- Other players are never recorded by name: no chat, no trade or mail partners. The combat log is never read.
- `/sagarec export off` stops recording at any time, and `/sagarec status` shows what has been recorded.
- Your ledger on the website is visible only to you. It's shown to others only if you share it or add a character to a group.

More: [sagaledger.com/privacy](https://sagaledger.com/privacy).

## Support

Saga is free and stays free; nothing is locked behind a tip. If you'd like to help cover what it costs to run (servers, the domain, the signed uploader), you can [support Saga on Ko-fi](https://ko-fi.com/sagaledger).

## Commands

| Command | What it does |
| --- | --- |
| `/saga ledger` | open the ledger |
| `/saga recap` | your last session |
| `/saga pace` | show or hide the pace strip |
| `/saga minimap` | show or hide the minimap button |
| `/sagarec status` | what has been recorded |
| `/sagarec export on` / `off` | start or stop recording |

*Saga was called FCollector / FCompanion (Forever Collector) before 0.4. Your old records carry over automatically, the old slash commands still work, and the uploader moves its settings over from `%APPDATA%\ForeverCollector`.*
