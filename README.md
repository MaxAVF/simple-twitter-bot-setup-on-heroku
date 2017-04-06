# Simple Twitter Bot Setup On Heroku

# Pre-requisite
* Python Installed Obviously
* VirtualEnv Installed (pip install virtualenv)
* You must know how to deploy app on heroku [Read here](https://devcenter.heroku.com/articles/getting-started-with-python)

# Get Started
We're going to use heroku's worker dyno to acomplish this task. Although you can use job scheduling to run your bot at certain time than keep running it all time.

* **Clone this Repo**
* run `virtualenv twibot --no-site-packages` and activate it.
* Make changes to `main.py` because this is your Bot main entry file.
* see `main_example.py` for reference.
* When all done means when you've your working bot locally. Run `pip freeze requirements.txt` in the bot directory.
* And finally deploy and scale the worker dyno or run it.
# Quick Walkthrough

## Procfile
This is main file which tells Heroku, which dyno to use. We're using `worker` dyno. [Learn more about dyno](https://devcenter.heroku.com/articles/dynos).
So `worker: python main.py` tells heroku to run worker dyno and run `python main.py` command on that.
 
## Requirements (requirements.txt)
This is file created by pip when we run `pip freeze requirements.txt`. This is important because heroku will look for this file to install module dependency of your bot.

## Runtime (runtime.txt)
If you're using python 2.7 then change runtime in this file. Available runtimes are listed [here](https://devcenter.heroku.com/articles/python-runtimes)

# Me
### Twitter: [@sh4hidkh4n](https://twitter.com/sh4hidkh4n)
