speedtest-cli
=============

Origin source taken from https://github.com/sivel/speedtest-cli

Updates
--------

Adding color scheme on result, on master version of this app is flat, 
and I adding some red color to make it more readable

::

    wget -O speedtest-cli https://raw.githubusercontent.com/cwicaksono/speedtest-cli/master/speedtest.py
    chmod +x speedtest-cli


Inconsistency
-------------

It is not a goal of this application to be a reliable latency reporting tool.

Latency reported by this tool should not be relied on as a value indicative of ICMP
style latency. It is a relative value used for determining the lowest latency server
for performing the actual speed test against.

There is the potential for this tool to report results inconsistent with Speedtest.net.
There are several concepts to be aware of that factor into the potential inconsistency:

1. Speedtest.net has migrated to using pure socket tests instead of HTTP based tests
2. This application is written in Python
3. Different versions of Python will execute certain parts of the code faster than others
4. CPU and Memory capacity and speed will play a large part in inconsistency between
   Speedtest.net and even other machines on the same network

Issues relating to inconsistencies will be closed as wontfix and without
additional reason or context.
