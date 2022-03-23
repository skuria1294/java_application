pipeline{

agent any

tools{

maven "Maven3.8.4"
}
stages{
stage("git"){
steps{
git branch: 'steve-branch', credentialsId: 'my-github-credentials', url: 'https://github.com/skuria1294/java_application.git'
}
}
}
 stage("maven build"){
 
 steps{
 
 sh "mvn clean install"
 
 }
 
 }


}
