---
layout: post
title:  "python flask study notes"
date:   2019-01-12
categories: jekyll update
author: "Luke"
---


Today I started to learn python flask

网上有不少python flask的教程啦 我就是记录记录我学了啥

I followed along with this youtube https://www.youtube.com/watch?v=MwZwr5Tvyxo&list=PL-osiE80TeTs4UjLw5MM6OjgkjFeUxCYH

lesson1: basic setup

In order to make the localhost reflexing what's new in the code,
instead of ctl+c and then flask run. There are two ways to automate
it (to run the app in debug mode):

1. set up a environemnt varibale:
just type in the terminal export FLASK_DEBUG=1 (notice! no space around the equal sign, otherwise bash is gonna complain with "bad assignment")

2. add this to the the app.py file (currently it's the only file in my folder)

```
if __name__ == '__main__':
    app.run(debug=True)
```

and the final code look like this:

```
from flask import Flask

app = Flask(__name__)


@app.route('/')
@app.route('/home')
def hello_world():
    return '<h1>Home Page</h1>'


@app.route("/about")
def about():
    return "<h1>about</h1>"


if __name__ == '__main__':
    app.run(debug=True)

```

The reason behind it is that the condition(`__name__ == '__main__'`) is only true
if we run this script directly.

The `@app.route('/home')` is called decorator. It basically handle all of the complicated
stuff and allows us to write a function that returns the information that will be shown on
our website for this specific route(`/home`)
