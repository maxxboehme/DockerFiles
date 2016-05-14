# Development image used for building C/C++ projects
# Installs
# - gcc g++
# - catch (C++ Automated Test Cases in Headers)
# - gtest
FROM maxxboehme/base-dev:latest

RUN apt-get install -y gcc g++

RUN apt-get install -y catch

ENV GTEST_VERSION 1.7.0

# installing gtest
RUN wget https://googletest.googlecode.com/files/gtest-$GTEST_VERSION.zip \
   && unzip gtest-$GTEST_VERSION.zip \
   && cd gtest-$GTEST_VERSION \ 
   && mkdir /opt/gtest /opt/gtest/include /opt/gtest/lib \
   && ./configure --prefix=/opt/gtest \
   && make \
   && cp -a include/gtest/ /opt/gtest/include \
   && cp -a lib/.libs/* /opt/gtest/lib \
   && rm /opt/gtest/lib/libgtest.la \
   && rm /opt/gtest/lib/libgtest_main.la \
   && cp -a lib/libgtest.la /opt/gtest/lib \
   && cp -a lib/libgtest_main.la /opt/gtest/lib
