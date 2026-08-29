# U-verse

In-place dump of files off a MIPS AT&T U-verse set-top box hard drive. Microsoft Mediaroom on Windows CE.

This may or may not be a complete copy of the disk. Files were pulled as they sat on the drive. Some things at the root look stubbed or truncated. Don't assume the tree is intact, signed, or bootable.

U-verse IPTV is a dead/dying platform. This repo is public archival of abandonware — a record of the software and on-disk layout before the boxes and the backend disappear. It is not here so anyone can steal service, strip DRM, or redistribute video. Copyright stays with Microsoft, AT&T, and whoever else originally owned this stuff.

## What's on the box

Windows Embedded CE 5.0, Broadcom BCM7405, MIPS R4000. The TV client is `tv2clientce` (Mediaroom). Version on this unit: `2.6.31312.24`. Guide/manifest leftovers are from August 2024, Miami (`MIAMFL`).

| Path | What it is |
| --- | --- |
| `nk.bin`, `etc.bin`, `sec.bin` | CE image/partition blobs. Zipped copies sit next to them. |
| `dump/` | Extracted CE system files. The PE binaries here are MIPS Windows CE. |
| `tv2clientce/` | Mediaroom client: UI sounds, fonts, `tv2config.xml`. |
| `Application/` | On-box store and user data — listings, MPF packages, PlayReady leftovers. |
| `*.prf`, `*.ctc`, `*.sig`, `*.bz` | Boot, profile, signature, and error files from the box root. |

The 2 KB `.dll` files sitting in the repo root are not real libraries. Real CE binaries, when they made it into the dump, are under `dump/` and `tv2clientce/`.

This is a filesystem dump, not a project. Nothing here builds or runs on a PC.
