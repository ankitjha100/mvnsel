pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/ankitjha100/mvnsel.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run Jar') {
            steps {
               sh 'java -jar target/MyMavenSeleniumApp01-1.0-SNAPSHOT.jar'
            }
        }
    }
}
