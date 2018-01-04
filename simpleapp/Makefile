APP = node-web-app
DOCKER_REPO = some-repo
DOCKER_IMAGE = $(DOCKER_REPO)/$(APP)

build:
	docker build -t $(DOCKER_IMAGE):initial .
	docker tag $(DOCKER_IMAGE):initial $(DOCKER_IMAGE):latest

run: build
	docker run -p 12080:8080 $(DOCKER_IMAGE):latest

runmany: build
	docker run -d -p 12081:8080 $(DOCKER_IMAGE):latest
	docker run -d -p 12082:8080 $(DOCKER_IMAGE):latest
	docker run -d -p 12083:8080 $(DOCKER_IMAGE):latest