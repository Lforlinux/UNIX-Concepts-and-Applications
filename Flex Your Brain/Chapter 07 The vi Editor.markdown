### Flex Your Brain

---

01. The three modes of **vi** are: **Command Mode**, **Input Mode** and **ex Mode** (or Last Line Mode).

    The editor starts in Command mode by default. To switch to Input mode, enter one of `i`, `I`, `a`, `A`, `o`, `O`, `r`, `R`, `s` or `S` key. To switch back to Command mode, press the `[Esc]` key. To enter ex mode, switch back to Command mode first if you are currently in Input mode, then press the `:` key followed by ex mode command. ex mode command is executed by pressing the `[Enter]` key, which on completion switches the editor back to Command mode.

##

02. First navigate to the desired line using appropriate navigation keys. Press `I` key to insert text at the beginning of the line. Enter `/*` characters and press `[Esc]` key to switch back to Command mode. Now press `A` key to append text at the end of the line. Enter `*/` characters and press the `[Esc]` key to switch back to the Command mode.

##

03. Since the cursor is still placed at the last character of the line, press `x` twice to delete two characters at the end of the line. Now press `0` to move to the beginning of the line. Again press `x` twice to delete the two characters at the beginning of the line.

##

04. To move to line number 100, enter `:100`.

    To write the lines from that point onwards to the end of the file to a file named `newfile`, enter the ex mode command:

    `:.,$w newfile`.

##

05. This happens when there are unsaved changes in the buffer. To discard the unsaved changes and exit anyways, enter the ex mode command: `:q!`

##

06. (i). `:.,10w foo` : Saves the lines from the current line to 10th line below in a file named `foo`.

    (ii). `:$w! foo` : Saves the last line in a file named `foo`. Overwrite the file `foo` if it already exist.

##

07. Enter the character sequence shown below as it is. Enter the characters as indicated:

    (i). `e`, `a`, enter the characters: ` `, ` -n`, `[Esc]`, `w`, `r"`, `3e`, `2x`, `r"`.

    (ii). `i`, enter the characters: `f`, `[Esc]`, `w`, `a`, enter the characters: `stderr,`, ` `, `[Esc]`.

##

08. By running the `who` command by issuing ex mode command as `:!who`.

    Switch to shell without quitting the editor by issuing ex mode command as `:sh`. Quitting the shell will returns to the editor session.

##

09. Make sure you are in command mode. Then enter the following sequence:

    `:/#include[Enter], 4dd, :1, P`

##

10. `:1,$s/printf(/fprintf(stderr,/g`

##

11. In default configuration, `u` undoes the most recent, single editing change. Subsequent pressing of the key will redo the change.

    When a number of editing changes have been made to a single line, pressing `U` will discard all the changes made since the cursor was moved to the line.

##

12. (i). `:1,10s/cnt/count/g`

    (ii). `:.s/cnt/count/g`

    (iii). `:1,$s/cnt/count/g`

    by changing the flag to `gc` from `g`.

##

13. vi editor stores most of the unsaved buffer in a hidden swap file on disk. The file is automatically removed by the editor upon successful exit.

    If the same file is opened after a crash, the editor complains. In such a case, it is advised to use

    `:recover`

    ex mode command.

##

14. Save the file under a different name after making sure that the file doesn't exist, using the command:

    `:w filename`.

##

15. Copy the file in the home directory by running:

    `cd ; cp /etc/passwd .`

    Start the editor by running:

    `vi passwd`

    Subsequently enter the following ex mode commands one by one:

    `:1,10w passwd1`

    `:11,20w passwd2`

    `:21,$w passwd3`.

##

16. Enter the character sequence shown below as it is. Enter the characters as indicated

    `:1`, `O`, enter the characters: `#include <stdio.h>`, `[Esc]`, `j`, `0`, `l`, `x`, `6e`, `a`, enter the characters: `, int exit_status`, `A`, enter the characters: ` {`, `[Esc]`, `j`, `dd`, `0`, `w`, `i`, enter the characters: `/* `, `[Esc]`, `A`, enter the characters: ` */`, `[Esc]`, `j`, `0`, `w`, `i`, enter the character: `f`, `[Esc]`, `w`, `a`, enter the characters: `stderr, `, `[Esc]`, `2w`, `rE`, `5w`, `i`, enter the characters: `quitting program\n`, `[Esc]`, `j`, `dd`, `0`, `3w`, `s`, enter the characters: `exit_status`, `[Esc]`.

##