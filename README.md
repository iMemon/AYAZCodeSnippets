# AYAZCodeSnippets

_Easy to do trivial things._

Don't waste your time on trivial code even it is easy to write. We focus on making awesome products, right?
If you have some blocks of code, and if they are not private, it is better if you share them to other peers. Now waiting for what? Let's contribute! All of you are welcome warmly!


## How to install?
Xcode provides an area to save snippet code for later using. Press ```Control + Option + Command + 2``` to show
Code Snippet Library (right-lower corner).

Xcode saves its snippets code at location:

```bash
~/Library/Developer/Xcode/UserData/CodeSnippets/
```

Therefore, we will make a git repo which also locate at that location. Do that, we can make snippets to be updated just by pulling/pushing git repo.

So, here is the step by step process to make your snippet go visible on git repository.

```
// Goto Xcode CodeSnippets path
$ cd ~/Library/Developer/Xcode/UserData/

// Check if the CodeSnippets folder exists or not
$ ls CodeSnippets
```

##### Do this if the CodeSnippets folder doesn't exists
```
// Pull the code snippets from GitHub
$ git clone https://iMemon@github.com/iMemon/AYAZCodeSnippets.git CodeSnippets

// Next, pull or push, it is up to you. Recommend that PULL first if your repo is not up-to-date.
```

##### Do this if the CodeSnippets folder already exists
``` 
// Backup CodeSnippets folder
$ cp CodeSnippets CodeSnippetsBackup

// Remove CodeSnippets folder
$ rm -r CodeSnippets

// Pull the code snippets from GitHub
$ git clone https://iMemon@github.com/iMemon/AYAZCodeSnippets.git CodeSnippets

// If you want to merge the exisiting snippets and snippets from repo
cp CodeSnippetsBackup/* CodeSnippets/

// Delete CodeSnippetsBackup folder
$ rm -r CodeSnippetsBackup

// Next, PUSH or PULL, it is up to you. Recommend that PUSH first if your repo is merged!
```

## TroubleShooting

Error: 
```bash
error: The requested URL returned error: 403 while accessing https://github.com/hugo53/iCodeSnippets.git/info/refs?service=git-receive-pack
fatal: HTTP request failed
```

Fix:
```
git remote set-url origin https://username@github.com/username/iCodeSnippets.git
```

May need to change ownership of the Snippets folder and its subfolders

```
chmod -R 777 CodeSnippets/
```

> **Warning: Besure that your code is WILLING to go PUBLIC if you use public git repository!!!**

> Next task: Synchronize Bookmark Documentation.
> Bookmark is saved in ```~/Library/Preferences/com.apple.dt.Xcode.plist``` with key ```Xcode.Organizer.Documentation.Bookmarks```. Just parse this key and get all items. 
