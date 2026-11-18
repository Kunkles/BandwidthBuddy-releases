# BandwidthBuddy

**A Mac app for DITs and digital loaders that shows where your drives are
really plugged in, how fast each route is, and how to cable the cart for
the fastest offload.** It draws your Mac with its actual ports, hangs each
drive off the port it is on, tests the routes a real offload uses, and
turns the result into a setup rundown for Pomfort Silverstack.

**[Download BandwidthBuddy](../../releases/latest/download/BandwidthBuddy.zip)** ·
macOS 14 or later · made for Apple silicon · free · [all releases](../../releases/latest)

---

## What it does

### One device per bus

The idea the app is built on: every Thunderbolt port on an Apple silicon
Mac is its own bus with its own bandwidth. Give each busy device its own
port if you can help it. Two fast drives on one port, through a daisy
chain, a dock or a hub, split a single cable. Sharing is fine where it
costs nothing: a card reader with one destination, since one is read and
the other written, or slow media on a hub. A short walkthrough on a
practice cart shows all of it the first time the app opens.

### Guided setup

The first screen walks you through it. Plug in every backup drive and
card reader. Say what each one is: card reader, daily shuttle, or larger
backup. The app tests them as they are plugged in, shows where each one
should go and why, and tests again once you have moved them, so you end
with a before and after.

### See the rig

BandwidthBuddy reads which Thunderbolt enclosure, daisy chain, dock or USB
hub each drive sits behind and draws it on a picture of your Mac. If a
drive is drawn on the wrong port, drag it to the right one and the app
remembers that for your Mac model. Macs from M1 on are in its port
database.

### Say what each drive is

Give each drive a role (card, RAID, shuttle) and a media type: CFexpress,
SD, CFast, RED MINI-MAG, Codex, NVMe, SATA SSD, hard drive and so on. The
type sets how fast the app expects it to go before you have tested
anything.

### Test the routes

Each drive alone, then card to shuttles, card to RAID, card to everything,
RAID to shuttles, and every destination writing at once. Cards are only
read, never written. Test files are deleted afterwards.

### Get told what to move

The app suggests where each drive should go: its own Mac port, the spare
port on a Thunderbolt enclosure, or a hub. It costs each option with the
bandwidth that cable shares, so fast media gets its own port and slow
media stops taking one. Move the drives, rescan, test again, and it shows
the two runs side by side.

### Catch a bad connection

A drive on a marginal cable or an underpowered hub can stay mounted while
macOS keeps resetting it underneath. BandwidthBuddy reads the system log
for that, warns you, and will not write test files to a drive that is
dropping.

### Silverstack rundown

Multi-destination or Cascading Copy, which drives go in the 1st and 2nd
Run, checksum method, verification behaviour, ASC MHL, minutes per card
and the cabling. Copy it or export it as Markdown. Setting names follow
Pomfort's documentation; check them against your Silverstack version.

## What it does not do

It does not offload, verify or copy your footage. It measures and advises.
Speeds are sustained numbers from sequential test files; real offloads of
many small files run slower.

## Updates

**BandwidthBuddy › Check for Updates…** asks this repository for the latest
release. It can also look on its own every couple of days, but only if you
say yes when it asks on first launch. Nothing about you, your Mac or your
drives is sent. The app never installs anything itself: it shows what
changed and opens the release page.

## Beer

Made by a DIT who got tired of guessing which port was the slow one.
BandwidthBuddy is free. If it saved you an offload, there is a code to
point a phone at in **Help › Buy Me a Beer**.

## Trademarks

Silverstack is a trademark of Pomfort GmbH. Thunderbolt is a trademark of
Intel Corporation. Mac and macOS are trademarks of Apple Inc. Other product
names belong to their owners. No affiliation or endorsement.

---

## Changelog

BandwidthBuddy shows where your drives are plugged in, how fast each
offload route is, and how to cable the cart.

### 0.2.1 — 2026-11-18

#### Fixed
- **Sidebar names.** The screen list down the left showed only icons;
  Guided Setup, Rig, Speed Tests, Results & Advice and Silverstack Plan
  are named again.
- **The walkthrough no longer covers the screen.** It sat over the
  bottom-right corner, on top of the drives and buttons it was describing.
  It is now a bar under the screen, which scrolls above it, and Next
  stays in one place from page to page.

#### Changed
- A first window opens larger, with room for the Mac, a row of drives
  and a chained drive under them. A window you have already sized keeps
  its size.

### 0.2.0 — 2026-11-18

#### Added
- **Walkthrough.** Opens on first launch and any time from Help ›
  BandwidthBuddy Walkthrough. It runs on a practice cart, so nothing it
  shows touches your drives, and takes you through Guided Setup, the rig,
  a drive that keeps dropping, and the Silverstack rundown.
- **One device per bus.** The walkthrough opens with the idea the whole
  app is built on: every Thunderbolt port is its own bus, so give each
  busy device its own port if you can help it, and share a cable only
  where it costs nothing: a card reader with one destination, or slow
  media on a hub. The Layout step in Guided Setup leads with the same
  rule.

#### Changed
- The question about checking for updates automatically is now a page of
  the walkthrough rather than a dialog on first launch. Skip the
  walkthrough before reaching it and you are asked once when it closes.
- Leaving the demo rig clears its drives straight away instead of when
  the scan of your own finishes.

### 0.1.0 — 2026-11-18

First release.

#### Added
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
