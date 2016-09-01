---
title: Driver Documentation
---

## Debug

To be able to debug a reader driver you may need to start pcscd by hand instead of automatically when the reader is connected.

To do that, edit the file /System/Library/LaunchDaemons/com.apple.securityd.plist

Change the file from something like:

    <key>ProgramArguments</key>
    <array>
        <string>/usr/sbin/securityd</string>
        <string>-i</string>
    </array>

to something like:

    <key>ProgramArguments</key>
    <array>
        <string>/usr/sbin/securityd</string>
        <string>-i</string>
    <string>-s</string>
    <string>off</string>
    </array>

Reboot

Source: <http://lists.apple.com/archives/apple-cdsa/2007/Nov/msg00009.html>
