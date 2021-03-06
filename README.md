# TODO Tools

Hey, do you like `TODO`s? Yeah, we all probably like them a little too much...
Why write actual code when you could just leave a `TODO`?

Well, fear no more about losing track of those desired code changes. This tool
is a git post-commit hook that warns you about `TODO`s that you left in your
code.

## Example (How do you mean?)

```
Here's a list of TODOs you added in this commit:
------------------------------------------------
+ todo_tools.py | # TODO(@zeb[2016-08-04]): pls check if werks
+ todo_tools.py | # TODO(@zeb[2015-08-04]): This should fail
+ todo_tools.py | # TODO: copy instance of running file to given directory
+ todo_tools.py | # TODO: consolidate saving
+ todo_tools.py | if potential_todos:  # TODO: test
+ todo_tools.py | print('')  # print newline for prettiness # TODO: ask user
These might be TODOs.  Did you mean to do them?
-----------------------------------------------
+ README.md | # TODO Tools (y/N) 
```

## Installation

We have three different ways to install this.

Note, you *do not have to do this to use the full installation*. The manual
installation method works without cluttering your `$PATH`. If you don't care
about that, by all means make your life easier and use `pip` or `setuptools`.

### PyPI

**[Coming Soon]**

```bash
┬─[william@fillory:~/todo-tools]
╰─>$ pip install todo_tools --user
```

### By Hand

Clone this repository using `git clone`, and then run `./bin/todo -i <desired
installation repository root>` to install it as a post-commit hook. For example:

```bash
┬─[william@fillory:~/todo-tools]
╰─>$ git clone https://github.com/willzfarmer/todo-tools
┬─[william@fillory:~/todo-tools]
╰─>$ cd todo-tools
┬─[william@fillory:~/todo-tools]
╰─>$ ./bin/todo -i ~/myawesomerepo
```

And it's enabled on that repository! Woo!

### Setuptools

```bash
┬─[william@fillory:~/todo-tools]
╰─>$ python setup.py install --user
┬─[william@fillory:~/todo-tools]
╰─>$ todo --install-to-bashrc
```
