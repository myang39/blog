---
layout: post
title:  "Mac - Add to Path and Add Environment Variable"
date:   2019-01-18
categories: jekyll update
author: "Luke"
---

### "Add the bin directory to your path"

This sentence scares people away ... It's true that
there are several stackOverflow posts tells you what to do.
But still it's not clear especially for people who lives
in the world of IDE.

So what does 'Add the bin directory to your path' ?
The 'path' here is actually the environment variable that
lives in your terminal. You can check its current value
by 
```$echo $PATH``` the ```$``` before the ```PATH``` indicates
its a variable.
The output is gonna looks like this: ```$/home/jacob/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games```
which is quite confusing to people who looks at it for the first time.

The output is actually just directory locations that the terminal would be
looking at when it trys to find the the command software (Yes! Commands like ls, rm, mv are all pieces of
software living inside some folders) you typed in the terminal. These
directory locations are __separated by colon__.

So if you want your software to be accessible to the terminal (which is
also a piece of software), you need to tell it by add the folder's that
contains your software (usually it's called bin (short for binary) when you download some
package from the internet) __to the PATH__. You can do that
by add a line like
```export PATH=${PATH}:the/directory/location/you/want/to/add```
or ```export PATH=the/directory/location/you/want/to/add:${PATH}```
to the ~/.bash_profile ot ~/.bashrc or ~/.zshrc (if you use zsh)

what the line above does is it append or prepend the directory location
you want to add to the old PATH (all other directory locations that alreay
in the PATH)

Now in order for the newly updated PATH to take effect. You could
either ```$source ~/.zshrc``` (assume you add the line in ~/.zsh,
if you add the line in ~/.bashrc, ```$source ~/.bashrc``` instead)
, or you could fully close (quit) the terminal and restart the terminal.


### Add Environment Variable

So PATH is a environment variable which the terminal uses to find
pieces of command software.

 

