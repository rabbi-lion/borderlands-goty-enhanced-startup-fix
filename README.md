# Borderlands GOTY Enhanced Startup Fix

A workaround for startup and launcher problems in Borderlands GOTY
Enhanced on Linux and Windows.

## Steam launch options

Open the game's properties in Steam and add the following to
**Launch Options**:

```
%command% -NoLauncher -NoStartupMovies
```

## Bypass the launcher

The workaround is the same on Linux and Windows: preserve the
original launcher, and make Steam launch the actual game executable
instead.

The steps are identical on both platforms — only the path differs.

### Linux

The default Steam path is:

```
~/.local/share/Steam/steamapps/common/BorderlandsGOTYEnhanced/Binaries/Win64/
```

If your Steam library is stored elsewhere, open the game through
`Steam → Borderlands GOTY Enhanced → Properties → Installed Files →
Browse` and navigate to `Binaries/Win64/`.

### Windows

The default Steam path is:

```
C:\Program Files (x86)\Steam\steamapps\common\BorderlandsGOTYEnhanced\Binaries\Win64\
```

If your Steam library is stored elsewhere, open the game through
`Steam → Borderlands GOTY Enhanced → Properties → Installed Files →
Browse` and navigate to `Binaries\Win64\`.

### Steps

In the game directory, for your platform:

1. Rename `Launcher.exe` to `Launcher.exe.bak`.
2. Make a copy of `BorderlandsGOTY.exe`.
3. Name the copy `Launcher.exe`.

## Result

The directory should contain:

```
BorderlandsGOTY.exe
Launcher.exe
Launcher.exe.bak
```

Steam will now start the game executable instead of the original
launcher.

## Restore the original launcher

Delete the replacement `Launcher.exe`, then rename `Launcher.exe.bak`
back to `Launcher.exe`.

Steam's file verification can also restore missing or modified game
files.

## Notes

A game update or Steam file verification may restore the original
launcher and require the workaround to be applied again.

## License

Made by rabbi-lion.

Original text in this repository is licensed under the Creative
Commons Attribution-ShareAlike 4.0 International License.

Referenced projects, games, and third-party material retain their
respective rights and licenses. See `LICENSE` for the full license
text.
