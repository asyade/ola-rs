all:
	docker build . --tag=build-ola

it:
	docker run --rm -it --volume ${PWD}/ola:/src ola-build

build:
	docker run --rm --volume ${PWD}/ola:/src ola-build