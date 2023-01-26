pipeline {
  agent {
    docker {
      image "ubuntu:22"
    }
  }

  environment {
    MY_ENV = "123"
  }

  parameters {
    choice(
      name: "priority",
      choices: "low\nmedium\high",
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
        