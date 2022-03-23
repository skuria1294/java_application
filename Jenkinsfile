pipeline{
  agent any
  
  stages{
    stage("Git"){
      steps{
        git branch: 'main', credentialsId: 'my-github-credentials', url: 'https://github.com/skuria1294/java_application.git'
      }
    }
  }
}
