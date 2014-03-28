axcli
=====

A simple actionlib CLI client

How to use
----------

Add this package in your `catkin` workspace, don't forget to
source your `devel/setup.bash` after running `catkin_make`

```shell
axcli [--nowait] [--timeout TIMEOUT] [-v] <action namespace> <goal>
```

Bash should provide TAB-completion of available action
servers and their associated goals.
By default `axcli` will wait for the goal to terminate, and pressing
<kbd>Ctrl+c</kbd> will send a goal cancel request to the action
server.

The following optional arguments are available to change
`axcli`'s behavior:

* `--nowait` don't wait for result, fire and forget.

* `--timeout` timeout in seconds used to wait for the action server
               (default: infinite timeout).

* `-v, --verbose` verbose output.
