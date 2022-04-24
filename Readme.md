# mozdevice - fork

mozdevice is an rust adb client, its the most complete one I could find at the time.

I made this fork, because I have no idea how the mozilla dev stuff works and even less clue about the mercurial VCS.

it's forked from https://hg.mozilla.org/mozilla-central/file/tip/testing/mozbase/rust/mozdevice

at "Deployed from [4351c386f60d](https://hg.mozilla.org/hgcustom/version-control-tools/rev/4351c386f60d) at 2022-03-16T17:25:32Z."

## Changes I did:

- make struct fields `RemoteDirEntry` and `RemoteFileMetadata` public
- list does not fail on special file types anymore (Character, Socket, Block and NamedPipe)
  - thanks to https://www.livefirelabs.com/unix_tip_trick_shell_script/unix_operating_system_fundamentals/file-types-in-unix.htm for the info about the different file types
- make `Device::list_dir_flat` public and document that `Device::list_dir` is recursive