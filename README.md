vishgit & Smellinux
===============

A text-first discipline for computer literacy

Overview
---------------

vishgit is a deliberately small, text-centered practice built around three timeless tools:

vim — for editing all text

sh — specifically a POSIX-lean shell (dash / Almquist shell) for execution

git — for memory, sharing, collaboration, and publication
Rather than treating these as separate utilities, vishgit treats them as one integrated discipline:

- Edit with vim.
- Execute with sh.
- Remember with git.

The goal is not convenience or abstraction, but fluency—developed through repetition until these tools live in muscle memory and thought flows naturally from text to execution to versioned history.


What is Smellinux?
------------------------------

Smellinux stands for “A Small Environment for Learning Linux.”

It is not a distribution in the traditional sense. Instead, Smellinux is a portable userspace, created by running a shell script in a host terminal that launches a customized Alpine Minirootfs. 

This Alpine-based userspace becomes the learning environment in which all vishgit work happens.

Key characteristics:

- Minimal and distraction-free
- Text-first by design
- Reproducible across machines
- Focused on fundamentals rather than tooling sprawl

Smellinux can run anywhere a terminal exists, making it suitable for low-resource devices, shared machines, or constrained environments.


The Shell Standard
‐-----------------------------

All executable scripts in Smellinux begin with: (Sh)
#!/bin/sh

This is intentional.

In practice, /bin/sh resolves to dash (Debian Almquist Shell) or another Almquist-derived POSIX shell. 

This enforces a portable, standards-based shell language and avoids shell-specific extensions.

The result:

- Scripts that run the same almost everywhere
- A clear mental model of what “sh” actually is
- A strong foundation for understanding UNIX systems
- vim as the Universal Interface

In vishgit, everything is text:

- Shell scripts
- CSV databases
- Journal entries
- Notes and essays
- Documentation

All of it is created and maintained in vim.

This is not about preference—it is about unification. One editor. One set of motions. One mental model. Over time, editing becomes instinctive rather than cognitive.


git as Memory and Fellowship
------------------------------------------------

git is not treated merely as version control.

It is used as:

- A personal memory system
- A collaboration mechanism
- A publishing pipeline
- A historical record of thought and practice

Writing, data, and scripts all evolve together. Learning is visible. Changes are traceable. Sharing is native.


The KJV CSV Dataset
-‐---------------------------------

At the heart of Smellinux is a git pull of a public-domain King James Version Bible, structured as a simple CSV database (Meta-V).

This choice is both practical and historical:

- The KJV is public domain
- It is rich, structured text
- It invites reading, writing, querying, and transformation

Historically, English literacy was built around reading and writing the Bible—memorizing, annotating, preaching, and applying text. Smellinux revives this tradition, but reframes it through modern computing literacy:

- Text processing
- Shell scripting
- Data manipulation
- Versioned study and annotation

English literacy and computer literacy begin together.

A Practice, Not a Platform
vishgit is not a course, framework, or product.

It is a practice.

Through repetition:

- Editing becomes natural
- Scripting becomes conversational
- The shell becomes expressive
- Versioning becomes instinctive

The aim is flow, not speed. 

Depth, not breadth.


Why “Small”?
---------------------

Smellinux is intentionally small because:

- Fewer tools force understanding
- Constraints sharpen thinking
- Text reveals structure
- Simplicity invites mastery

This project moves in the opposite direction of GUI-heavy, abstracted “learn to code” platforms. It returns to the UNIX tradition: plain text, simple tools, composed together.


Summary
---------------

vishgit + Smellinux is:

- A minimalist Linux learning environment
- A text-first approach to computing
- A revival of literacy through reading and writing
- A disciplined integration of vim, sh, and git
- A path toward fluency through repetition

Small tools. Deep practice. Lasting skills.


