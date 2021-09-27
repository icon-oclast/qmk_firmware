
This is a simple single-purpose keymap for quickly testing the hyper7 physical hardware, even before you have your system ready to properly handle all the fancy stuff.

To easily distinguish physical hardware issues from firmware/keymap/os-configuration issues, this keymap assigns a regular printable ascii character to every key. No macros, no send_string, no unicode, no modifiers, no whitespace. Every key should output a character.  If it does, then your hardware works and you can flash a normal usable keymap in place of this one.

WARNING: This assumes that if you're still testing the hardware you still have access to the physical reset switch on the PCB.  You'll need it to reflash a usable keymap as the typical key-combo for flashing won't work from this keymap.
