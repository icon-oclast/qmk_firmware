
This is a simple single-purpose keymap for quickly testing the hyper7 physical hardware, even before you have your system ready to properly handle all the fancy stuff.

To easily distinguish physical hardware issues from firmware/keymap/os-configuration issues, this keymap assigns a regular printable ascii character to every key. No macros, no send_string, no unicode, no modifiers, no whitespace. Every key should output a character.  If it does, then your hardware works and you can flash a normal usable keymap in place of this one.

Note: This keymap doesn't enable the usual Function-Reset key combo. When ready to flash your next keymap either use the hardware button on the PCB or else hold the top left key ("Help") while plugging in the USB to trigger reset.
