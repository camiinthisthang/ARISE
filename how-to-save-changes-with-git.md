# Something to keep in mind

All of the tools we use (git, javascript, phaser, etc.) were created by people like us (in other words, humans). When they were making these tools, these humans made some choices about how to name things.

**They did not always make the best choices for how to name things.**

If you see a word (like commit, stage, key, mkdir, etc.) being used in a way that doesn't make any sense at first, don't worry, it's not just you. Try to figure out what it means, and create your own word for it.

# How to save changes with git

### 1) **Open** the "git bash" command prompt
- find it from the windows icon in the lower-left-hand corner of your screen
- BONUS: figure out how to add a shortcut to your desktop so you can just double-click it in the future?

### 2) **Navigate** to your project repository
- it's probably located somewhere like `Desktop/spring_2018/my-team-name`
- HINT: use the `cd` command

### 3) Check the **status** of your repo

```
$ git status
```

In the example output below, two files have unsaved changes: `another_cool_file.txt` and `cool_sprite.png`. `cool_sprite.png` is inside of a folder called `cool_folder`.

```
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

  modified:   another_cool_file.txt
  modified:   cool_folder/cool_sprite.png

no changes added to commit (use "git add" and/or "git commit -a")
```

- In git-land, "saving" is called "commiting." Like, "I commit to taking out the trash every wednesday night." Or, "I commit to feeding fresh worms to my pet raccoon."

- BONUS: In the example output above, what do you think this phrase means: "Changes not staged for commit."

### 4) Next, **add** the files that you want to commit

```
$ git add another_cool_file.txt
```

You can also add all the files in a folder by using the name of the folder:

```
$ git add cool_folder
```

Check that it worked by running `git status` again. Example output:

```
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

  modified:   another_cool_file.txt
  modified:   cool_folder/cool_sprite.png
```

### 5) **Commit** your changes! Wooooooooooooo! Be sure to include a message describing what new stuff you did.

```
$ git commit --message 'I added new sprites to my game'
```

Example output:

```
[master a128bbb] I added new sprites to my game
 2 files changed, 2 insertions(+)
 ```

- BAM! Now those changes are saved forever in the history of your code repository. If you want to share these changes with other people on your team, you still need to **push** your changes to github.

### 6) `git push`

- Open up the github website for your repo to verify that your changes actually got there.

