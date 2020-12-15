pipeline {
  agent {
    docker {
      image "maven:3.6.3-jdk-13"
      //label "docker"
      args '-v /root/.m2:/root/.m2'
    }
  }
      
  stages {
    stage('Compile Package') {
      steps {
        script {
         echo 'Compile Package'
         def mvnHome = tool name: 'maven3.6.3', type: 'maven'
         sh ${mvnHome}/bin/mvn package -Dmaven.test.failure.ignore=true
         //sh "${mvnHome}/bin/mvn package -Dmaven.test.failure.ignore=true"
        }
      }
    }
  }
  post {
    always {
      cleanWs()
    }
  }
} 
