# DeckHand

A fast, offline-first Magic: The Gathering card search tool for Windows.

> **This repository is for distribution only.** It hosts documentation and
> signed release binaries. Source code lives in a separate private repository.

## Download

Grab the latest installer from the [Releases](https://github.com/PackPrecision/DeckHandPub/releases) page.

Current platforms:

- Windows x64 (`deckhand-windows-x64.exe`)

## What is DeckHand?

DeckHand is a desktop card search tool built on top of Scryfall's bulk data.
It runs entirely offline once the local database is populated — no API calls
per keystroke, no rate limits, no network lag.

- Scryfall-style query syntax (`c:ub t:instant cmc<=3`, etc.)
- Full-text search over oracle text, type lines, flavor, and keywords
- Tag-aware search using Scryfall Tagger data (art & functional tags)
- Card detail pane with rulings, legalities, prices, and high-res images
- ~37k cards · ~1.5M tag associations · ~75k rulings, all local

## Tiers

DeckHand uses a **free-to-download, pay-to-update** shareware model.

| Feature                              | Free | Paid |
| ------------------------------------ | :--: | :--: |
| Search all cards shipped with build  |  ✓   |  ✓   |
| Full-text & tag search               |  ✓   |  ✓   |
| Card detail, rulings, legalities     |  ✓   |  ✓   |
| Deck-building (planned)              |  ✓   |  ✓   |
| Auto-download new Scryfall data      |  ✓   |  ✓   |
| **Access to new cards after release**|      |  ✓   |
| **Access to new tag associations**   |      |  ✓   |
| No nag screen on startup             |      |  ✓   |

The free tier always gets the cards available when you first installed. Cards
released after that sit on-disk, visible in counters but filtered out of
search until you drop in a license file — at which point every new card and
tag unlocks instantly with no re-download.

See [docs/LICENSING.md](docs/LICENSING.md) for the full breakdown.

## Install

See [docs/INSTALL.md](docs/INSTALL.md).

## Auto-updates

DeckHand checks GitHub Releases on launch (once per day, opt-out in
`Settings → Updates`) and prompts before replacing itself. No telemetry; the
only network calls are to `api.github.com` for the release manifest and
`api.scryfall.com` for card data.

## License

DeckHand is proprietary freeware. See [LICENSE](LICENSE) for the full EULA.

Magic: The Gathering, MTG, and all card names/art are trademarks of Wizards
of the Coast LLC. DeckHand is not affiliated with or endorsed by Wizards of
the Coast. Card data courtesy of [Scryfall](https://scryfall.com/).

## Issues & Feedback

Found a bug? Want a feature? Open an issue on this repo — you don't need a
paid license to report problems.
