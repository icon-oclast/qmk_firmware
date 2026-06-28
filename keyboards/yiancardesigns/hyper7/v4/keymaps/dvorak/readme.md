
# Dvorak layout and the Hyper7

The Hyper7 is a unique keyboard, but it can present some unusual challenges for non-default layouts.
Most of what's written below is aimed at those wanting to use a space cadet inspired key set for the Hyper7r4, such as those the recent SA group buy. Of course you don't strictly need those keycaps to use this layout, but it's what this layout was designed to match.
If you happen to have an older keyset such as the KAT or DSA Ferrous sets from the Hyper7r3 era that you'd like to use (with either an r3 or r4) let me know, I have the files for those layouts available.
This is a variant of the space cadet layout and so it relies heavily on QMK's Unicode features. If you don't care about Unicode, APL, greek characters or any of the other space cadet inspired features, you might find the Vial keymap easier to work with.
If you're looking to have all the frills of the space cadet layout but type in Dvorak, then this might be for you.

This will work with either the classic or modern varients of the Hyper7r4.

## Dvorak vs remappable
The USB HID spec has a really significant limitation known as US ANSI (QWERTY), and any other layout or language or whatever has to work around that, which usually means remapping keys to behave the way you actually want them to.
At a high level, there are at least two ways to remap your keys for Dvorak.
1. Set Dvorak as your keyboard layout in your OS, and let it handle the mapping. This has the advantage that almost any keyboard you plug into that computer will also type Dvorak. If this is your preferred approach, you probably want to look at the "remappable" layout instead of this one.
2. Set Dvorak mapping in the keyboard firmware. This has the advantage that the keyboard can be plugged into almost any computer that's expecting qwerty and instead type Dvorak. If this is your preferred approach, you are likely in the right place.

## Space Cadet keycaps
Unlike the keycaps available around the time of the Hyper7r3, there isn't a "dedicated" Dvorak space cadet option currently available.
The SA space cadet set doesn't really lend itself to moving keycaps to different rows due to their steep row profile.
The XDA keycaps available with the board don't show the APL symbols, but are a uniform row profile so they can be moved around to other positions as you see fit.
Neither set has the greek symbols marked on it (nor has any other modern space cadet inspired keyset) so their placement is based on the original space cadet keyboard.
Nevertheless, the approach taken by this layout is to keep the APL and greek symbols with their latin counterpart. That is to say, if a key is moved to a different location for a Dvorak layout, the APL and greek symbols move with it.

## Misc
This is essentially just a reordering of the keys and features from the space cadet layout. Check the readme from there for more details on how to use it and be sure to read the QMK Unicode information linked from there.
