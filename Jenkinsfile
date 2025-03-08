pipeline {
    agent any

      environment {
        PATH = "/usr/share/maven/bin:$PATH"  // Use system-installed Maven
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/jangamamahesh/Git-practice.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Using Maven version:"'
                sh 'mvn --version'  // Debugging step to verify Maven path
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
}
