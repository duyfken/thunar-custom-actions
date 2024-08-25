This is a list of possible Thunar Custom Actions, using established programs.

They are examples and you may not need all of them or may need to tweak them for your distribution. APT for DNF, Mousepad for xed, GTKHash for sha1sum... you get the drift, adjust accordingly.

Drop the [uca.xml](https://github.com/duyfken/thunar-custom-actions/blob/main/uca.xml) file into `~/.config/Thunar/`, or grab an action segment and drop it in your pre-existing `~/.config/Thunar/uca.xml` to activate them on your system.

Most actions are specific to certain filetypes or folders etc. in the [uca.xml](https://github.com/duyfken/thunar-custom-actions/blob/main/uca.xml) but that info. is not visible below.

| Action  | Command | Description
| ------------- | ------------- | ------------- |
| Open Terminal here | `x-terminal-emulator --working-directory=%f`  | Open a terminal in the selected directory |
| Open Thunar as root here | `pkexec thunar %f`  | Open the selected directory as root in Thunar |
| Edit as root | `pkexec mousepad %f`  | Edit file as root with Mousepad |
| Play with Deadbeef | `deadbeef %F`  | Play the selected audio files for playback in Deadbeef |
| Enqueue in Deadbeef | `deadbeef --queue %F`  | Enqueue the selected audio files for playback in Deadbeef |
| Mediainfo | `x-terminal-emulator -e bash -c &quot;mediainfo %F; echo;read -n 1 -s -r -p &apos;Press any key to close.&apos;&quot;`  | Get the mediainfo of selected file/s |
| Extract Here | `xarchiver --extract %F`  | Extract archive without dialogs using Xarchiver |
| Compress | `xarchiver --compress=%F`  | Compress selected file/s into an archive using Xarchiver |
| Checksum | `gtkhash %f`  | Get checksum of the selected file using GTKHash |
| Search with Catfish | `catfish %f`  | Search the selected directory in Catfish |
| Disk Usage | `x-terminal-emulator -e ~/dua i`  | Check disk usage of the directory, using dua binary (that resides in the user&apos;s home directory) |
| Create symlink | `ln -Ts %f %n&quot; (symlink)&quot;`  | Create symlink of the selected file/directory next to the original |
| Install package with APT | `x-terminal-emulator -e bash -c &quot;sudo apt install %F; echo;read -n 1 -s -r -p &apos;Press any key to close.&apos;&quot;`  | Install a Debian package using APT |
| Shred securely | `x-terminal-emulator -e bash -c &quot;shred -fvu %F; echo;read -n 1 -s -r -p &apos;Press any key to close.&apos;&quot;`  | Use shred to delete a file or a folder |
| Compare | `sudo meld %F`  | Compare files using Meld |
