# Gren ANSI

[ANSI escape sequences](https://en.wikipedia.org/wiki/ANSI_escape_code) for [gren](https://gren-lang.org/) [node](https://packages.gren-lang.org/package/gren-lang/node/latest/overview) apps.

```elm
import Ansi
import Stream exposing (Stream)

coolGreeting : Stream -> Cmd msg
coolGreeting stdout =
    "Hello!"
        |> Ansi.wrapItalic
        |> Ansi.wrapColor Ansi.Green
        |> Stream.sendLine stdout
```

See [Ansi module docs](https://packages.gren-lang.org/package/blaix/gren-ansi/latest/module/Ansi) for everything that's available.

There are also functions for controlling the screen and cursor.
See the [gren-tui examples](https://github.com/blaix/gren-tui) for usage in a full program, including interactivity!
