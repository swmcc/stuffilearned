# Squashing commits 

When in the middle of spiking some code I like to use git
to for 'sanity checkins'. This ensures I don't go too far down a path 
without having the safety net of reverting. If I am refactoring a bit of 
code it is also nice to do short checkins for the same reason.

To aid me in this I have two vim shortcuts.

```vimscript
map ,gaw :!git add . && git commit -m 'WIP'<cr>
map ,gw :!git commit -am 'WIP'<cr>
```

Obviously this isn't good for documenting what I've been doing. So after
several commits I like to do squash them into a single commit with a meaningful
message.

```
$ git rebase -i HEAD~5 # where five is the number of commits I want to squash
```

You'll then be presented with the following summary:

```
pick 314c916 #29 - Added the models to the admin panel
pick c5a9d15 #30 - upgraded django version
pick a879e07 #17 - Added in programmes endpoint
pick edddbe8 Set up codecoverage
pick df3c6a9 Updated __unicode__ for broadcast to include the programme name
```

Simply replace the ones you want to squash with 'squash' and job done.

NOTE: Only do this on commits that haven't been pushed. 
