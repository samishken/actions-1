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
