# Front-End Course from Kottans. Michael's endeavor :)

## Stage 0. Self-Study

### General
- [x] 0. [Git Basics](https://github.com/kottans/frontend/blob/master/tasks/git-intro.md)
- [ ] 1. [Linux CLI and Networking](https://github.com/kottans/frontend/blob/master/tasks/linux-cli-http.md)
- [ ] 2. [VCS (hello gitty), GitHub and Collaboration](https://github.com/kottans/frontend/blob/master/tasks/git-collaboration.md)

### Front-End Basics
- [ ] 3. [Intro to HTML & CSS](https://github.com/kottans/frontend/blob/master/tasks/html-css-intro.md)
- [ ] 4. [Responsive Web Design](https://github.com/kottans/frontend/blob/master/tasks/html-css-responsive.md)
- [ ] 5. [HTML & CSS Practice](https://github.com/kottans/frontend/blob/master/tasks/html-css-popup.md)
- [ ] 6. [JavaScript Basics](https://github.com/kottans/frontend/blob/master/tasks/js-basics.md)
- [ ] 7. [Document Object Model](https://github.com/kottans/frontend/blob/master/tasks/js-dom.md) - practice

### Advanced Topics
- [ ] 8. [Building a Tiny JS World (pre-OOP)](https://github.com/kottans/frontend/blob/master/tasks/js-pre-oop.md) - practice
- [ ] 9. [Object oriented JS](https://github.com/kottans/frontend/blob/master/tasks/js-oop.md) - practice
- [ ] 10. [OOP exercise](https://github.com/kottans/frontend/blob/master/tasks/js-post-oop.md) - practice
- [ ] 11. [Offline Web Applications](https://github.com/kottans/frontend/blob/master/tasks/app-design-offline.md)
- [ ] 12. [Memory pair game](https://github.com/kottans/frontend/blob/master/tasks/memory-pair-game.md) — real project!
- [ ] 13. [Website Performance Optimization](https://github.com/kottans/frontend/blob/master/tasks/app-design-performance.md)
- [ ] 14. [Friends App](https://github.com/kottans/frontend/blob/master/tasks/friends-app.md) - real project!
________________________________________________


## 0. Git Basics

- [x] Finish the course [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)

  I have created the 'Version Control with Git [Udacity] set of flashcards on [memecode](https://www.memcode.com/users/1823) to better memorize all of these GIT commands. I'm going to add more commands to the flashcards as I learn new ones elsewhere.

  Unfortunetely, the flashcards make me memorizie the commands in the *command -> definition* manner. Now and then, I need to revise them in the *command <- definition* manner or just have sth for a quick reference, which is why I've put the list of all the commands in the table below:

<details>
  <summary>Click to see the table</summary>
  
|#|Git command|Explanation
|---|:---|---
|1.| `git pull --rebase` | Ensures that changes made to the local repo are put on top of the changes made in the remote (коротка форма для `git fetch` а потім `git rebase`)
|2.| `git push`| Uploads local repository content to a remote repository
|3.| `git pull`| Fsetches and downloads content from a remote repository and immediately updates the local repository to match that content (*просто коротша форма для `git fetch` а потім `git merge`*)
|4.| `git fetch`| Downloands all changes from a remote repository <remote> (commits, files, and refs) into your local repo, BUT don't merge/integrate them into HEAD. Fetching is what you do when you want to see what everybody else has been working on. ... This makes fetching a safe way to review commits before integrating them with your local repository.
|5.| `git rebase x`, where x is the name of branch on which you put the current branch| Applies any commits of current branch ahead of specified one, meaning, it takes all the changes that were committed on one branch and replay them on a different branch. This way of merging makes for a cleaner history. If you examine the log of a rebased branch, it looks like a linear history: it appears that all the work happened in series, even when it originally happened in parallel.
|6.| `git reset --hard HEAD^`| Erases the latest commit. Resets your HEAD pointer to a previous commit and discards all changes since then. You can use it, for example, to undo the merge if you make a merge on the wrong branch
|7.| `git reset HEADx`, where x is the required reference (`^`, `^^`, `^2`, etc.)| move the HEAD (current branch pointer to a referenced commit
|8.| `git reset --soft HEAD^`| Moves committed changes to the staging index of the latest commit
|9.| `git reset --mixed HEAD^`| Unstages previously committed changes of the latest commi
|10.| `git reflog`| Git does keep track of everything for about 30 days before it completely erases anything. This command is used to access this content
|11.| `git show HEAD^^^2` or `HEAD~2^2`| Refereneces the second parent of the grandparent of a the current merge commit
|12.| `git show HEAD^^` or `HEAD~2`| Refereneces grandparent of the current commit
|13.| `git show HEAD^^^` or `HEAD~3`| Refereneces great-grandparent of the current commit
|14.| `git show SHA^2`, where SHA is the SHA of a merge commit| References the second parent of a merge commit
|15.| `git show HEAD^` or `HEAD~` or `HEAD~1`| Refereneces the parent commit of the current commit
|16.| `git commit --amend`| Додає все з **останнього** коміту в проміжну область для виправленого коміту. Якщо ви помітили, що ви зробили помилку у вашому коміт-повідомленні, або ви забули додати файл після того, як зробили коміт, ви можете легко виправити це за допомогою цієї команди.
|17.| `git revert x`, where x is the SHA of commit to revert| Reveres a previously made commit. Використовується для більш складних виправлень, які знаходяться **не в останньому коміті** (або якщо ви вже завантажили свої зміни через push). Це дасть змогу взяти всі зміни, які були у коміті, відмінити їх, і створити новий комміт. Коли ви повертаєтесь до старих комітів, майте на увазі, що виникає ризик отримати т.з. "конфлікти злиття". Це відбувається, коли файл змінюється через інший пізніший коміт, і тепер git не може знайти правильні рядки, до яких треба повернутися, так як їх там вже нема.
|18.| `git merge x`, where x is the name of the branch to be merged into the branch that's currently checked out| Combines two branches. When a merge happens, Git will: **(1)** look at the branches that it's going to merge, **(2)** look back along the branch's history to find a single commit that both branches have in their commit history, **(3)** combine the lines of code that were changed on the separate branches together, **(4)** make a commit to record the merge
|19.| `git branch backup`| With this command, for example before doing any resetting, you can create a reserve-branch on the most-recent commit so that u could get back to the commits if u had made a mistake
|20.| `git log --oneline --graph --all`| We can't see other branches in the git log output unless we switch to a branch. With this command, however, u can see all branches at once in the git log output. `--graph` tells Git to show the commit tree in the form of an ASCII graph layout
|21.| `git checkout -b x y`, where x is the name of the newly-created branch, y is the branch name (the most recent commit in that branch) or a commit's SHA which the newly-created brach will stem from| Creates a branch, switches to it, and, at the same time, makees this new branch to stem from a specific branch, all in one go
|22.| `git branch -D x`, where x is the name of the branch, and the flag MUST be CAPITALIZED| Git won't let you delete a branch if it has commits on it that aren't on any other branch. With this command, however, u force Git to delete the branch.
|23.| `git branch -d x`, where x is the name of the branch| Deletes a branch. **Things to note: _(1)_ you can't delete a branch that you're currently on, _(2)_ Git won't let you delete a branch if it has commits on it that aren't on any other branch (meaning the commits are unique to the branch that's about to be deleted)
|24.| `git checkout x`, where x is is the name of the brance| Switches between brances. It's important to understand how this command works. Running this command will: **(1)** remove all files and directories from the Working Directory that Git is tracking (files that Git tracks are stored in the repository, so nothing is lost), **(2)** go into the repository, and **(3)** pull out all of the files and directories of the commit that the branch points to
|25.| `git branch x`| Creates a branch called 'x' **and still points to the latest commit**
|26.| `git branch`|  Lists all branches
|27.| `git commit -m "x"`, where x is used as the commit message. Be aware that you can't provide a description for the commit, only the message part| If the commit message you're writing is short and you don't want to wait for your code editor to open up to type it out, you can pass your message directly on the command line with this command
|28.| `git tag -d x`, where x is the name of the tag| Deletes a tag
|29.| `git tag`| Displays all tags that are in the repository
|30.| `git tag -a x`, where x is the name of the tag. If you don't provide the flag, then it'll create what's called lightweight tag.| Creates an annotated tag to the most recent commit. Annotated tags are recommended because they include a lot of extra information such as: the person who made the tag, the date the tag was made, a message for the tag. Because of this, you should always use annotated tags.
||**Wildcards:**|
||- `**`| Matches nested directories. For example, `a/**/z` would match `a/z`, `a/b/z`, `a/b/c/z`
||- `[a-z]`| Match one occurrence of a character between a and z; alternatively, there could be [0-9], [4 and 89], u name it.
||- `[abc]`| Matches at least one character within the brackets; case-sensitive
||- `?`| Matches a single alphabet in a specific position
||- `samples/*.jpg`| Say u have 50 JPEG images in the "samples" folder. This line in the .gitignore file would tell Git to ignore all 50 images
||.gitignore| Tells Git about the files that Git should not track. This file should be placed in the same directory that the .git directory is in.
|31.| `git diff <sha 1> <sha 2>`| Compares any two commits you need
|32.| `git rm --cached x`, where x is the name of the file| Unstages a file if it has'n't been committed yet
|33.| `git add .` (in a regular way it would be used as `git add x x ... xN`, where x, xN are the names of the files| Moves all files (including all nested files and directories!) from the Working Directory to the Staging Index
|34.| `git config --global user.name "x"`, where x is Your-Full-Name| Sets the name that will be attached to your commits and tags
|35.| `git config --global user.email "x"`, where x is Your-Email| Sets the e-mail address that will be attached to your commits and tags
|36.| `git show x`, where x is first 7 chars of the commit's SHA:| Displays log of only one commit
|| - `--stat`| shows the how many files were changed and the number of lines that were added/removed
|| - `-p` or `--patch`| displays the actual changes that have been made to the commit, icluding; this the default, but if --stat is used, the patch won't display, so pass -p to add it again
|| - `-w`| ignores changes to whitespace
|37.| `git log -p` (or `--patch`)| Displays the *files* that have been modified, displays the *location of the lines* that have been added/removed, and displays the *actual changes* that have been made
|38.| `git log --stat`| Displays the *file(s)* that have been modified in the commit, displays the *number of lines* that have been added/removed in the commit, and displays a summary line with the *total number of modified files and lines* that have been added/removed in the commit
|39.| `git log [-n x]` (to leave Less text editor, use **q**)| List commit history of current branch. By default, this command displays: the SHA, the author, the date, and the message. `-n x` limits list to last N number of x commits.
|40.| `git status`| List which files are staged, unstaged, and untracked
|41.| `git clone [project url]` (optionally, u could add the folder name after the url, to clone the repository into that folder, e.g. use another name of the repository locally)| Downloads a project with the entire history from the remote repository.
|42.| `git init [project name]` | Create a new local repository. If `[project name]` is provided, Git will create a new directory name `[project name]` and will initialize a repository inside it. If `[project name]` is not provided, then a new repository is initialized in the current directory.
|43.| `git config --list`| Checks all the keys available in the Git config file
|44.| `git config --global core.editor "code --wait"`| Associates VS Code with Git
|45.| `git config --global merge.conflictstyle diff3`| Adds a `|||||||` marker and the original text before the `=======` marker. The default is "merge", which shows a `<<<<<<<` conflict marker, changes made by one side, a `=======` marker, changes made by the other side, and then a `>>>>>>` marker.
  </details>

  It seems like all the aforementioned commands are very basic and useful, so I'm gonna use all of them where needed.



- [x] Complete the Main: Introduction Sequence and Remote: Push & Pull -- Git Remotes

  Many commands weren't new for me since I had already learnt most of them in the Git course from Udacity. Nevertheless, all new commands I have included into the list above and to flashcards as well.

  Despite the fact that I somehow managed to solve the 8th task (Remote: Push & Pull -- Git Remotes), I couldn't understand it at first. However, having tried to solve the practical task of this section, Git basics, now I understand how to apply this knowlege (keep reading further to see what a beatiful pic I managed to create while trying to understand this topic).


- [x] Create repository named kottans-frontend

- [x] Create README.md for the repository

- [x] Describe your impressions about learned materials.

- [x] Send a pull-request to Kottans/mock-repo proposing a change.

  Here is what I understand from [the task given](https://github.com/kottans/frontend/blob/master/tasks/git-intro.md), i.e. what I understand at How to make a pull-request:

<details>
  <summary>Click to see the pic</summary>
  
![how to make a pull-request](https://clip2net.com/clip/m0/33c0a-clip-191kb.jpg?nocache=1)
</details>

## Extra Materials

- [x] [Git за 30 хвилин](https://codeguida.com/post/453)

  I have learned a few new git commands, namely:

  <details>
  <summary>Click to see the table</summary>

  |#|Command|Description
  |---|---|---
  |1.|`git remote add origin https://github.com/...`| Зв'язує наш локальний репозиторій з репозиторієм на GitHub і дає кличку origin останньому. Проект може мати безліч дистанційних репозиторіїв одночасно. Для того, щоб відрізнити їх один від одного ми даємо їм різні клички/назви. Традиційно основний дистанційний репозиторій в git називають *origin*.
  |2.|`git pull x y`| Отримує зміни з сервера. x - назва/кличка дистанційного репо, y - назва гілки цього репозиторію, яку ми хочемо отримати
  |3.| `git push x y`| Завантажує коміти на сервер. Приймає два параметри - назва/кличка дистанційного репо (у нашому випадку x) і гілка, на яку ми хочемо завантажити коміт (за замовчування для кожного репозиторія встановлена гілка master, але в нашому випадку y).
  |4.| `git difftool <sha 1> <sha 2>`| графічний клієнт, що показує всі відмінності між двома заданими комітами
  |5.| 'git checkout <sha>| Виявляється з допомогою цієї команди можна не тільки перемикатися між гілками, а щей й між комітами, тобто переміщуватсия в минуле :), а потім назад в майбутнє ))
  |6.| `git mergetool`| Більшість розробників вважають, що краще вирішувати дані конфлікти за допомогою GUI клієнту. Щоб запустити графічний клієнт використовують цю команду. Проте в статті нічого про те, як її конфігуруфвати
  
  </details>
  
- [x] [Git tips](http://sixrevisions.com/web-development/git-tips/) — consolidate your knowledge of Git

  This article is emptly :(

- [x] [About Merge Conflicts](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-merge-conflicts)

  I got that it's possible to resolve merge conflicts both using the conflict editor on GitHub and using the command line. With former option, however, you can resolve merge conflicts only between branches in your Git repository, and these conflicts are only about competinig line changes. All the other conflicts can be resolved with the latter option.

- [x] [Resoilving a Merge Conflict](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)

  I've learned a new git command: `git rm x`, where x is the name of the file to be removed from the repository.  This command comes in useful when resolving removed file merge conflicts.

- [x] [Communicating using Markdown](https://lab.github.com/githubtraining/communicating-using-markdown)

  I have created the 'MARKDOWN [GIT] set of flashcards on [memecode](https://www.memcode.com/users/1823) to better memorize Markdown syntax.

  Unfortunetely, the flashcards make me memorize the commands in the *command -> definition* manner. Now and then, I need to revise them in the *command <- definition* manner or just have a quick reference, which is why I've put the list of all the commands in the table below:

<details>
  <summary>Click to see the table</summary>
  
|#|Piece of Syntax|Description
|---|---|---:
|1.| `-` or `*`| Creates an unordered list
|2.| `- [ ] x`| Adds a checkbox
|3.| `- [x] x`| Adds a ticked checkbox
|4.| `[title](url)`| Creates a link (TIP: use the keyboard shortcut **command + k** to create a link
|5.| `# header 1` ... `###### header 6`| Header 1 is the largest, while header 6 is the smallest
|6.| `![title](url)`| Adds an image
|7.| `**x**`| Bold **x**
|8.| `*x*`| Italic *x*
|9.| `~~ABC~~`| Strikethrough x (закреслений)
|10.| `**aaa _aaa_ aaa**`| **aaa _aaa_ aaa**
|11.| `***aaa aaa aaa***`| ***aaa aaa aaa***
|12.|  `> x`| Adds quotation
|13.| `@perseon`, where *person* is a person's username or team name| Mentions a person or a team; autocomplete results are restricted to repository collaborators and any other participants on the thread
|14.| `@organisation/team` | Subscribes all members of the team to the conversation
|15.| `#`| Brings up a list of suggested issues and pull requests within the repository
|16.| `:`| Brings up a list of suggested emoji ([emoji-cheat-sheet.com](https://www.webfx.com/tools/emoji-cheat-sheet/))
|17.| `---`| Creates each column's header of a table. **At least 3 hyphens must be used**
|18.| `\|`| Separates each column of the table
|19.| `:---`, `:---:`, `---:`| Aligns text to the left, center, and to the right, respectively
|20.| `\```xxx *code* ```/`| Adds an optional language identifier to enable syntax highlighting in your fenced code block. Use `HTML`, `CSS`, or `JavaScript` instead of `xxx`. Other identifiers for more languages you can find [here](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml). Don't pay your attention to the `\/`, they are not needed in the real syntax.
|21.| `<details><summary>message</summary> content</details>`| Adds a collapsible section containing sth. NB: Make sure you have an empty line after the closing `</summary>` tag, otherwise the markdown/code blocks won't show correctly. NB: Make sure you have an empty line after the closing `</details>` tag if you have multiple collapsible sections.
</details>

  I also have learned how to make saved replies and gists.

- [x] [Learn anything front-end](https://learn-anything.xyz/web-development/front-end)

  I can see that this is a beautiful resource – I've added it to my bookmarks.

- [x] [TypingClub](https://www.typingclub.com/) — improve your typing speed

  I had had this skill at this popint.

- [x] [Как учиться и справляться с негативными мыслями](https://guides.hexlet.io/learning/)

  I have started writing this README.md to track my progress making notes of my troubles and successes. It's my diary now so to speak :)



_________________________________________________________________________

## Stage 1. The Show Must Go On

Main part of the _Front-End Course_.

### Lectures & Workshops

#### HTML, CSS & DOM

- [ ] W3C and WHATWG Standards. HTML markup. Intro to CSS. Grids.
- [ ] Graphics on the web. А11Y & forms. Content handling
- [ ] DOM and Layout Trees
- [ ] Cookies, document.cookie

#### JavaScript

- [ ] Scopes & Closures
- [ ] Concept of this
- [ ] Prototypes
- [ ] Types & Grammar
- [ ] Callbacks & Promises
- [ ] Async & Await
- [ ] ESNext Api / Generators
- [ ] Functionality
- [ ] How browser works/Web workers


#### Frontend Framework

#### TypeScript

#### Soft Skills


