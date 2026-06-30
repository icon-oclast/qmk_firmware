
# Remappable layout for the Hyper7

The Hyper7 is a unique keyboard, but it can present some unusual challenges for non-default layouts.
Most of what's written below is aimed at those wanting to use a space cadet inspired key set for the Hyper7r4, such as those the recent SA group buy. Of course you don't need those keycaps to use this layout, but the space cadet features of the layout was based on that.

Although Dvorak is mentioned as an example of a non-default layout, it is just one example and this is intended to work with whatever key mapping you prefer. If you're using this with a mapping other than dvorak however, you will want to change the include on line 6 of keymap.c.

This is a variant of the space cadet layout and so it relies heavily on QMK's Unicode features. If you don't care about Unicode, APL, greek characters or any of the other space cadet inspired features, you might find the Vial keymap easier to work with.

If you're looking to have all the frills of the space cadet layout but with a different key mapping, such Dvorak for example, then this might be for you.

This will work with either the classic or modern varients of the Hyper7r4.

## Space Cadet vs. remappable layout
The USB HID spec has a really significant limitation known as US ANSI (QWERTY), and any other layout or language or whatever has to work around that, which usually means remapping keys to behave the way you actually want them to.
At a high level, there are at least two ways to remap your keys for your preferred layout.
1. Set a layout mapping in the keyboard firmware. This has the advantage that the keyboard can be plugged into almost any computer that's expecting qwerty and instead type your remapped layout. If this is your preferred approach, you probably want to look for a dedicated layout keymap (such as "Dvorak" for example) instead of this one.
2. Set a layout in your keyboard configuration of your OS, and let it handle the mapping. This has the advantage that almost any keyboard you plug into that computer will also type your selected layout. If this is your preferred approach, you are likely in the right place.

## What it does
The Hyper7 is an unusual keyboard and has some unusual keys.
Using the SA space cadet keycaps as an example, The key just left of the "1" on the number row produces either a ":" or if you hold shift then a "~". Meanwhile, the key just right of the "L" on the home row produces a ";" or if you hold shift then a "`". Neither of these are typical for most keyboards, and there's some slight-of-hand going on behind the scenes to make it work. Your OS doesn't know anything about this and so when it remaps your keys you get some surprising results. If you've configured for Dvorak for example, you'll suddenly find that lowercase "s" and uppercase "S" are now on opposite sides of the keyboard!

As you may have already guessed there's a pretty simple fix for this which is basically to restore some of these specialty keys to their US ANSI behavior. The trade-off is that even when switching to qwerty mode these keys won't be exactly what they keycap shows, but you'll have a lot less trouble typing with your preferred OS remapping configuration.
The intent here is to retain as much of the space cadet layout feature set while only replacing those that cause problem for typing in a non-default layout. In a sense you can think of this as "space cadet lite".

## Caveats
As mentioned previously, USB only understands US ANSI (QWERTY) and anything else is a software hack required to work around this limitation. Sometimes these workarounds trip over each other.
The most obvious form of this is with Unicode. Every OS handles Unicode differently, all require some configuration to enable it, most require special additional software as well.
As one example, the QMK Unicode entry for Linux/ibus uses Ctrl-Shift-U as a hot-key prefix (the default for ibus), but once you apply a dvorak keymap, it comes across as Ctrl-Shift-G instead. If you try to outsmart it by changing the ibus trigger to Ctrl-Shift_G you'll find that many terminal emulators have special handling of Ctrl-G ("bell") that may or may not take precedence over the ibus handing, depending on which app you're using. The QMK trigger key can be changed as well, but you'll need to modify the config before you compile.
An another example, the bottom row of the upper panel on the Hyper7 is a combination of Unicode keys and things that are likely to get remapped by your chosen layout. Hitting the question mark with a Dvorak layout will produce an uppercase "Z", and the angle brackets will give you "W" and "V". Reverse mapping these is going to be layout specific and so not handled by this keymap.
In addition to Unicode, a number of special behaviors in this keymap make use of the sendstring() function. This is another thing that remapping keys will likely break. There is a workaround, but it is layout specific. Currently on line 6 of keymap.c we include the table to compensate for dvorak remapping and so sendstring should work as expected, but if you're using a different layout you'll want to change that line accordingly. See the QMK docs for [language-specific](https://docs.qmk.fm/reference_keymap_extras) details.
These are just a few examples, you will undoubtedly run across others. The main focus of this keymap has been to make the main typing layout work well enough to be usable out-of-the-box when remapped by the OS, and otherwise retain as much of the space cadet setup as possible.
It may be best to think of this as a starting point for your own personal configuration.

## Misc
This is essentially just a reordering of the keys and features from the space cadet layout. Check the readme from there for more details on how to use it and be sure to read the QMK Unicode information linked from there.
