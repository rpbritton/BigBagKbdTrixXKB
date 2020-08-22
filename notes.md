# Running

`qwerty` with `extend` for `ANSI` keyboard:

```bash setxkb.sh -k -l us 4n```

# Enabling mouse keys on an `ANSI` keyboard

Since an `ANSI` keyboard does not have `<LSGT>` (key to the right of left-shift on `ISO`) and most laptop keyboards do not have number lock, it can be hard to enable mouse keys.

Use this command to enable:

```xkbset mousekeys```

Theoretically `xdotool` can do it, but it didn't work for me:

```xdotool key Pointer_EnableKeys```

# Bugs fixes

* `qwerty` ``shift + space` did not produce a space
* Disables `extend`'s'xkb scrolling (falling back to grabbing `mod3 + {w,s}` in sxhkd)
* Stops redirecting `<ESC>` in `extend` since `<ESC>` is caps lock, and that is what it sends instead.
