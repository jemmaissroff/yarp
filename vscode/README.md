# VSCode YARP LSP

VSCode support for [YARP](https://github.com/ruby/yarp). Currently YARP is under development, so this LSP is acting as a way to minimize the effort for reporting incorrect diagnostics.

## Getting Started
To install, download the latest `yarp-lsp.vsix` release and run the following command:
```
code --install-extension /path/to/yarp-lsp.vsix
```

Once installed, clone the [YARP repository](https://github.com/ruby/yarp), running `rake` to build.

Either add `bin/yarp-lsp` to your path or use the `yarp-lsp.commandPath` override in your VSCode settings.

Finally add `build/librubyparser.dylib` to your local bin path with:
```
ln -s build/librubyparser.dylib /usr/local/lib/librubyparser.dylib.
```

## Features

**Error/Warning diagnostics**

<img width="486" alt="image" src="images/diagnostics.png">

## Reporting issues with diagnostics

If you find an issue with the error/warning diagnostics there are a few ways to report the issue. All ways will generate a new GitHub issue for you to explain what you're observing and what would be expected.

**Quick Fix**

<img width="708" alt="image" src="images/quick-fix.png">

Clicking the `Quick Fix...` button of the diagnostic will bring up a list of the diagnostics that you can report on.

**Command Palette**

<img width="624" alt="image" src="images/command-palette-report.png">

Selecting `YARP: Report issue` from the VSCode Command palette.


**Context menu**

<img width="344" alt="image" src="images/context-report.png">

If you have a code snippet you would like to add to the issue, you can select the snippet, right click, and select `YARP: Report issue` to include it in the generated GitHub issue.
