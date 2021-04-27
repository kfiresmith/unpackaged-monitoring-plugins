# unpackaged-monitoring-plugins
A holding pen for various monitoring plugins from disparate sources and authors

## Content Origins
The checks within this repo are collected from various non-VCS locations, and were written by random sysadmins who may have posted the checks in online help forums or other locations that are not as easy to pull from or refer to as a Git repo.

When possible, I try to track down check authors and encourage them to submit their checks to [https://monitoring-plugins.org], but often the checks are abandoned by their original authors.  

The goal of this repo is to compile these checks and archive them for posterity.

## Are you a check author?
If you wrote one of the checks in this repo - thanks!  

If you object for some reason to my including your content here, please drop me a line and I'll remove your check and optionally include a pointer to it if you have it hosted elsewhere and wish for people to continue using it. 


## Useful checks that are not packaged, but hosted elsewhere:
**[check_squid](https://git.dinotools.org/monitoring/check_squid)**

This check monitors the following aspects of Squid: Connections (default), Cache, Resources, Memory(broken), FileDescriptors.
You must have Squid ACLs in place that enable access to the monitoring interface, like so:
```
acl monitoring_servers src 123.123.234.10/32 123.123.234.11/32

http_access allow manager monitoring_servers
http_access deny manager
```
You also must have 'squidclient' installed on the Nagios (or Icinga etc) servers.
