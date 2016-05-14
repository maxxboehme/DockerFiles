# Development image used for building C/C++ projects
# Installs
# - gcc g++
# - catch (C++ Automated Test Cases in Headers)
# - gtest
FROM maxxboehme/base-dev:latest

RUN apt-get install -y gcc g++

RUN apt-get install -y catch

# Tnstalling gtest
# This does not generate the library file.
# Please read 'Why is it not recommended to install a pre-compiled copy of Google Test (for example, into /usr/local)?'
# at https://github.com/google/googletest/blob/master/googletest/docs/FAQ.md#why-is-it-not-recommended-to-install-a-pre-compiled-copy-of-google-test-for-example-into-usrlocal
#
# To build static library, do something like below in your build process
# $ cd /user/src/gtest
# $ sudo cmake .
# $ sudo make
# $ sudo mv libg* /usr/lib/
RUN apt-get install -y libgtest-dev
