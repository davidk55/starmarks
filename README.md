# Simple path storage with Starmarks ⭐

Starmarks is a simple POSIX compliant shell script that allows you to easily add, delete and jump to paths.

**note**: it clears the current screen and you can save up to 9 URLs.

## Usage

<details>
<summary> Adding a path </summary>

```
starmarks -a /home/username/importantDirectory
```

you can also add the current path with `c`

```
starmarks -a c
```

</details>

<details>
<summary> Deleting a path </summary>

```
starmarks -d
```

after that you have to enter the id of the path you want to delete

</details>

<details>
<summary> Jumping to a path </summary>

since scripts are run in a subshell `cd` (used for jumping) will not work, a workaround is to use a `.` before to run it in the current shell instead

```
. starmarks -j
```

after that you have to enter the id of the path where you want to jump to

</details>

## Recommended Aliases

```
sa='starmarks -a'
sd='starmarks -d'
sj='. starmarks -j'
```

## Known Issues

Ctrl+c will exit starmarks but it will not run on the next time, you have to run it again. Currently I don't really know how to fix this.

**Workaround**: press Enter or any other key than the id's instead of Ctrl+c to stop starmarks
