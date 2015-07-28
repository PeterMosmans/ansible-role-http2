Ansible Role: http2
===================


Build status for this role: [![Build Status](https://travis-ci.org/PeterMosmans/ansible-role-http2.svg)](https://travis-ci.org/PeterMosmans/ansible-role-http2)


This role installs and configures several HTTP/2 tools straight from their github source. The following tools are built:
* [OpenSSL 1.0.2-chacha - an OpenSSL fork containing the ChaCha20 and Poly1305 cipher)](https://github.com/PeterMosmans/openssl)
* [SPDYLAY - SPDY protocol version 2, 3 and 3.1 implementation in C](https://github.com/tatsuhiro-t/spdylay)
* [nghttp2 - HTTP/2 C Library and several tools](https://github.com/tatsuhiro-t/nghttp2)
* [curl - built with http/2 support](https://github.com/bagder/curl)

The following tools will be at your disposal:
* curl
* h2load
* nghttp
* nghttpx
* nghttpd
* openssl

The following libraries will be installed:
* libcrypto
* libssl
* libspdylay
* libnghttp2
* libcurl

Note that the role installs all libraries and tools each time, fresh from their github repositories. Currently it doesn't check the status of previously installed libraries and tools. It also doesn't remove the packages necessary for compiling all the tools.


Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: all
  become: yes
  become_method: sudo
  roles:
    - role: PeterMosmans.http2
```
This example will configure, build and install all tools.


License
-------

GPLv3

Author Information
------------------

Created by Peter Mosmans. Feedback always appreciated.
