pipeline {
    agent any
    stages {
        stage('parallel-stage') {
          parallel {
            stage('stage1') {
                steps {
                    withMaven(maven: 'maven 3.6.1', jdk: 'jdk 8u212') {
                        sh 'mvn clean install'
                    }

                  }
            }
            stage('stage2') {
              steps {
                echo 'Hello Cat2!!!'
              }
            }
          }
        }
    }
}
