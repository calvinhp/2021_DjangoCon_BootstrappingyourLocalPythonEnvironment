---
title-prefix: Six Feet Up
pagetitle: Bootstrapping your Local Python Environment
author: Calvin Hendryx-Parker, CTO, Six Feet Up
author-meta:
    - Calvin Hendryx-Parker
date: IndyPy ChiPy 2021
date-meta: 2021
keywords:
    - Python
    - Programming
    - Code
---

# Bootstrapping your Local Python Environment {data-background-image="images/david-clode-d0CasEMHDQs-unsplash.jpg"}
#### Calvin Hendryx-Parker, CTO
#### Six Feet Up

:::{.credits}
Photo by <a href="https://unsplash.com/@davidclode?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">David Clode</a> on <a href="https://unsplash.com/s/photos/python?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
:::

# Let's set our intention {data-background-image="images/sean-stratton-ObpCE_X3j6U-unsplash.jpg"}
~~~ {.stretch .shell}
$ python -m this

The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
~~~

:::{.credits}
Photo by <a href="https://unsplash.com/@seanstratton?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Sean Stratton</a> on <a href="https://unsplash.com/s/photos/zen?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
:::

# {data-background-image="https://imgs.xkcd.com/comics/python_environment.png"}

![](https://imgs.xkcd.com/comics/python_environment.png)

<https://xkcd.com/1987/>

::: notes

April 2018 Randall Munroe posted this comic and admitted he did some bad things to get to this point.

The Python environmental protection agency wants to seal it in a cement chamber, with pictorial messages to future civilizations warning them about the danger of using `sudo` to install random Python packages.

:::

# Python lives in many places {data-background-image="images/5450163349_7d5d45befb_o.jpg"}

* Python provided by OS (macOS, RedHat, Ubuntu)
* Python installed from an App Store (Microsoft Store)
* Python installed from [python.org](https://python.org) installer
* Python installed from a Package Manager (apt, [brew](https://brew.sh), [chocolatey](https://chocolatey.org/))
* Python installed by a Python Distribution ([ActiveState](https://www.activestate.com/products/python/), [Anaconda](https://www.anaconda.com/products/individual))

::: notes
Photo Credit: <https://flic.kr/p/9iBvFB>
:::

# So why should you care about all of this? {.r-fit-text data-background-image="images/fermin-rodriguez-penelas-LcJkpSoA0es-unsplash.jpg"}

:::{.credits}
Photo by <a href="https://unsplash.com/@ferminrp?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Fermin Rodriguez Penelas</a> on <a href="https://unsplash.com/s/photos/thinking-dog?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
:::

# Stay Zen {.r-fit-text data-background-image="images/sean-stratton-ObpCE_X3j6U-unsplash.jpg"}

~~~
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
~~~

# Some Rules {.r-fit-text}

# 🚯 No `sudo` {.r-fit-text}
## I don't care, no whining {.fragment}

# 📵 Do not use the sytem Python {.r-fit-text}

## For Anything {.fragment}

# 🤔 Ok Smart Guy

# pyenv

# Virtual Environments are Included 🔋 {.r-fit-text}

# pipx

<https://pypa.github.io/pipx/>

~~~{.shell}
$ brew install pipx
$ pipx ensurepath
~~~

pipx is ready to go! ✨ 🌟 ✨


## Let's do some damage {.fragment}

~~~{.shell .fragment}
$ pipx install httpie
  installed package httpie 2.4.0, Python 3.9.6
  These apps are now globally available
    - http
    - https
done! ✨ 🌟 ✨
~~~


# What about the "user scheme"?

    $ python -m pip install --user SomePackage

# But what about ...

* [Anaconda Python and Conda](https://www.anaconda.com/products/individual)
* [ActiveState Python](https://www.activestate.com/products/python/)
* [pipenv](https://pipenv.pypa.io/en/latest/)
* [poetry](https://python-poetry.org/)
* [PDM](https://pypi.org/project/pdm/)
* [pyproject.toml](https://www.python.org/dev/peps/pep-0621/)

# But I want repeatability...

* [piptools](https://github.com/jazzband/pip-tools/#readme)

# I mean really repeatable...

## Enter Docker + `pip-tools`