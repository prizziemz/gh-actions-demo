name: Hello World!
on: 
  push:
    branches: [main]
  pull_request:
    branches: [main]        
jobs:
  hello-job: 
    runs-on: ubuntu-latest
    steps:
    - name: Run a one-line script
      run: echo "Hello Github Actions 3 2!"
    - name: Retrive Client payload 
      run: echo "Client payload is ${github.event.client_payload.status}"
  Second-job:
    runs-on: ubuntu-latest
    needs: hello-job
    steps:
      - name: "Check runner OS and name" 
        run: echo "This job is running on ${RUNNER_OS} and the runner name is ${RUNNER_NAME}"      
