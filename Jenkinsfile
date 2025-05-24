pipeline {
  agent any  // Runs directly on Jenkins master
  
  stages {
    stage('Clone Repo') {
      steps {
        git(url: 'https://github.com/d2arshan/PRTDevOps', branch: 'main') 
      } 
    }

