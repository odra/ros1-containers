SHELL := /bin/bash
REG := quay.io
ORG := lrossett
NAME := ros
TAG := latest
IMAGE := ${REG}/${ORG}/${NAME}:${TAG}
CRIO := podman
BUILD_OPTS :=

build:
	${CRIO} build ${BUILD_OPTS} -t ${IMAGE} .

push:
	${CRIO} push ${IMAGE}

debug:
	${CRIO} run -it ${IMAGE} /bin/bash

.PHONY: build push debug
