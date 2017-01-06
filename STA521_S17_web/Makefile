REMOTEUSER ?= clyde
REMOTEHOST ?= okeeffe.stat.duke.edu
REMOTEDIR ?= /web/isds/docs/courses/Spring17/sta521
REMOTE ?= $(REMOTEUSER)@$(REMOTEHOST):$(REMOTEDIR)

.PHONY: clean
clean:
	rm -rf _site/*

push: build
	rsync -az _site/* $(REMOTE)

build:
	jekyll build

unbind:
	lsof -wni tcp:4000

serve:
	jekyll serve --watch --baseurl ''


