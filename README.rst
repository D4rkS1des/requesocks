💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎

the project is obsolete, just use the recent version of **Requests**, with built-in socks support

💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎💎

Requesocks is the fork of github.com/foxx/requests == python-requests *working with socks proxy* (i.e tor).
Just renamed the package to allow simultaneously use of original requests and socks-capable-requests.

Requests: HTTP for Humans
=========================

.. image:: https://secure.travis-ci.org/kennethreitz/requests.png?branch=develop

Requests is an ISC Licensed HTTP library, written in Python, for human
beings.

Most existing Python modules for sending HTTP requests are extremely
verbose and cumbersome. Python's builtin urllib2 module provides most of
the HTTP capabilities you should need, but the api is thoroughly broken.
It requires an enormous amount of work (even method overrides) to
perform the simplest of tasks.

Things shouldn't be this way. Not in Python.

::
    session = requesocks.session()
    session.proxies = {'http': 'socks5://127.0.0.1:9050',
                       'https': 'socks5://127.0.0.1:9050'}
    r = session.get('https://api.github.com', auth=('user', 'pass'))
    print(r.status_code)
    print(r.headers['content-type'])
    print(r.text)
    ...

See `the same code, without Requests <https://gist.github.com/973705>`_.

Requests allow you to send  **HEAD**, **GET**, **POST**, **PUT**,
**PATCH**, and **DELETE** HTTP requests. You can add headers, form data,
multipart files, and parameters with simple Python dictionaries, and access the
response data in the same way. It's powered by httplib and `urllib3
<https://github.com/shazow/urllib3>`_, but it does all the hard work and crazy
hacks for you.


Features
--------

- International Domains and URLs
- Keep-Alive & Connection Pooling
- Sessions with Cookie Persistence
- Browser-style SSL Verification
- Basic/Digest Authentication
- Elegant Key/Value Cookies
- Automatic Decompression
- Unicode Response Bodies
- Multipart File Uploads
- Connection Timeouts


Installation
------------

To install requests, simply: ::

    $ pip install requesocks

Or, if you absolutely must: ::

    $ easy_install requesocks

But, you really shouldn't do that.



Contribute
----------

#. Check for open issues or open a fresh issue to start a discussion around a feature idea or a bug. There is a Contributor Friendly tag for issues that should be ideal for people who are not very familiar with the codebase yet.
#. Fork `the repository`_ on Github to start making your changes to the **develop** branch (or branch off of it).
#. Write a test which shows that the bug was fixed or that the feature works as expected.
#. Send a pull request and bug the maintainer until it gets merged and published. :) Make sure to add yourself to AUTHORS_.

.. _`the repository`: http://github.com/kennethreitz/requests
.. _AUTHORS: http://github.com/kennethreitz/requests/blob/master/AUTHORS
