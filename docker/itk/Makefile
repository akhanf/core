NAME = khanlab/itk
VERSION = 0.0.1

.PHONY: all build tag_latest push push_latest run last_built_date

all: build

build:
	docker build -t $(NAME):$(VERSION) --rm .

tag_latest:
	docker tag $(NAME):$(VERSION) $(NAME):latest

push:
	docker push $(NAME):$(VERSION)

push_latest:
	docker push $(NAME):latest

run:
	docker run --rm -it $(NAME):$(VERSION) /bin/bash	

last_built_date:
	docker inspect -f '{{ .Created }}' $(NAME):$(VERSION)

