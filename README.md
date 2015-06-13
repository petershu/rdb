# rdb v1.1.0

## Usage
rdb [OPTIONS] \<COMMAND\>

## Options
Option | Parameters | Description
-----: | :--------- | :----------
-s | [DeviceSerialNumber] | sends the command to the specified device
-a |  | sends the command to all connected devices (this will override -s)

## Commands
Command | Parameters | Description
------: | :--------- | :----------
dev |  | adb devices & fastboot devices
ds |  | launches Developer Settings
elog | [PackageName] | adb logcat -v threadtime -b events (and filters for a specific package name if specified)
frb |  | fastboot reboot
gitdf |  | checks whether your git working directory has any unstaged changes (using git diff-files)
gitdi |  | checks whether your git working directory has any staged but uncommitted changes (using git diff-index)
gitdr |  | checks whether your git local branch HEAD differs from the remote
gp | [SearchString] | adb shell getprop (and filters using a search string if specified)
help |  | display this manual
helpmd |  | display this manual in markdown format
k | [PackageName\|PID] | kill application with the specified package name or PID (Note: Killing by PID only works on rooted devices)
l | <ComponentName> | adb shell am start
log |  | adb logcat -v threadtime
loge |  | adb logcat -v threadtime *:e
pid | [PackageName\|SearchString] | get PID (process id) by full or partial package name
pkg | [SearchString] | List all installed packages or all matching a specified name
plog | [PackageName] | filters logcat output for a specific package name
pmc | [PackageName] | clears data for the specified application
rb |  | adb reboot
rbb |  | adb reboot bootloader
scp | <ScreenshotSavePath> | captures screenshot from device and saves it to the designated path
scr | <ScreenRecordingSavePath> | captures screen recording and saves it to the designated path
sh | [OptionalAdbShellCommands] | adb shell with optional commands
u | <PackageName> | adb uninstall
view | <URI> | sends an 'android.intent.action.VIEW' intent to open the specified URI

