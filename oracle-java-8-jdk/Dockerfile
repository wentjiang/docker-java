FROM centos:7

MAINTAINER Ma Qian<maqian258@gmail.com>

RUN curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/set-sources-cn' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/install-base-pkgs' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/install-build-pkgs' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/install-oracle-java' | sh -s jdk 8 152 16 aa0333dd3019491ca4f6ddbe78cdb6d0 \
  && export JAVA_HOME=/usr/java/jdk1.8.0_152 \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/sysfree/install-jemalloc' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/sysfree/install-perf-map-agent' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/sysfree/install-ejava' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/set-timezone-cn' | sh \
  && curl -sSL 'https://raw.githubusercontent.com/maqian/toolbox/master/centos/7/set-locale-cn' | sh

ENV TIMEZONE=Asia/Shanghai TZ=Asia/Shanghai \
    LANG=zh_CN.UTF-8 LC_ALL=zh_CN.UTF-8 LANGUAGE=zh_CN.UTF-8:zh:en_US:en \
    JAVA_HOME=/usr/java/jdk1.8.0_152 \
    AGENT_HOME=/usr/local/perf-map-agent
