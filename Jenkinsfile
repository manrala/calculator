pipeline {
  agent any
  stages {
    stage('CheckOut'){
      steps{
        checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/manrala/calculator.git']])
      }
    }
    stage('Compile'){
      steps{
        sh "./gradlew compileJava"
      }
    }
  }
}
