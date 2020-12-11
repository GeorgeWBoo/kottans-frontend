# Front-End Course from Kottans. Michael's endeavor :)

## Stage 0. Self-Study

### General
- [ ] 0. [Git Basics](https://github.com/kottans/frontend/blob/master/tasks/git-intro.md)
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

Unfortunetely, the flashcards make me memorizie the commands in the *command -> definition* manner. Now and then, I need to revise them in the *command <- definition* manner, which is why I've put the list of all the commands but without definitions right below:

|#|Git command|Explanation
|---|:---|---
|1.| `git pull --rebase` |Ensures that changes made to the local repo are put on top of the changes made in the remote (коротка форма для `git fetch` а потім `git rebase`)
|2.| `git push`|Uploads local repository content to a remote repository
|3.| `git pull`|Fetches and downloads content from a remote repository and immediately updates the local repository to match that content (*просто коротша форма для `git fetch` а потім `git merge`*)
|4.| `git fetch`|
|5.| `git rebase x`|
|6.| `git reset --hard HEAD^`|
|7.| `git reset HEADx`|
|8.| `git reset --soft HEAD^`|
|9.| `git reset --mixed HEAD^`|
|10.| `git reflog`|
|11.| `git show HEAD^^^2` or `HEAD~2^2`|
|12.| `git show HEAD^^` or `HEAD~2`|
|13.| `git show HEAD^^^` or `HEAD~3`|
|14.| `git show SHA^2`, where SHA is the SHA of a merge commit|
|15.| `git show HEAD^` or `HEAD~` or `HEAD~1`|
|16.| `git revert x`, where x is the SHA of commit to revert|
|17.| `git commit --amend`|
|18.| `git merge x`, where x is the name of the branch to be merged into the branch that's currently checked out|
|19.| `git reset --hard HEAD^`|
|20.| `git log --oneline --graph --all`|
|21.| `git checkout -b x y`, where x is the name of the newly-created branch, y is the branch name (the most recent commit in that branch) or a commit's SHA which the newly-created brach will stem from|
|22.| `git branch -D x`, where x is the name of the branch, and the flag MUST be CAPITALIZED|
|23.| `git branch -d x`, where x is the name of the branch|
|24.| `git checkout x`, where x is is the name of the brance|
|25.| `git branch x`|
|26.| `git branch`|
|27.| `git commit -m "x"`, where x is used as the commit message. Be aware that you can't provide a description for the commit, only the message part|
|28.| `git tag -d x`, where x is the name of the tag|
|29.| `git tag`|
|30.| `git tag -a x`, where x is the name of the tag. If you don't provide the flag, then it'll create what's called lightweight tag.|
||**Wildcards:**|
||- `**`|
||- `[a-z]`|
||- `[abc]`|
||- `?`|
||- `samples/*.jpg`|
||.gitignore|
|31.| `git diff`|
|32.| `git rm --cached x`, where x is the name of the file|
|33.| `git add .` (in a regular way it would be used as `git add x x ... xN`, where x, xN are the names of the files|
|34.| `git config --global user.name "x"`, where x is Your-Full-Name|
|35.| `git config --global user.email "x"`, where x is Your-Email|
|36.| `git show x`, where x is first 7 chars of the commit's SHA:|
|| - `--stat`|
|| - `-p` or `--patch`|
|| - `-w`|
|37.| `git log -p` (or `--patch`)|
|38.| `git log --stat`|
|39.| `git log` (to leave Less text editor, use **q**)|
|40.| `git status`|
|41.| `git clone https://...` (optionally, u could add the folder name after the url, to clone the repository into that folder, e.g. use another name of the repository locally)|
|42.| `git init`|
|43.| `git config --list`|
|44.| `git config --global core.editor "code --wait"`|
|45.| `git config --global merge.conflictstyle diff3`|

It seems like all the aforementioned commands are very basic and useful, so I'm gonna use all of them where needed.



- [x] Complete the Main: Introduction Sequence and Remote: Push & Pull -- Git Remotes

Many commands weren't new for me since I had already learnt most of them in the Git course from Udacity. Nevertheless, all new commands I have included into the list above and to flashcards as well.

Despite the fact that I somehow managed to solve the 8th task (Remote: Push & Pull -- Git Remotes), I couldn't understand it at first. However, having tried to solve the practical task of this section, Git basics, now I understand how to apply this knowlege (keep reading further to see what a beatiful pic I managed to create while trying to understand this topic).


- [x] Create repository named kottans-frontend

- [x] Create README.md for the repository

- [x] Describe your impressions about learned materials.

- [ ] Send a pull-request to Kottans/mock-repo proposing a change.

Here is what I understand from [the task given](https://github.com/kottans/frontend/blob/master/tasks/git-intro.md), i.e. what I understand at How to make a pull-request:

![how to make a pull-request](https://clip2net.com/clip/m0/33c0a-clip-191kb.jpg?nocache=1)

## Extra Materials

- [ ] [Git за 30 хвилин](https://codeguida.com/post/453)

- [x] [Git tips](http://sixrevisions.com/web-development/git-tips/) — consolidate your knowledge of Git

This article is emptly :(

- [ ] [About Merge Conflicts](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-merge-conflicts)

- [ ] [Resoilving a Merge Conflict](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line)

- [ ] [Communicating using Markdown](https://lab.github.com/githubtraining/communicating-using-markdown)

I have created the 'MARKDOWN [GIT] set of flashcards on [memecode](https://www.memcode.com/users/1823) to better memorize Markdown syntax.

Unfortunetely, the flashcards make me memorizie the commands in the *command -> definition* manner. Now and then, I need to revise them in the *command <- definition* manner, which is why I've put the list of all the commands but without definitions right below:

|#|Piece of Syntax|Description
|---|---|---:
|1.| `-` or `*`| Creates an unordered list
|2.| `- [ ] x`| - [ ] x
|3.| `- [x] x`| - [x] x
|4.| `[title](url)`| Creates a link (TIP: use the keyboard shortcut **command + k** to create a link
|5.| `# header 1` ... `###### header 6`| Header 1 is the largest, while header 6 is the smallest
|6.| `![title](url)`| Adds an image
|7.| `**x**`| Bold **x**
|8.| `*x*`| Italic *x*
|9.| `~~ABC~~`| Strikethrough x (закреслений)
|10.| `**aaa _aaa_ aaa**`| **aaa _aaa_ aaa**
|11.| `***aaa aaa aaa***`| ***aaa aaa aaa***
|12.|  `> x`| > x
|13.| `@perseon`, where *person* is a person's username or team name| Mentions a person or a team; autocomplete results are restricted to repository collaborators and any other participants on the thread
|14.| `@organisation/team` | Subscribes all members of the team to the conversation
|15.| `#`| Brings up a list of suggested issues and pull requests within the repository
|16.| `:`| Brings up a list of suggested emoji ([emoji-cheat-sheet.com](https://www.webfx.com/tools/emoji-cheat-sheet/))
|17.| `---`| Creates each column's header of a table. **At least 3 hyphens must be used**
|18.| `\|`| Separates each column of the table
|19.| `:---`, `:---:`, `---:`| Aligns text to the left, center, and to the right, respectively
|20.| `\```xxx *code* ```/`| Adds an optional language identifier to enable syntax highlighting in your fenced code block. Use `HTML`, `CSS`, or `JavaScript` instead of `xxx`. Other identifiers for more languages you can find [here](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml). Don't pay your attention to the `\/`, they are not needed in the real syntax.


- [x] [Learn anything front-end](https://learn-anything.xyz/web-development/front-end) – I can see that this is a beautiful resource – I've added it to my bookmarks.

- [x] [TypingClub](https://www.typingclub.com/) — improve your typing speed – I had had this skill at this popint.

- [x] [Как учиться и справляться с негативными мыслями](https://guides.hexlet.io/learning/) – I have started writing this README.md to track my progress making notes of my troubles and successes. It's my diary now so to speak :)



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


