# Changelog

BandwidthBuddy shows where your drives are plugged in, how fast each
offload route is, and how to cable the cart.

## 0.1.0 — 2026-11-18

First release.

### Added
- **Guided Setup.** The first screen walks you through it: say what each
  drive is (card reader, daily shuttle, larger backup), test everything
  as it's plugged in, see where each drive should go and why, move them,
  and test again for a before and after.
- **The rig, drawn.** Your Mac with its real ports, and each drive hung
  off the port it is on: Thunderbolt enclosures, daisy chains, docks and
  USB hubs, including a hub with nothing plugged into it. Drag a drive to
  the right port if the drawing has it wrong and the app remembers. Macs
  from M1 on are in the port database.
- **Roles and media types.** Mark each drive as card, RAID or shuttle,
  and say what it is: CFexpress, SD, CFast, XQD/SxS, RED MINI-MAG, Codex,
  SSD mag, NVMe, SATA SSD or hard drive. The type sets the speed the app
  expects before anything is tested.
- **Speed tests.** Each drive alone, then card to shuttles, card to RAID,
  card to everything, RAID to shuttles, and every destination writing at
  once. Cards are only read. Test files are deleted afterwards.
- **Where to plug things.** Suggestions weigh a free Mac port, a spare
  port on a Thunderbolt enclosure, or a hub, each costed with the cable
  it shares. Move the drives, rescan, test again, and the two runs are
  shown side by side.
- **Port fit by media type.** For each drive: what its media needs, what
  its connection gives it, and whether that is a good fit, held back,
  sharing, or slow enough to share.
- **Dropped connections.** A drive that macOS keeps resetting is flagged
  from the system log, and speed tests refuse to write to it.
- **Silverstack rundown.** Multi-destination or Cascading Copy, 1st and
  2nd Run, checksum method, verification, ASC MHL, minutes per card and
  cabling. Copy it or export it as Markdown.
- **Demo rig.** A pretend cart to try the app on with nothing plugged in.
- **Check for Updates.** Asks the releases page whether there is a newer
  version, on its own every couple of days only if you say yes. It never
  installs anything itself.
- **Buy Me a Beer.** A code to point a phone at, in Help › Buy Me a Beer.
  Deliberately not a link: the app doesn't send anybody to a payment page.
