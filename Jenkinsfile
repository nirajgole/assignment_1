pipeline {
    agent any  // Use any available agent

    triggers {
        scm;
    }

    stages {
        stage('Pull Code') {
            steps {
                git branch: 'develop', // Specify the branch to pull (optional)
                    // credentialsId: 'your-credentials-id', // Replace with your credential ID (optional)
                    url: 'https://github.com/nirajgole/assignment_1.git' // Replace with your Git repository URL (optional)
                    // Use the above options if you didn't provide them in the SCM configuration
                sh 'git pull origin develop' // Pull code from the Develop branch
            }
        }
        stage('Build') {
            steps {
                // Steps to build the project (e.g., using build tools like Maven, Gradle)
                echo "Successfully built!"
            }
        }
    }
}
