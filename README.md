#Overview of GitHub Actions:

The github actions file is written in .yml file. 
Path of the file should be =repository-name/.github/workflows/file-name.yml

```
The flow of GitHub Actions is as follows:

		Workflow
		    |
		    |
		   Jobs
		    |
		    |
		   Steps

```

1. How the workflow will run?
A) using --> on:

2. When will it run?
A) Whenever I push the code.

3. Mention on which branch you will push so that the workflow runs.
A) branches: [main]

4. Where does jobs run?
A) By default GitHub Actions gives Runners(servers where jobs run)
   Every jobs need a runner.
   Every job needs a seperate runners, now this is called "Parallelism".

Runners are 2 types:
- GitHub Runners {it has few limitations}
- Self-Hosted Runners {such as EC2}

Every Month we get 2,000 mins/month github runners for free.

5. how to set a Manual click (continuous delivery) workflow.
```
on:
  workflow-dispatch:
```


