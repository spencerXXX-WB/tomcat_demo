pipeline {
    agent any
      tools {
        jdk 'jdk17'
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
        stage('Deploy') {
            steps {
              deploy adapters: [tomcat9(path: '', url: 'http://54.227.178.17:8080/')], contextPath: 'spencer', onFailure: false, war: 'target/*war'
            }
        }
    }
}
