# actions-1
Welcome to my Github Actions course

### Workflows: offer flexibility and ease of use for task automation
- 
### Actions:  
- Actions provide a structured, reusable framework for complex business logic and integrations
- "Checkout Action" 

### Disable
- disable unnessary workflows

### How to execute shell script

# by default all job in a single workflow run parallelly
- "needs": help us run jobs in sequence.

### how to move artifacts from one job to another
- moving artifacts from one job to another use these actions
- - - - `actions/download-artifact@v4`
- - - - `actions/download-artifact@v4`

### Variables
- Variables defined inside a job applies to all steps inside that job.
- `vars.DOCKER_USERNAME`: vars for variables
- `secrets.DOCKER_PASSWORD`: secrets for secrets


### Triggers 
- "pull"
- "cron jobs" (site: crontab.guru)
- "workflow_dispatch:"    # manually trigger workflows


### Concurrency
- we don't want to deployments happening at the same time
- concurrency takes two parameters: group and cancel-in-progress
- "cancel-in-progress": 
- - - - True: will cancel any running workflow and start running the new workflow
- - - - False: will wait until running workflow completes before running new workflow

### Timeouts
- can be added at job or step level
- protects workflows from running for unneccessary long time.
- Example: `timeout-minutes: 1`

### Matrix for jobs
- Matrix strategy lets us use variables in a single job definition to automatically create multiple job runs that are based on the combinations of variables.
- one job is enough
- - - - Exclude: ensures certain os/runner from running a specific image
- - - - Include: ensures to run a specific image on specific os/runner
- - - - fail-fast: cancel failing jobs from linguring
- - - - max-parallel: control number of jobs running at the same time