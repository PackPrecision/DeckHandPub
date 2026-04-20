# Installing DeckHand

## Windows (x64)

1. Download `deckhand-windows-x64.exe` from the latest
   [release](https://github.com/PackPrecision/DeckHandPub/releases/latest).
2. SmartScreen may warn — the binary is unsigned for now. Click
   **More info → Run anyway** if you trust the source.
3. On first launch, DeckHand downloads the Scryfall bulk data (~200 MB) into
   `%APPDATA%\DeckHand\data\`. Subsequent launches open instantly.

## First-run data download

DeckHand fetches three files from Scryfall on first launch:

| File                  | Approx. size |
| --------------------- | -----------: |
| `oracle_cards.json`   |       170 MB |
| `rulings.json`        |        25 MB |
| `tagger-tags.json`    |       335 KB |

These are decompressed into a local SQLite database (~220 MB) and a cached
image database (~545 MB) after you browse cards for a while.

## Activating a license

1. Purchase a license (TBD — purchase link will appear on the Releases page).
2. You will receive `deckhand.license` via email.
3. Drop it into `%APPDATA%\DeckHand\` (or click **Help → Install License**
   and select the file).
4. Restart DeckHand. The title bar will show **Licensed** and new cards /
   tags will unlock.

## Uninstalling

DeckHand is portable — delete the `.exe` and `%APPDATA%\DeckHand\` to remove
it completely. No registry keys are written.

## Troubleshooting

**"This database is out of date"**
Force a refresh from **Settings → Data → Re-download bulk data**.

**"License file rejected"**
Check the file is named exactly `deckhand.license` and hasn't been edited.
License files are signed; any modification invalidates them.

**Auto-update fails**
Set **Settings → Updates → Check on launch** to off and update manually by
downloading the latest release.
