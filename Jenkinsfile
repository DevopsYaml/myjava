pipeline {
    agent any

    tools {
        maven 'mymaven' // Change this to your configured Maven version in Jenkins
        jdk 'myjava'       // Change this to your configured JDK in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/DevopsYaml/myjava.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/classes com.example.App'
            }
        }
    }
}

