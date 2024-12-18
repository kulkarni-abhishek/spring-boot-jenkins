@Library('jenkins-shared-library') _
pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                gitCheckout(
                    branch: 'master',
                    url: 'https://github.com/kulkarni-abhishek/spring-boot-jenkins.git'
                )
            }
        }

        stage('Unit test gradle') {
            steps {
                gradleTest()
            }
        }
    }
}