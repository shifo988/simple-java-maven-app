pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'  // Run tests
            }
        }
        stage('Deploy') {
            steps {
                // Assuming a simple deployment command, replace with your actual deployment logic
                sh 'scp target/myapp.jar user@server:/path/to/deploy' 
            }
        }
    }
}
