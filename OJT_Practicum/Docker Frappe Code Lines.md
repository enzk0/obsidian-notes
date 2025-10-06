
#### Setting an Existing App
---

1. Start ***Docker***
2. Start ***Ubuntu***
3. Go to the `frappe-docker-dev-env` directory
4. Run Command:
	- `docker compose -f .devcontainer/docker-compose.yml up -d`
	- Docker containers should be running
5. Run command:
	- `docker exec -e "TERM=xterm-256color" -w /workspace/development -it devcontainer-frappe-1 bash`
	- Should enter in frappe shell
6. Create a new ***site***, run command:
	- `bench new-site <sitename>`
	- Recommended site name is the name of the school
	