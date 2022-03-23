pipeline{
  agent any
  tools {
    maven "Maven3.8.4"
  }
  stages{
    stage("Git"){
      steps{
        git branch: 'main', credentialsId: 'my-github-credentials', url: 'https://github.com/skuria1294/java_application.git'
      }
    }
	
	stage("Maven Build"){
		steps{
			sh "mvn clean install"
		}
	}
    
  }
}
