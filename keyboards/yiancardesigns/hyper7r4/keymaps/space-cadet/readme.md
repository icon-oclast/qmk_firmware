# Hyper7 R4 Space Cadet layout

This keymap includes the APL and Greek symbols similar to the Space Cadet keyboard.

This is an update for the Hyper7 R4 of the incredible work done for the R3 by [bit-shifter](https://github.com/bit-shifter/qmk_firmware/tree/hyper7).
It has been dropped on top of the hard work already done for the R4 by folks like [MegaHakkero](https://github.com/MegaHakkero/vial-qmk-hyper7), [yiancar](https://github.com/qmk/qmk_firmware/tree/master/keyboards/yiancardesigns/hyper7/v4) and others.

This will work with either the classic or the modern variants of the Hyper7R4, with minor caveats.

## Basic Usage
Assuming that you're using the default Hyper7 layout and Space Cadet inspired keycaps,
- Hold the "Top" key to use the APL symbols seen at the top of your keycap
- Hold the "Symbol" or "Greek" key to produce the greek letters
- To get capital greek letters, also hold "Shift"
- Function with L, M, W, or C to set the Unicode mode for your OS, or Function+Mode to cycle through them

## Caveats
This clearly relies heavily on QMK's Unicode features, and has the usual trade-offs of such.
- Don't expect this to work in Vial/Via. Adjust you keymap if you like before compile.
- The Modern layout has a different default ordering of Alt and Hyper keys than Classic. Adjust you keymap if you like before compile.
- OS-specific setup is likely required
- Read the details of the QMK documentation for [Unicode](https://docs.qmk.fm/features/unicode)
- In particular read the OS specifics for [input mode](https://docs.qmk.fm/features/unicode#input-modes)
- This has been tested, albeit only lightly. Patches welcome.
