pipeline {
    agent any
      tools {
        jdk 'jdk20'
        maven 'maven'
    } 

    stages {
         stage('Complie') {
            steps {
               sh " mvn compile"
            }
        }
        stage('Test') {
            steps {
                  sh "mvn test"
            }
        }
        stage('Package') {
            steps {
                  sh "mvn package"
            }
        }
    }
}
