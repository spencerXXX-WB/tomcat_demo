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
                 deploy contextPath: '/opt/tomcast/webapps', war: '/home/ubuntu/.jenkins/workspace/job-1/target/*war'
            }
        }
    }
}
