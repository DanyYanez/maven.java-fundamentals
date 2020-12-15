node {
  def app
  
  stage ('Clone Repository') {
    checkout scm
  }
  
  stage ('Build Image') {
    app = docker.build
  }
  
}



//pipeline {
  //agent any 
  //stages {
    //stage('Compile Package') {
      //steps {
        //script {
         //echo 'Compile Package'
         //def mvnHome = tool name: 'maven3.6.3', type: 'maven'
         //sh "${mvnHome}/bin/mvn package -Dmaven.test.failure.ignore=true"
          //}
      //}
    //}
  //}
//} 
