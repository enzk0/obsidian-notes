
## Task 1: Creating a Site and App
---
> [!NOTE] Notable Commands:
> To Start docker container:
> 	`docker compose -f .devcontainer/docker-compose.yml up -d`
> 
> To enter in Frappe Shell
> 	`docker exec -e "TERM=xterm-256color" -w /workspace/development -it devcontainer-frappe-1 bash`
> 

Important: When executing bench commands make sure you are in your ***frappe-bench*** folder
- [x] New site:
- Using the command:
	`bench new-site (site name)`

Ex.:
	`bench new-site my-site.localhost

- [ ] New App:
	`bench new-app (app name)`

Ex.:
	`bench new-app my_app

- [ ] Installing App to the site:
	`bench --site (site name) install-app (app_name)

Ex.
	`bench --site my-site.localhost install-app my_app


> [!References] References
> 
[https://frappeframework.com/docs/user/en/tutorial/create-a-site](https://frappeframework.com/docs/user/en/tutorial/create-a-site) [https://frappeframework.com/docs/user/en/tutorial/create-an-app](https://frappeframework.com/docs/user/en/tutorial/create-an-app) [https://frappeframework.com/docs/user/en/basics/apps#installing-an-app-into-a-site](https://frappeframework.com/docs/user/en/basics/apps#installing-an-app-into-a-site)

```
bench new-app test-app
App Title [Test App]: 
App Description: For Testing
App Publisher: 
App Publisher: Admin
App Email: test@livro.systems
```

## Task 2: Make a DocType name Athlete

- [ ] ***Make A DocType***
**Fields**
- First Name (Data)
- Last Name (Data)
- Middle Name (Data)
- Age (Integer)
- Sports (Type: Select, Options: Basketball, Baseball, Soccer)

References: [https://frappeframework.com/docs/user/en/tutorial/create-a-doctype#creating-a-doctype](https://frappeframework.com/docs/user/en/tutorial/create-a-doctype#creating-a-doctype)