pipeline {
    parameters {
	   string(name: 'P1', defaultValue: '0.0.0.0', description: 'P1')
       booleanParam(name: 'P2', defaultValue: true, description: 'P2')
   }

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
