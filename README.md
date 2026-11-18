# BandwidthBuddy

**A Mac app for DITs and digital loaders that shows where your drives are
really plugged in, how fast each route is, and how to cable the cart for
the fastest offload.** It draws your Mac with its actual ports, hangs each
drive off the port it is on, tests the routes a real offload uses, and
turns the result into a setup rundown for Pomfort Silverstack.

**No release yet.** The first build will appear under
[releases](../../releases) · macOS 14 or later · Apple silicon · free

---

## What it does

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
