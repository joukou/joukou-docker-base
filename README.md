Base Dockerfile for Joukou
==========================
[![Build Status](https://circleci.com/gh/joukou/joukou-docker-base/tree/develop.png?circle-token=5768d1c8d51530e3b7083a02e6c7783daa316b2c)](https://circleci.com/gh/joukou/joukou-docker-base/tree/develop) [![Docker Repository on Quay.io](https://quay.io/repository/joukou/base/status?token=466de50c-9ef1-4ac0-ae88-60625549cf25 "Docker Repository on Quay.io")](https://quay.io/repository/joukou/base) [![Apache 2.0](http://img.shields.io/badge/License-Apache%202.0-brightgreen.svg)](#license) [![Stories in Ready](https://badge.waffle.io/joukou/joukou-docker-base.png?label=ready&title=Ready)](http://waffle.io/joukou/joukou-docker-base) [![IRC](http://img.shields.io/badge/IRC-%23joukou-blue.svg)](http://webchat.freenode.net/?channels=joukou)

A lean, stable and CoreOS focused Dockerfile to be used as the base for all
Dockerfiles created for [Joukou](https://joukou.com).

## Base Image

This Dockerfile is based on
[Ubuntu Trusty Tahr](https://github.com/joukou/joukou-docker-ubuntu).

## Philosophy

While we believe a Docker container should only execute a single service,
therefore no init system is included.

The SSH daemon is not included as it is a potential attack vector and an
unnecessary overhead to run in every container. Instead use
[`nsenter`](https://github.com/jpetazzo/nsenter).

Tools that are useful for CoreOS deployments are included; e.g.
[`jq`](http://stedolan.github.io/jq/), `etcdctl`, `docker`.

## Metrics

[![Throughput Graph](https://graphs.waffle.io/joukou/joukou-docker-base/throughput.svg)](https://waffle.io/joukou/joukou-docker-base/metrics)

## License

Copyright &copy; 2014 Joukou Ltd.

Base Dockerfile for Joukou is under the Apache 2.0 license. See the
[LICENSE](LICENSE) file for details.

Parts of the [Phusion Base Image](https://github.com/phusion/baseimage-docker)
used under the terms of the MIT license Copyright (c) 2013-2014 Phusion.
