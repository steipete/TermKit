# Development notes

## Debug the example in Xcode

Open the package in Xcode and select the `Example` scheme. Because the example needs an interactive terminal, edit the scheme's **Run > Info > Launch** setting to **Wait for the executable to be launched** before starting the debugger.

Launch the built `Example` executable from a separate terminal. This command prints SwiftPM's current binary directory:

```sh
swift build --show-bin-path
```

## Watch TermKit logs

TermKit's internal diagnostics use the macOS unified logging subsystem `termkit`. Stream those messages from another terminal while the application runs:

```sh
log stream --style compact --predicate 'subsystem == "termkit"'
```
