pipeline {
    agent any

    tools {
        maven 'mymaven' // Your configured Maven installation
        jdk 'myjava'    // Your configured JDK installation
        git 'mygit'     // Add this line for the Git tool
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/DevopsYaml/myjava.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/classes com.example.App'
            }
        }
    }
}

