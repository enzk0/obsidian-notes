
#### Setting an Existing App
---
Start ***Docker***
Start ***Ubuntu***
Go to the `frappe-docker-dev-env` directory

Run Command:
```
docker compose -f .devcontainer/docker-compose.yml up -d
```
- Docker containers should be running

Run command:
```
docker exec -e "TERM=xterm-256color" -w /workspace/development -it devcontainer-frappe-1 bash
```
- Should enter in frappe shell

Create a new ***site***, run commands:
```
bench new-site <sitename>
```
- Recommended site name is the name of the school
```
bench use <sitename>
```
- This is to use the site

Go to the product link of the site
	- Go to download backups
	- Request to download the latest backup
	- Download and Unzip the backup
	- Move backup to the to the branch development folder

Run command:
```
bench --site <sitename> --force restore <backup>.sql
```
- This restores the backup
- When SQL has -s:
```
head -20 <database.sql>
```
- then:
``` 
sed -i 's/\\-/-/g' <database.sql>
```

Get the app by running this command:
```
bench get-app <ssh_repository_link>
```
 Run command `nano .git/config`
		- check upstream to fetch all branches
		- check ssh link and add `-work`

Run command:
```
bench migrate && bench set-config -g developer_mode 1 && bench set-admin-password pass123
```
- Then
```
bench start
```

#### Starting the Task
---
***Setting an Existing App*** should already be done

1. Set your current directory to the app directory
2. Run commands:
	- `git pull`
	- `git checkout dev`
	- `git checkout dev -b <recommended branch name>`
3. Complete the tasks
4. Push the branch by using:
	- `git push upstream <branch name>`
5. See ***Creating a Pull Request***

#### Creating a Pull Request
---
Can be a ***normal pull request*** or a ***hotfix pull request***

After pushing a branch, should create a ***pull request*** to the Github client

***Normal Pull Request***
- check if the base for comparison is the dev branch
- go to discord and write the PR Link, Task Link to the livro-prs channel
- assign Ma'am Reyah as the current assignee
- merge if changes are approved

***Hotfix Pull Request***
- check if the base for comparison is the master branch
- go to discord and write the PR Link, Task Link to the livro-prs channel
- assign Ma'am Reyah as the current assignee
- wait for changes, DO NOT MERGE


***In updating***

- run on wela_colleges:
```
git pull
```

- run:
```
./apps/wela_colleges/update_script.sh
./apps/wela/update_script.sh
./apps/billing/update_script.sh
```

