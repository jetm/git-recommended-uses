class: center, middle

# Git Recommended Uses

Practices to get comfortable using and learning Git

Javier Tiá / August 26, 2015

---

# Who am I to talk about Git?

* Using Git professionally since 2011.

* Developed tools around Git: repo tool, WSSW Git Hooks and various little
utilities.

* Migrated severals projects to Git from Clearcase, CVS and Subversion.

* Solved hundreds of issues helping people using Git. Today I still do it, but
 no hundreds 😊.

---

# Expectations

* I expect from this presentation you can take some knowledge and apply it to
your frequent Git routine.

???

Just one expectation.

---

# Why 'Git Recommended Uses' presentation?

1. People struggle while are learning Git.

2. Git is a powerful tool, but it has some hard hills to climb.

3. At the beginning poor documentation and severals ways to get same result.

4. Git is not Subversion.

???

1. By experience I have seen many smart people struggle while are learning Git.
Some people compare Git with Hitler.

2. When are too many options, usually you get confused.

3. With each Git release the documentation is getting better, but still are the
options to get same result..

4. Git redefined how to use a Control Version software and the world was used
to Centralized approach. It's not Subversion, but it can be used similar.

---

# Little Git History

* Created in 2005 by Linus Torvalds and maintained today by Junio Hamano.

* Meaning 'git' as word: unpleasant person.

* Git arrived as a necessity.

???

* Created 10 years ago, patches and many contributors and thousands contributions.

* Torvalds said: "I'm an egotistical bastard, and I name all my projects after
myself. First 'Linux', now 'git'."

* After close accesses of Linux kernel developers to BitKeeper (SCM). Torvalds
released the first Git version and the world of Control Version software
started to change.

---

# Why Git and no another SCM

.center[![Centered image](images/git-job-trends-indeed.com.png)]

???

* Git won SCM war.

* When Torvalds designed Git, he already has experience with BitKeeper in the big
Linux Kernel code base. He studied all defects of CVS, Subversion, Darcs,
Baazar, Monotone and others.

* Be distributed, simple designed, making quickly and clean merges, all together
was a big deal on that time.

---

# How to self-study Git?

* Mindset: Think Git as you are exploring a tree.

* Get started with:

  * http://try.github.io/

  * http://gitimmersion.com/

* Complement always with:

  * `git help <COMMAND>` || `git help --all` || `git help --guides`

  * Making questions with a Web searcher.

  * Practice in a terminal.

???

Problem to solve:

> How to learn Git by your self?

Show hints commands to probe Git is a Tree

With Internet: show the training sites

Show how it works all `git help` commands.

Make an example how to practice in terminal.

DEMO

---

# Use latest stable Git version

> ### $ sudo add-apt-repository ppa:git-core/ppa
> ### $ sudo apt-get update
> ### $ sudo apt-get install git

???

Assuming Ubuntu default Distribution.

Problem to solve:

> Ubuntu has a Git version is not updated frequently.

Normally, people has fears to update software due to avoid a 'possible'
breakdown system. Others are just lazy people. Git code has a strong Test Suite
with thousands test cases.

In all these years using Git, I have never lost information for update to the
latest stable Git version.

DEMO

---

# Get a better CLI prompt

![Default-aligned image](images/jetm-terminal.png)

https://github.com/nojhan/liquidprompt

???

Problem to solve:

> Know where are you while you're using Git in CLI

DEMO

---

# Identify yourself

<br />

> ### $ git config --global user.name "__YOUR NAME__"

> ### $ git config --global user.email "__YOUR EMAIL ADDRESS__"

???

Problem to solve:

> Identify your commits with a proper authorship

Remember now you are an author.

---

# Increase Git usability by leveraging *.gitconfig*

> ### * Set per repository or global options.

> ### * `git config` to Get, Set and Unset options.

> ### * Don't forget look for more detail: `git help config`.

???

Problem to solve:

> Teach how to take advantage of .gitconfig file

Show how to Get, Set and Unset Git options.

---

# Common Git aliases

> #### $ git config --global alias.br branch
> #### $ git config --global alias.ci commit
> #### $ git config --global alias.co checkout
> #### $ git config --global alias.st status
> #### $ git config --global alias.ls ls-files
> #### $ git config --global alias.rb rebase
> #### $ git config --global alias.mg merge

???

Problem to solve:

> Reduce keystrokes

Where you're using Git, you will type commands more than you could imagine.

If you're looking yourself typing a command more than two times, you should
thinking to create an alias.

---

# How to write a commit message

Structure of a commit message:

> Subject line<br/>
> _BLANK LINE_<br/>
> Body message

Rules:

1. Write subject line thinking: What am I doing?
2. Use imperative mood in subject line: no -ing, -ed.
3. Do not end subject line with a period.
4. Limit subject line between 50 to 70 characters.
5. Insert a blank line between subject line and body message.
6. Write body message thinking: Why am I doing it? vs How am I doing it?
7. Limit body message to 72 characters.

???

Problem to solve:

> People write commit messages without care about it.

If you find yourself struggling and thinking too much about your commit, it
could be is too long all changes. Make it shorter.

If it's too much rules, consider a good editor as helper, e.g.: Vim.

DEMO

---

# Use Interactive mode to commit

> > ### $ git add --patch

* It gives the user a chance to review the changes before commit them.

* Help you to write the commit.

???

Problem to solve:

> People gets confuse about how to commit changes

Interactively choose hunks between the index and the work tree and add them to
the index.

DEMO

---

# Merge vs Rebase

* One of most controversial Git discussions, just search: Merge vs Rebase.

* Know when use _merge_ or _rebase_ add significant added value. It produces a
clean and semantically correct history graph.

Rules:

1. Work always with topic or temporal branch, avoid work over master or
feature branch.

2. Use `git merge` when incorporating an entire feature set into another branch,
use `git rebase` for rest of cases.

3. Golden rule: Never use `git rebase` over published changes, only over new
and no pushed changes.

???

Problem to solve:

> Extended confusion about when to use `git merge` or `git rebase`.

Clarify rebase concept. Show it in next slide.

DEMO

---

# Rebase concept

.center[![Centered image](images/git-rebase.gif)]

---

# Keep a clean and correct Git history

Always rebase your local commits and preserve all merges:

> ### $ git config --global pull.rebase preserve

> _Require Git v1.8.5+_

<br />

Only allow fast-forward merges:

> ### $ git config --global merge.ff only

???

Problem to solve:

> How to keep a clean and correct Git history.

Clarify fast-forward merges.

DEMO

---

# References

* This presentation: https://github.com/jetm/git-recommended-uses

# Contact information

* javier.tia@gmail.com / javier.tia@hp.com

---

class: center, middle

# Questions?

