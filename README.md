axcli
=====

A simple actionlib CLI client


How to use
----------

Add this package in your `catkin` workspace, don't forget to
source your `devel/setup.bash` after running `catkin_make`

```shell
axcli <action server> <goal> [--wait]
```

Bash should provide TAB-completion of available action
servers and their associated goals.

Unless `--wait` is specified, the program will return immediately
after sending the goal to the action server, without waiting for
any feedback or result.

If `--wait` is specified, `axcli` will wait for the goal to
terminate. Pressing 
<kbd>Ctrl+c</kbd>
will send a goal cancel request
to the action server.
