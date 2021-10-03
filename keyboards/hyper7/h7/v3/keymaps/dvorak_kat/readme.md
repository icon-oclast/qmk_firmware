
# Dvorak layouts for the Hyper7

Each of the keycap sets for the Hyper7 handle dvorak slightly differently, and so there are two separate keymaps for Dvorak. The biggest difference between them has to do with the APL layer.

Keyboard-layout-editor format files have been included for reference and to help visualize both of these keymaps.

## KAT Space Cadet

A Dvorak kit was offered during the group buy for KAT Space Cadet. Overall, the positions of APL characters were kept at or near the key they used with Qwerty. While some keys did need to change positions, a logical grouping of the symbols was generally maintained.

`make hyper7/h7/v3:dvorak_kat:dfu`

## DSA Ferrous

Since DSA has the same profile across all rows, keycaps can be placed where needed and the Dvorak package for DSA Ferrous just adds the correct scooped homing keys.  As a result, APL symbols move with the latin glyph they share a key with.

`make hyper7/h7/v3:dvorak_dsa:dfu`

## Misc
### Greek layer

In both keymaps the Greek symbol layer has been adjusted to maintain the pairing with their latin counterparts. Alpha is on "A", Zeta is on "Z", and so forth.  These aren't actually marked on the keycaps of either set and so this was done just to keep things somewhat intuative.

### Top

With the KAT Space Cadet the latin character at the base of the key is what you get when you press the key normally.  To get the APL character marked on the top of the key you would hold down the modifier marked "TOP" while pressing the selected key.

With the DSA Ferrous keyset, the latin characters are at the top of the key with the APL characters marked below them.  So holding down the "TOP" modifier actually gives you the glyph from the bottom of the key.  In the interest of usability, I've resisted the temptation to "fix" this.

## Credit

* This keymap was build on top of the excellent work of bit-shifter and the default layout.
