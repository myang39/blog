---
layout: post
title:  "Python Virtual Environment"
date:   2019-01-20
categories: jekyll update
author: "Luke"
---

A quick look up for python virtual environment table

Install virtualenv:
```
$pip install virtualenv
```

List all the packages in the current env:
```
$pip list
```

Make a directory:
```
$mkdir Environments
```

Make the virtual environment:
```
$virtualenv project1_env 
```

Activate the new python environment:
```
$source project1_env/bin/activate
```

Now we are inside our new virtual environment, we could check that
by the prompt of the terminal. We can also check it by

```$which python```, or ```$which python3```, or ```$which pip```


Now ```$pip list``` will only show the packages installed in this
virtual env, and ```$pip install numpy``` would only install the
```numpy``` package in the current environment.

Export all the packages in the current virtual env so I might want to
use the same set up for another virtual env:
```
$pip freeze --local > requiremets.txt
```

Notice: you could also use your global side packages within a virtual
python env. The command would only take the local (virtual env) dependencies
that you had in your virtual python env and put them into requirements.txt

Get out of the python virtual environment:
```$deactivate```

Delete the virtual env:
```$rm -rf project1_env```

Make a virtual python env with a specific python version(e.g.3 ):
```$virtualenv -p /usr/bin/python3 py3_env```
the Path after the ```-p``` flag may vary

Activate the env:
```$source py3_env/bin/activate```

Install all the dependencies from requirement.txt:
```$pip install -r requirements.txt```


Thanks to https://www.youtube.com/watch?v=N5vscPTWKOk












