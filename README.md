pyUnQLite
=========

Modify cython binding of pyunqlite more like python sqlite interface and dict interface


I copy from (https://bitbucket.org/east301/py-unqlite)

version 1f1e3ab-2013.07.06

Follow is original project doc.

py-unqlite
==========

Unofficial python bindings for [UnQLite](http://unqlite.org/), an embeddable NoSQL database engine.


Example
-------

    import pyunqlite

    db = pyunqlite.UnQLite()
    db.open('/tmp/test.db')

    db.store('foo', 'bar')
    print db.fetch('foo')  # => 'bar'

    db.delete('foo')

    db.close()


Installation
------------

    $ pip install cython
    $ cd path/to/pyunqlite/source/code/directory
    $ python setup.py build
    $ python setup.py install


Files
-----

* __example.py__: usage example of py-unqlite
* __pyunqlite.pyx__: UnQLite python wrapper written in [Cython](http://cython.org/)
* __unqlite.c__, __unqlite.h__: [UnQLite 1.1.6 source code](http://unqlite.org/downloads.html)


Credits
-------

### UnQLite

    /*
     * Copyright (C) 2012, 2013 Symisc Systems, S.U.A.R.L [M.I.A.G Mrad Chems Eddine <chm@symisc.net>].
     * All rights reserved.
     *
     * Redistribution and use in source and binary forms, with or without
     * modification, are permitted provided that the following conditions
     * are met:
     * 1. Redistributions of source code must retain the above copyright
     *    notice, this list of conditions and the following disclaimer.
     * 2. Redistributions in binary form must reproduce the above copyright
     *    notice, this list of conditions and the following disclaimer in the
     *    documentation and/or other materials provided with the distribution.
     *
     * THIS SOFTWARE IS PROVIDED BY SYMISC SYSTEMS ``AS IS'' AND ANY EXPRESS
     * OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
     * WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, OR
     * NON-INFRINGEMENT, ARE DISCLAIMED.  IN NO EVENT SHALL SYMISC SYSTEMS
     * BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
     * CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
     * SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR
     * BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
     * WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
     * OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN
     * IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
     */
