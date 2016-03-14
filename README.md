# alpine-rvm-gcc
Dockerfile for installing RVM and latest ruby on Alpine Linux and retains build tools

Installs [RVM](https://rvm.io/) as a non-root user on [Alpine](https://www.alpinelinux.org/), then installs [Ruby](https://www.ruby-lang.org/).

## Notes
* Version of [Alpine Linux](https://www.alpinelinux.org/) is hard-coded in "FROM".
* Version of [Ruby](https://www.ruby-lang.org/) is hard-coded in both the Dockerfile *and* /home/rvm/.profile
* [RVM](https://rvm.io/) as such isn't the best on this platform. It really only understands non-[musl](http://www.musl-libc.org/) Linux, but it's a useful base for installing.
* Indeed, it still moans about musl's ldd when you log in.
* This image is intended to be used as a base for others, and keeps the compiler, etc. installed. Once ready for production apk del the packages. See [alpine-rvm](https://github.com/nicdoye/alpine-rvm) for a version where that has already been done.

Nic Doye - 2016.03.14
