pebble-sdk-characterRegex
=========================

Pebble SDK release 001 patch to support unicode in 'characterRegex' filter of a font manifest

This is a trivial patch to the Pebble SDK version 001 which addresses one
simple problem: inability to use unicode regular expressions in the
"characterRegex" field of a font definition in resource_map.json.

The "characterRegex" parameter is used to filter only necessary characters from
the TTF font to be included in the bitmap resource used by Pebble app. Any
Python regex can be specified here, but only ascii encoded ones are supported
by the SDK tools. This patch fixes this issue. 


Installing the patch 
--------------------

Execute the following command, replacing $(SDK) by the path to the Pebble SDK
installation folder.

        patch -d $(SDK) -p1 < patch.txt


