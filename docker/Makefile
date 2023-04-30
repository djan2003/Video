#!/usr/bin/make

SHELL = /bin/sh

fresh: build run init info # refresh all/create new

build: # build db, nginx and app container
	docker-compose build

run: # run existing containers
	docker-compose up -d

init: # init lumen app in app container
	docker exec -it video-app composer install
	#docker exec -it video-front yarn install
	#docker exec -it video-front quasar dev

	 # docker exec -it video-app php artisan l5-swagger:generate

info: # information about containers
	docker-compose ps

down: # stop all containers
	docker-compose down
