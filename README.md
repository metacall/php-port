<div align="center">
  <a href="https://metacall.io" target="_blank"><img src="https://raw.githubusercontent.com/metacall/core/master/deploy/images/logo.png" alt="M E T A C A L L" style="max-width:100%; margin: 0 auto;" width="80" height="80">
  <p><b>M E T A C A L L</b></p></a>
  <p>A library for providing inter-language foreign function interface calls</p>
</div>

# Abstract

**METACALL** is a library that allows calling functions, methods or procedures between programming languages. With **METACALL** you can transparently execute code from / to any programming language, for example, call Python code from PHP.

# Install

Install MetaCall binaries first ([click here](https://github.com/metacall/install) for additional info about the install script):
```bash
bash <(curl -sL https://raw.githubusercontent.com/metacall/install/master/install.sh)
```

Then install MetaCall PHP package through MetaCall:
```bash
# TODO: Composer not implemented yet in the CLI (Guix Distributable builds)
metacall composer install metacall
```

# Example

`sum.py`
``` python
def sum(a, b):
  return a + b
```

`main.php`
``` php
require('metacall.php'); // Import MetaCall
require('sum.py'); // Import Python script

sum(3, 4); // 7
```

``` sh
# TODO: PHP Loader not implemented yet
metacall main.php
```
