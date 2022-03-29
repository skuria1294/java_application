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
	
	stage("Sonarqube"){
		environment {
			scannerHome = tool 'Sonar'
		}
		steps{
			withSonareQubeEnv('SonarServer'){
				sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=java_maven -Dsonar.sources=. -Dsonar.java.binaries=target/classes/com/mycompany/app/ "

			}
		}
	}
    
  }
}
