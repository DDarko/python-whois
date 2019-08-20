whois
=====
A Python package for retrieving WHOIS information of domains.

Features
=============
* Python wrapper for Linux "whois" command
* simple interface to access parsed WHOIS data for a given domain
* able to extract data for all the popular TLDs (com, org, net, biz, info, pl, jp, uk, nz,  ...)
* query a WHOIS server directly instead of going through an intermediate web service like many others do
* works with Python 2.4+ and Python 3.x
* all dates as datetime objects
* possibility to cache results

Help Wanted
===========
You contributions are welcome , look for the Help wanted tag https://github.com/DannyCork/python-whois/labels/help%20wanted

Usage example
=============

.. code-block:: text

    $pip install whois

.. code-block:: python

    >>> import whois
    >>> domain = whois.query('google.com')

    >>> print(domain.__dict__)
    {
    'expiration_date': datetime.datetime(2020, 9, 14, 0, 0),
    'last_updated': datetime.datetime(2011, 7, 20, 0, 0),
    'registrar': 'MARKMONITOR INC.',
    'name': 'google.com',
    'creation_date': datetime.datetime(1997, 9, 15, 0, 0)
    }

    >>> print(domain.name)
    google.com

    >>> print(domain.expiration_date)
    2020-09-14 00:00:00


ccTLD & TLD support
===================


global top level domains (GTLD)

.tv
.cc
.nyc
.pw
* biz
* com
* info
* me
* name
* net
* org
* io
.xyz
.tel
.online
.wiki
.press
.rest
.security
.site
.website
.tickets
.theatre
.tech
.store
.space

Country code top leve domains (ccTLD)
.tv
.cc
.nyc
.pw
* uz
* at
* be
* br
* co
* co.jp
* cz
* de
* eu
* fr
* it
* jp
* lv
* nz
* pl
* ru
* uk
* us
* mx
* br
* sh
* id

Issues
=============
Raise an issue https://github.com/DannyCork/python-whois/issues/new


Support
=======
Python 3.x supported. Should work on Python 2.x but not supported.
