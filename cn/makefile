.PHONY: baseimage

cn_flags = NUCLIO_BASE_IMAGE_NAME=golangcn NUCLIO_BASE_IMAGE_TAG=1.17 NUCLIO_BASE_ALPINE_IMAGE_NAME=golangcn  NUCLIO_BASE_ALPINE_IMAGE_TAG=alpine3.16

baseimage:
	docker build -t golangcn:1.17 -f dockerfile.base .
	docker build -t golangcn:alpine3.16 -f dockerfile.alpine .


handler-builder-golang-onbuild-alpine: baseimage
	cd .. && $(cn_flags) make handler-builder-golang-onbuild-alpine


handler-builder-golang-onbuild: baseimage
	cd .. && $(cn_flags) make handler-builder-golang-onbuild 
	
