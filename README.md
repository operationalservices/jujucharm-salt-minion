# Overview

This charm provides a Salt Minion service from
[SaltStack](http://www.saltstack.com/).

Salt is a powerful remote execution manager that can be used to
administer servers in a fast and efficient way. It allows commands to
be executed across large groups of servers. This means systems can be
easily managed, but data can also be easily gathered. Quick
introspection into running systems becomes a reality. Remote execution
is usually used to set up a certain state on a remote system. Salt
addresses this problem as well, the Salt state system uses Salt state
files to define the state a server needs to be in. Between the remote
execution system, and state management Salt addresses the backbone of
cloud and data center management.

This particular package provides the worker / agent for Salt.

**Note:** Be advised that while the Salt software is mature and
  proven, this particular packaging in a juju charm is rather
  untested.

This charm is tested with Ubuntu 14.04 (trusty).

# Usage

This is a subordinate salt minion charm.

Deploy the service:

    juju deploy salt-minion
    juju set salt-minion salt-master="<IP of the salt master server>"
    juju add-relation salt-minion another-service

