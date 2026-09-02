# Borderlands GOTY Enhanced Startup Fix

A simple workaround for startup and launcher problems in Borderlands GOTY Enhanced on Linux and Windows.

## Steam launch options

Open the game's properties in Steam and add the following to **Launch Options**:

```text
%command% -NoLauncher -NoStartupMovies
```

## Bypass the launcher

The workaround is the same on Linux and Windows: preserve the original launcher and make Steam launch the actual game executable instead.

### Linux

Open:

```text
~/.local/share/Steam/steamapps/common/BorderlandsGOTYEnhanced/Binaries/Win64/
```

If your Steam library is stored somewhere else, open the game through:

```text
Steam → Borderlands GOTY Enhanced → Properties → Installed Files → Browse
```

and navigate to:

```text
Binaries/Win64/
```

Rename:

```text
Launcher.exe
```

to:

```text
Launcher.exe.bak
```

Make a copy of:

```text
BorderlandsGOTY.exe
```

and name the copy:

```text
Launcher.exe
```

### Windows

Open:

```text
C:\Program Files (x86)\Steam\steamapps\common\BorderlandsGOTYEnhanced\Binaries\Win64\
```

If your Steam library is stored somewhere else, open:

```text
Steam → Borderlands GOTY Enhanced → Properties → Installed Files → Browse
```

and navigate to:

```text
Binaries\Win64\
```

Rename:

```text
Launcher.exe
```

to:

```text
Launcher.exe.bak
```

Make a copy of:

```text
BorderlandsGOTY.exe
```

and name the copy:

```text
Launcher.exe
```

## Result

The directory should contain:

```text
BorderlandsGOTY.exe
Launcher.exe
Launcher.exe.bak
```

Steam will now start the game executable instead of the original launcher.

## Restore the original launcher

Delete the replacement:

```text
Launcher.exe
```

Then rename:

```text
Launcher.exe.bak
```

back to:

```text
Launcher.exe
```

Steam's file verification can also restore missing or modified game files.

## Notes

A game update or Steam file verification may restore the original launcher and require the workaround to be applied again.

## License

Made by rabbi-lion.

Original text in this repository is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.

Referenced projects, games and third-party material retain their respective rights and licenses.

See `LICENSE` for the full license text.
