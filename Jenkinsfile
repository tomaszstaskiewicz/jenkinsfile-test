pipeline {
  agent {
    docker {
      image "ubuntu:22"
      label "azure && ubuntu"
    }
  }

  environment {
    MY_ENV = "123"
  }

  parameters {
    choice(
      name: "priority",
      choices: "low\nmedium\nhigh",
      description: "Select the priority")
  }

  stages {
    stage("Stage 1") {
        steps {
            sh 'echo "Hello Wor(l)d!"'
          }
    }
    stage("Stage 2") {
        steps {
            script {
              sh 'go --version'
            }
        }
    }
  }
}
        