# Multiple Choice Questions for The Missing Semester

Please consult [Lecture 1, 2 and 4](https://missing.csail.mit.edu/2020/) from The Missing Semester.

Answer the following questions by editing this file by replacing the `[ ]` for the correct answer with `[x]`.
Only one choice per question is correct.
Selecting more than one choice will result in zero points.
No other changes to the text should be made.

1. Which permission(s) (listed as `rwx` by `ls -l`) for the directory `dir` are required to remove the file `dir/file` by calling `rm dir/file`?

    - [ ] a) only write (`-w-`)
    - [ ] b) only execute (`--x`)
    - [x] c) both write and execute (`-wx`)
    - [ ] d) all permissions (`rwx`)

2. Which permission(s) (listed as `rwx` by `ls -l`) for the directory `dir` are required to list its contents and permissions with the `ls -l` command?

    - [ ] a) only read (`r--`)
    - [ ] b) only execute (`--x`)
    - [ ] c) both read and write (`rw-`)
    - [x] d) both read and execute (`r-x`)
    - [ ] e) all permissions (`rwx`)

3. Which permission(s) (listed as `rwx` by `ls -l`) for the directory `dir` are required to create an empty file within it by calling `touch dir/empty_file`?

    - [ ] a) only write (`-w-`)
    - [ ] b) only execute (`--x`)
    - [ ] c) both read and write (`rw-`)
    - [ ] d) both read and execute (`r-x`)
    - [x] e) both write and execute (`-wx`)
    - [ ] f) all permissions (`rwx`)

4. Which is the shortest way to change the working directory to your home directory (assuming your username is `user`)?

    - [ ] a) `cd $HOME`
    - [ ] b) `cd home`
    - [ ] c) `cd /home`
    - [ ] d) `cd /home/user`
    - [x] e) `cd`

5. Which of the following uses of `chmod` will remove the write and execute permissions to `file` for all users which are not the owner of `file` and are not part of the group which owns `file`?
   The permissions for the file owner and the group which owns the file must remain unchanged.
   *HINT:* See the manual (`man chmod`) and [File permissions and attributes on the Arch Linux wiki](https://wiki.archlinux.org/index.php/Chmod).

    - [ ] a) `chmod o=r file`
    - [ ] b) `chmod -wx file`
    - [ ] c) `chmod +r-wx file`
    - [x] d) `chmod o-wx file`

6. Select the following use of `chmod` which modifies the permissions of `file` such that:
   (1) the user that owns `file` has `rwx` permissions.
   (2) the group that owns `file` has `r-x` permissions.
   (3) other users have no permissions (`---`).

    - [x] a) `chmod 750 file`
    - [ ] b) `chmod 760 file`
    - [ ] c) `chmod urwxgrxo-rwx file`
    - [ ] d) `chmod u+rwx g+rx o-rwx file`
    - [ ] e) `chmod u+rwx file`

7. What does the following shell script do?

    ```sh
    for file in $(ls dir/*.py); do
        mv "$file" $(echo "$file" | sed -E 's/\.py$/\.go/')
    done
    ```

    - [ ] a) moves the file `file` into `dir` if it has the `.py` file suffix
    - [ ] b) moves the file `file` into `dir` if it has the `.py` suffix, then gives it the `.go` suffix
    - [x] c) renames any file within `dir` with the `.py` suffix to have the `.go` suffix
    - [ ] d) moves any files with a `.py` or `.go` suffix out of `dir`
