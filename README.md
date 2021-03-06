# std-domain

[![Coverage Status](https://coveralls.io/repos/github/EvanDarwin/std-domain/badge.svg?branch=master)](https://coveralls.io/github/EvanDarwin/std-domain?branch=master)[![Build Status](https://travis-ci.org/WhoisBuster/std-domain.svg?branch=master)](https://travis-ci.org/WhoisBuster/std-domain)

**std-domain** is a Python library that intends to provide a simple interface for dealing with International Domain Names (IDN).
 
It is a simple library that depends on other libraries to provide an interface for handling UTF-8 and standard domain names, and converting between the two.

## Installation

The library is available as the ``std-domain`` [package in PyPI](https://pypi.python.org/pypi?name=std-domain&version=0.0.1&:action=display).

You can either install it from *pip* like:

```sh
pip install std-domain
```

or install it in your application's dependency list.

## Usage

```python
from stddomain import Domain

# Full SLD and TLD IDN support
domain = Domain(u'名がドメイン.中国')

print(domain)
> "xn--v8jxj3d1dzdz08w.xn--fiqs8s"

# Printing the domain defaults to punycode
print(domain.domain)
> "xn--v8jxj3d1dzdz08w.xn--fiqs8s"

print(domain.idn)
> "名がドメイン.中国"

print(domain.is_idn)
> True
```

## License

This software is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license, which is [available here](https://creativecommons.org/licenses/by/4.0/)

Copyright &copy; 2016-2017 WhoisBuster