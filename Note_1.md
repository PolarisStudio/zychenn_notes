This is the report dedicated on organizing all the codes I learn on the national holiday, which covers *Markdown*, *Git* and *Flask*.

# Markdown

## Basic syntax

The basic syntax are collected by myself [here](https://github.com/paradoxXD/paradoxical/blob/master/basic_markdown.md "the example deployed on github").  [This](https://github.com/paradoxXD/paradoxical/blob/master/basic_markdown.pdf) is the rendered pdf version.

The document is a aggregation for the basic syntax of markdown, retrieved from [Official website](https://www.markdownguide.org/basic-syntax/).

The Latex equation part is collected from [here](https://www.zybuluo.com/codeep/note/163962#mjx-eqn-eqsample "other people's notes") and [here](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference "https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference").

---

## Marp

***Marp for VS Code*** is a VSC extension that is useful to convert Markdown to basic PowerPoint.

[This](https://github.com/paradoxXD/paradoxical/blob/master/marp_usage.md "the source code") is a trial, and [this](https://github.com/paradoxXD/paradoxical/blob/master/marp_usage.pdf "the pdf version") is the output.

To get more information, please visit [official website](https://marpit.marp.app/markdown).

---

## Typora

***Typora*** is a program that elevates the markdown writing experience, which is what I'm using now. I also use Typora to render different output, such as pdf file. The compatibility is superb!

Please visit [Typora](https://www.typora.io/) for more information.

# Git

The basic git usage can be found [official maunal book](https://git-scm.com/docs) and [Liao Xuefeng's tutorial](https://www.liaoxuefeng.com/wiki/896043488029600), and I use GitHub Desktop as my Git GUI, which is more convenient, you can find it [here](https://desktop.github.com/).

I'm not intended to reiterate the tutorial, so I'll just skip this part. If encounter any issue, I will refer to the tutorial.

# Flask

Flask is a segment of a greater project called Pallets.

Flask is a a flexible and popular web development framework.

The following tutorial is collected from [https://flask.palletsprojects.com/en/1.1.x/quickstart/](https://flask.palletsprojects.com/en/1.1.x/quickstart/).

***<u>Highly recommend</u> Harvard CS50, you can watch it via [Havard CS50](https://www.youtube.com/watch?v=zdgYw-3tzfI)***  :smile:

## Installation

### Dependencies

>[Werkzeug](https://palletsprojects.com/p/werkzeug/) implements WSGI, the standard Python interface between applications and servers.
>
>[Jinja](https://palletsprojects.com/p/jinja/) is a template language that renders the pages your application serves.
>
>[MarkupSafe](https://palletsprojects.com/p/markupsafe/) comes with Jinja. It escapes untrusted input when rendering templates to avoid injection attacks.
>
>[ItsDangerous](https://palletsprojects.com/p/itsdangerous/) securely signs data to ensure its integrity. This is used to protect Flask’s session cookie.
>
>[Click](https://palletsprojects.com/p/click/) is a framework for writing command line applications. It provides the `flask` command and allows adding custom management commands.

### Optional Dependencies

> [Blinker](https://pythonhosted.org/blinker/) provides support for [Signals](https://flask.palletsprojects.com/en/1.1.x/signals/#signals).
>
> [SimpleJSON](https://simplejson.readthedocs.io/) is a fast JSON implementation that is compatible with Python’s `json` module. It is preferred for JSON operations if it is installed.
>
> [python-dotenv](https://github.com/theskumar/python-dotenv#readme) enables support for [Environment Variables From dotenv](https://flask.palletsprojects.com/en/1.1.x/cli/#dotenv) when running `flask` commands.
>
> [Watchdog](https://pythonhosted.org/watchdog/) provides a faster, more efficient reloader for the development server.

### Virtual environment

```
py -3 -m venv venv
```

```
venv\Scripts\activate
```

```
pip install Flask
```

**.gitignore**

```
venv/
*.pyc
__pycache__/
instance/
.cache/
.pytest_cache/
.coverage
htmlcov/
dist/
build/
*.egg-info/
.idea/
*.swp
*~
```

**Hello.py**

```python
from flask import Flask

app = Flask(__name__) # this is an object, a web aplication


@app.route('/') # direct to root directory
def hello():
    return 'Hello, World!' # return a string
```

Actually, in order to understand the code in Flask, we need to know briefly about HTML, CSS, JS.

[W3school](https://www.w3schools.com/html/default.asp) is a very good reference to learn those basic concepts.

 