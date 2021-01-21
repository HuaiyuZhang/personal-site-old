---
layout: post
title: Linux Tricks
---

- `cd -`: return to the last working directory

- `cd ~` or `cd`: return to Home

- `ll` or `ls -l`: list contents of a directory

- `command1; command2; command3` run multiple commands.

- `command1 && command2 && command3` run multiple commands when the previous one succeed.

- `ctrl+r search_term` for reverse searching.

- `ctrl+A`: move to the beginning. `ctrl+E` move to the end

- `tail -f log_file | grep search_term`: read the log file in real time

- use `z` commands, `zcat`, `zless`, `zgrep`, `zdiff` to process files without extracting

- `less` to show less of a file

- `!$`: reuse the last item from the previous command. Often used for file path or names.

- `!!` reuse previous command, for example `sudo !!`

- `ctrl+shift+C` for copy, `ctrl+shift+V` for paste

- empty a file without deleting, just type the file name

- `command --help` for help


---

Reference: https://itsfoss.com/linux-command-tricks/
