all:
	@docker compose up -f ./srcs/docker-compose.yml -d --build
down:
	@docker compose -f ./srcs/docker-compose.yml down
clean:
	@rm -rf /home/ncruz-ga/data/mysql/*
	@rm -rf /home/ncruz-ga/data/wordpress/*
	@docker stop $$(docker ps -qa)
	@docker rm $$(docker ps -qa)
	@docker rmi $$(docker images -qa)
	@docker volume rm $$(docker volume ls -q)
	@docker network rm ncruz-ganet
.PHONY: all down clean
