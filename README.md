This is a collection of notes and scripts about doing iOS
development from the command line.

## Installing onto the simulator

Installing and running an app on the simulator can be achieved
from the command line.

`runsim` is a script to do so. More about the script is here
<http://psellos.com/ios/iossim-command-line.html>

`installsim` is a script to install an entire .app package onto
the simulator. I got the idea from here:
<http://stackoverflow.com/questions/12964021/script-to-install-app-in-ios-simulator>

## Debugging:

LLDB is the debugger that Xcode uses http://lldb.llvm.org

LLDB works really nice from the command line

    # Attach LLDB to a given process
    $lldb   -attach-name some-app-process

    # Set a breakpoint for an objc method
    (lldb) br s -S fire:

    # Continue to the next line in a breakpoint
    (lldb)n

    # Continue
    (lldb)c

    # Stop
    (lldb)ctrl-c

    # Show all breakpoints
    (lldb) br list

    # Disable all breakpoints
    (lldb) br disable

    # Enable all breakpoints
    (lldb) br enable

There is also a lldb plugin for vim
https://github.com/gilligan/vim-lldb 

## Simulator Log Reading

It is possible to tail the simulator by opening the logs:

    # Read the system log of the simulator
    $ tail -f ~/Library/Logs/iOS\ Simulator/7.0.3/system.log

Imagine all of the possiblities:

    # Read the system log of the simulator
    $ tail -f ~/Library/Logs/iOS\ Simulator/7.0.3/system.log | grep SomeString



