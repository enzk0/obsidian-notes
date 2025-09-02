
> [!NOTE] Notable Commands:
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


