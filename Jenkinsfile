pipeline{

agent any

tools{

maven "Maven3.8.4"
}
stages{
stage{
steps{
git branch: 'steve-branch', credentialsId: 'my-github-credentials', url: 'https://github.com/skuria1294/java_application.git'
}
}
}

}
