# Forever Collector — releases

Downloads for **FCollector** and **FCompanion**, the World of Warcraft: Forever addons behind
[forever-collector.vercel.app](https://forever-collector.vercel.app). This repository holds
release zips only.

- **FCollector** records what you do while you play into your own SavedVariables. It has no
  network access and sends nothing.
- **FCompanion** shows what FCollector recorded: a ledger window (`/fcompanion ledger`), a
  recap of your last session at login, a pace strip, and a minimap button. It only reads.

## Install with WowUp

1. Open WowUp and choose **Get Addons**, then **Install from URL**.
2. Paste `https://github.com/forever-collector/releases` and install.
3. Both addons arrive together in one zip. WowUp keeps them updated from here.

### If WowUp says "Failed to install" when updating

This is a known WowUp bug with every addon hosted on GitHub
([WowUp#1520](https://github.com/WowUp/WowUp/issues/1520)). WowUp only downloads updates
correctly when a GitHub token is set. A free, read-only token fixes it for good:

1. On GitHub, open **Settings → Developer settings → Personal access tokens → Fine-grained
   tokens → Generate new token**
   ([direct link](https://github.com/settings/personal-access-tokens/new)).
2. Name it `WowUp`, set **Repository access** to **Public repositories (read-only)**, and
   generate it. It needs no permissions.
3. In WowUp, paste it into **Options → Addons → GitHub Personal Access Token**.

Then update as normal. Without a token, removing the addon and installing it again from the
URL above also works.

## Install by hand

Download the newest `forever-collector-*.zip` from
[Releases](https://github.com/forever-collector/releases/releases) and unzip it
into `World of Warcraft\_classic_beta_\Interface\AddOns`, so that you end up with
`AddOns\FCollector` and `AddOns\FCompanion`.

## Show your ledger on the website (optional)

The addons work fully in game on their own. To also see your ledger at
[forever-collector.vercel.app](https://forever-collector.vercel.app):

1. Sign in there with Battle.net, open **Key**, and create an upload key.
2. Download **ForeverCollectorUploader.exe** from the newest
   [release](https://github.com/forever-collector/releases/releases/latest) and run it.
3. Paste your key when it asks (it will not be shown as you paste). Answer **Y** to start it
   with Windows, and it uploads by itself every time you log out of the game.

Windows may say **"Windows protected your PC"** the first time, because the program is new and
not yet code-signed. Choose **More info**, then **Run anyway**.

Handy options, run from a terminal: `ForeverCollectorUploader.exe --setup` enters a new key,
`--startup off` stops it starting with Windows, and `--once` uploads once and exits. It keeps its
settings and a log in `%APPDATA%\ForeverCollector`.

## Privacy

Other players only ever appear as salted hashes, class, race, level band and zone. Names, chat,
and trade or mail partners are never recorded. Nothing leaves your computer unless you run
the uploader yourself.
