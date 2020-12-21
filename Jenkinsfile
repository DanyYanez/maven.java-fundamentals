pipeline {
    agent {
      docker {
        image "maven:3-alpine"
        //label "docker"
        args '-v /root/.m2:/root/.m2'
      }
    }
      
    stages {
      stage('Compile Package') {
        steps {
          script {
            echo 'Compile Package'
            dir('$PWD/maven.java-fundamentals') {
              sh "mvn package -Dmaven.test.failure.ignore=true"
            }
            //def mvnHome = tool name: 'maven3.6.3', type: 'maven'
            //sh ${mvnHome}/bin/mvn package -Dmaven.test.failure.ignore=true
            //sh "${mvnHome}/bin mvn package -Dmaven.test.failure.ignore=true"
          }
        }
      }
    }
} 
