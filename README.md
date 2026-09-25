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

## Install by hand

Download the newest `forever-collector-*.zip` from
[Releases](https://github.com/forever-collector/releases/releases) and unzip it
into `World of Warcraft\_classic_beta_\Interface\AddOns`, so that you end up with
`AddOns\FCollector` and `AddOns\FCompanion`.

## Privacy

Other players only ever appear as salted hashes, class, race, level band and zone. Names, chat,
and trade or mail partners are never recorded. Nothing leaves your computer unless you run
the uploader yourself.
