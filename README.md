##Overview of GitHub Actions:

The github actions file is written in .yml file. 
Path of the file should be =repository-name/.github/workflows/file-name.yml

```
The flow of GitHub Actions is as follows:

		 Workflow
		    |
		    |
		   Jobs (one or more jobs that run in parallel by default; each gets its own fresh VM)
		    |
		    |
		   Steps (steps: — sequential commands inside a job. Each step is either uses: (a prebuilt action from the marketplace) or run: (a shell command))

```

1. How the workflow will run?  
A) using --> on:
   It is what triggers the workflow (push, PR, schedule, manual, etc.)

2. When will it run?  
A) Whenever I push the code.

3. Mention on which branch you will push so that the workflow runs.  
A) branches: [main]

4. Where does jobs run?  
A) By default GitHub Actions gives Runners(servers where jobs run)  
   Every job needs a seperate runners, now this is called "Parallelism". 
   for example:
   		runs-on: — which OS image (ubuntu-latest, windows-latest, macos-latest) 
```
runs-on: ubuntu-latest
```

Runners are 2 types:
- GitHub Runners (it has few limitations)
- Self-Hosted Runners (such as EC2)

Every Month we get 2,000 mins/month github runners for free.

5. how to set a Manual click (continuous delivery) workflow.
A)
```
on:
  workflow-dispatch:
```

##Trigger  
In place of tirgger we mention paths in .yml file. triggers are also called as filters.  

Whenever there is any change in index.html file, the workflow gets triggered and runs.  

```
on:  
  push:
    branches: [main]
    
    paths:'**.html'
```


Automated tests are nothing but Actions.  
Automated test = Actions  

#To clone a repository
```
uses: actions/checkout@v4
```

#To make website for free on GitHub we use github pages.
```
uses: actions/configure-pages@v4
```

