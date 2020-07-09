pipeline {
  agent any
  stages {
    stage('Compile') {
      steps{
        sh 'mvn clean compile'
      }
    }
    stage ('code review'){
         steps {
            sh 'mvn clean pmd:pmd'
           }   }
     
    stage('Unit Test') {
      steps{
        sh 'mvn clean test'
      }
    }
stage ('install')
     {
       steps
          {
            sh 'mvn clean install'
         }  }
    stage('Package') {
      steps{
        sh 'mvn clean package'
      }
    }
  }
}
