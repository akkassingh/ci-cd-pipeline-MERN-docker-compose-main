
tag:=v1.0.${TAG}
images_name:=ci-cd-frontend
repository:=akkassingh

all: build push

build:
	@ docker build --platform linux/amd64 --no-cache -t ${images_name}:${tag} .

push:
	@ echo "push ${repository}/${images_name}:${tag} to docker hub"
	@ docker tag ${images_name}:${tag} ${repository}/${images_name}:${tag}
	@ docker push ${repository}/${images_name}:${tag}