# Licensing Model

DeckHand ships as **shareware**: the binary is free to download, and a paid
license file unlocks ongoing data updates.

## Why this model?

Curating card data — in particular, re-scraping Scryfall Tagger for new
tags and merging them with each Scryfall bulk drop — takes real time. The
paid tier funds that upkeep. The free tier gives you a fully working search
tool frozen at the state it was in when you downloaded it.

## What's gated

### Free tier

- Every feature of the search UI
- Every card / ruling / tag present in the build you downloaded
- Deck-building (when released) with the cards you have
- Exports (plain text, MTGA, Moxfield, Archidekt)

### Paid tier (license file)

- **New cards** — cards printed after your build's cutoff become searchable
- **New tag associations** — Scryfall Tagger updates (art, functional)
- **New rulings** — rulings issued after your build's cutoff
- **No nag screen** — the startup reminder goes away

## How new data is handled before activation

DeckHand still downloads new Scryfall data on schedule, even without a
license. That data lands in your local database in a "locked" state:

- It's visible in the **Update Status** panel (e.g. *"1,247 new cards
  available — unlock with a license"*).
- It does **not** appear in search results.
- The moment you install a license file, the lock flips and every queued
  card / tag / ruling is live with zero re-download.

This keeps the upgrade path instant: when you pay, the data you've already
downloaded is already there.

## License-file anatomy

A license file is a small signed blob:

```
---- DECKHAND LICENSE v1 ----
email:      you@example.com
tier:       paid
issued:     2026-04-19
expires:    never
signature:  base64(ed25519 signature over the above)
---- END DECKHAND LICENSE ----
```

DeckHand ships with an embedded ed25519 **public key**. Verification is
fully offline — the app never phones home with your license. The only
network calls DeckHand makes are to Scryfall (for data) and GitHub (for
updates).

## Fair use

- One license file covers all devices you personally own.
- Sharing your license file publicly (forums, torrents, pastebins) violates
  the [EULA](../LICENSE) and will invalidate the key used to sign it in a
  future release.
- Refunds within 14 days if the paid features don't work for you.

## Refunds & transfers

Contact the project via a GitHub issue marked `licensing:`.

## Price

TBD — will appear on the Releases page when v0.1.0 ships.
