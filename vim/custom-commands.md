# Custom commands

Custom commands in Vim are defined via the `command` command. As I learn new
things throughout the week, I like to write them down in a `TIL.md` file. I
found myself constantly running `,e` to open my [notes.md](https://github.com/swmcc/dotfiles/blob/master/vim/.vimrc) file in a
new tab. To streamline the process, I added the following to my `.vimrc`:

```vimscript
command TIL tabe~/Dropbox/notes/TIL.md
```

Now, whenever I want to write down something I've learned I can just run `:TIL`.
I wanted a different workflow that `,e` as that has now become my project/todo notes.

NOTE: User-defined commands _must_ start with a uppercase letter.
