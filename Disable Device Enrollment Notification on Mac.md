# Disable Device Enrollment Notification on Mac.md

#### Restart the Mac in Recovery Mode by holding `Comment-R` during restart

##### Open Terminal in the recovery screen and type

```
csrutil disable
```

Restart computer

#### Edit `com.apple.ManagedClient.enroll.plist`

sudo open /Applications/TextEdit.app /System/Library/LaunchDaemons/com.apple.ManagedClient.enroll.plist

change

```
<key>com.apple.ManagedClient.enroll</key>
        <true/>
```

to

```
<key>com.apple.ManagedClient.enroll</key>
        <false/>
````