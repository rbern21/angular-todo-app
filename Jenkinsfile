pipeline {
  agent { label 'master' }
  environment {
    GIT_PATH = "https://github.com/rbern21/angular-todo-app/"
    GIT_CREDENTIALS = credentials("GitHub_Credentials")
  }
  stages {
    stage('Checkout SCM') {
      steps {
        echo "Checking out..."
        echo "Target Repo: ${GIT_PATH}"
        git credentialsId: "${GIT_CREDENTIALS}" , url: "${GIT_PATH}"
        sh "ls -lah"
      }
    }
}
