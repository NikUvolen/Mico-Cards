.DEFAULT_GOAL := help

MANAGER = python manage.py
DOCKER = docker compose

help:
	@echo "Makefile commands:"
	@echo "  manage <command>  - Run a Django management command"
	@echo "  run        	   - Start the Django development server"
	@echo "  migrate           - Apply database migrations"
	@echo "  createsuperuser   - Create a new superuser"
	@echo "  test              - Run tests"

up:
	$(DOCKER) up -d 

build:
	$(DOCKER) up --build -d

down:
	$(DOCKER) down

manage:
	$(MANAGER) $(filter-out $@,$(MAKECMDGOALS))

run:
	$(MANAGER) runserver

migrate:
	$(MANAGER) migrate

createsuperuser:
	$(MANAGER) createsuperuser

test:
	$(MANAGER) test

