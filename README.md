# Gren ANSI

Control terminal text, cursor, and screen with ANSI escape sequences in Gren.

```elm
import Ansi
import Stream exposing (Stream)

coolGreeting : Stream -> Task Never {}
coolGreeting stdout =
    "Hello!"
        |> Ansi.wrapItalic
        |> Ansi.wrapColor Ansi.Green
        |> Stream.sendLine stdout
```

See [Ansi module docs](https://packages.gren-lang.org/package/blaix/gren-ansi/latest/module/Ansi) for everything that's available.

There are also functions for controlling the screen and cursor.
See the [gren-tui examples](https://github.com/blaix/gren-tui) for usage in a full program, including interactivity!
