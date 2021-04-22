# Makefile

SHARELATEX_BASE_TAG := fred1653/sharelatex-base
SHARELATEX_TAG := fred1653/sharelatex
SHARELATEX_FULL_TAG := fred1653/sharelatex-full

build-base:
	DOCKER_BUILDKIT=1 docker build -f Dockerfile-base -t  $(SHARELATEX_BASE_TAG) .


build-community:
	DOCKER_BUILDKIT=1 docker build --build-arg SHARELATEX_BASE_TAG=$(SHARELATEX_BASE_TAG) -f Dockerfile -t $(SHARELATEX_TAG) .


build-community-full:
	DOCKER_BUILDKIT=1 docker build --build-arg SHARELATEX_BASE_TAG=$(SHARELATEX_BASE_TAG) -f Dockerfile-full -t $(SHARELATEX_FULL_TAG) .


PHONY: build-base build-community build-community-full
