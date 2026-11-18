BandwidthBuddy
==============

Shows where your drives are really plugged in, how fast each offload
route is, and how to cable the cart for the fastest offload.

Version 0.2.0. Newest download:
https://github.com/Kunkles/BandwidthBuddy-releases/releases/latest


INSTALLING

Drag BandwidthBuddy.app to your Applications folder and open it.

The first time it reads a camera card or an external drive, macOS asks
whether BandwidthBuddy may access removable volumes. It needs that to
read cards and to write its temporary test files.


USING IT

The first time it opens, BandwidthBuddy shows a short walkthrough on a
practice cart. Nothing it does touches your drives. It is in the Help
menu whenever you want it again.

The one idea to keep: every Thunderbolt port on an Apple silicon Mac is
its own bus. Give each busy device a port of its own if you can help
it. Share a cable only where it costs nothing, like a card reader with
one destination, or slow media on a hub.

Guided Setup
  Start here. Plug in every backup drive and card reader, with a card in
  each reader. Say what each one is: card reader, daily shuttle or
  larger backup. The app tests them as they are plugged in, tells you
  where each one should go and why, and tests again after you move them.

The other screens are the same information without the walk-through.

Rig
  Your Mac, drawn with its ports, and each drive on the port it is
  plugged into. If a drive is on the wrong port in the drawing, drag it
  to the right one. Give each drive a role (card, RAID, shuttle) and a
  media type from the menus on its row. No drives handy? Press Demo rig.

Speed Tests
  Pick a test size and press Run. Each drive is tested alone, then the
  routes a real offload uses. Cards are only read, never written. Test
  files go in a hidden folder on each destination and are deleted when
  the run ends.

Results & Advice
  What limited each route, where each drive should be plugged in, and
  whether each drive's connection suits its media. Move the drives,
  press Rescan, run the tests again, and the two runs are compared.

Silverstack Plan
  A rundown for the Offload Wizard built from your numbers. Setting
  names follow Pomfort's documentation; check them against your version.


GOOD TO KNOW

It does not offload, verify or copy your footage. It measures and
advises.

Speeds are sustained numbers from large sequential test files. Real
offloads of many small files run slower.

A drive that keeps dropping its connection is flagged, and the speed
tests will not write to it. Reading the system log for that needs an
administrator account.

Check for Updates is in the BandwidthBuddy menu. The app never installs
an update itself; it opens the release page.

macOS 14 or later. Made for Apple silicon Macs.
