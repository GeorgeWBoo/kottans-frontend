# kottans-frontend

# Front-End Course. Contents

## Stage 0. Self-Study

### General
- [ ] [Git Basics](https://github.com/kottans/frontend/blob/master/tasks/git-intro.md)
- [ ] [Linux CLI and Networking](https://github.com/kottans/frontend/blob/master/tasks/linux-cli-http.md)
- [ ] [VCS (hello gitty), GitHub and Collaboration](https://github.com/kottans/frontend/blob/master/tasks/git-collaboration.md)

### Front-End Basics
- [ ] [Intro to HTML & CSS](https://github.com/kottans/frontend/blob/master/tasks/html-css-intro.md)
- [ ] [Responsive Web Design](https://github.com/kottans/frontend/blob/master/tasks/html-css-responsive.md)
- [ ] [HTML & CSS Practice](https://github.com/kottans/frontend/blob/master/tasks/html-css-popup.md)
- [ ] [JavaScript Basics](https://github.com/kottans/frontend/blob/master/tasks/js-basics.md)
- [ ] [Document Object Model](https://github.com/kottans/frontend/blob/master/tasks/js-dom.md) - practice

### Advanced Topics
- [ ] [Building a Tiny JS World (pre-OOP)](https://github.com/kottans/frontend/blob/master/tasks/js-pre-oop.md) - practice
- [ ] [Object oriented JS](https://github.com/kottans/frontend/blob/master/tasks/js-oop.md) - practice
- [ ] [OOP exercise](https://github.com/kottans/frontend/blob/master/tasks/js-post-oop.md) - practice
- [ ] [Offline Web Applications](https://github.com/kottans/frontend/blob/master/tasks/app-design-offline.md)
- [ ] [Memory pair game](https://github.com/kottans/frontend/blob/master/tasks/memory-pair-game.md) — real project!
- [ ] [Website Performance Optimization](https://github.com/kottans/frontend/blob/master/tasks/app-design-performance.md)
- [ ] [Friends App](https://github.com/kottans/frontend/blob/master/tasks/friends-app.md) - real project!
________________________________________________


## 0. Git Basics

- [x] Finish the course [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)

I have created the 'Version Control with Git [Udacity] set of flashcards on [memecode](https://www.memcode.com/users/1823) to better memorize all of these GIT commands.

Unfortunetely, the flashcards make me memorizie the commands in the *command -> definition* manner. Now and then, I need to revise them in the *command <- definition* manner, which is why I've put the list of all the commands but without definitions right below:

- `git pull --rebase`
- `git push`
- `git pull`
- `git fetch`
- `git rebase x`
- `git reset --hard HEAD^`
- `git reset HEADx`
- `git reset --soft HEAD^`
- `git reset --mixed HEAD^`
- `git reflog`
- `git show HEAD^^^2` or `HEAD~2^2`
- `git show HEAD^^` or `HEAD~2`
- `git show HEAD^^^` or `HEAD~3`
- `git show SHA^2`, where SHA is the SHA of a merge commit
- `git show HEAD^` or `HEAD~` or `HEAD~1`
- `git revert x`, where x is the SHA of commit to revert
- `git commit --amend`
- `git merge x`, where x is the name of the branch to be merged into the branch that's currently checked out
- `git reset --hard HEAD^`
- `git log --oneline --graph --all`
- `git checkout -b x y`, where x is the name of the newly-created branch, y is the branch name (the most recent commit in that branch) or a commit's SHA which the newly-created brach will stem from
- `git branch -D x`, where x is the name of the branch, and the flag MUST be CAPITALIZED
- `git branch -d x`, where x is the name of the branch
- `git checkout x`, where x is is the name of the brance
- `git branch x`
- `git branch`
- `git commit -m "x"`, where x is used as the commit message. Be aware that you can't provide a description for the commit, only the message part
- `git tag -d x`, where x is the name of the tag
- `git tag`
- `git tag -a x`, where x is the name of the tag. If you don't provide the flag, then it'll create what's called lightweight tag.

Wildcars:
- `**`
- `[a-z]`
- `[abc]`
- `?`
- `samples/*.jpg`

.gitignore

- `git diff`
- `git rm --cached x`, where x is the name of the file
- `git add .` (in a regular way it would be used as `git add x x ... xN`, where x, xN are the names of the files
- `git config --global user.name "x"`, where x is Your-Full-Name
- `git config --global user.email "x"`, where x is Your-Email
- `git show x`, where x is first 7 chars of the commit's SHA:
  - `--stat`
  - `-p` or `--patch`
  - `-w`
- `git log -p` (or `--patch`)
- `git log --stat`
- `git log` (to leave Less text editor, use **q**)
- `git status`
- `git clone https://...` (optionally, u could add the folder name after the url, to clone the repository into that folder, e.g. use another name of the repository locally)
- `git init`
- `git config --list`
- `git config --global core.editor "code --wait"`
- `git config --global merge.conflictstyle diff3`

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

- `-`

- `- [ ] x`

- `- [x] x`

- `[title](url)`

- `# header 1` ... `###### header 6`

- `![title](url)`

- `**x**`

- `*x*`

- `~~ABC~~`

- `**aaa _aaa_ aaa**`

- `***aaa aaa aaa***`

- `> x`



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


