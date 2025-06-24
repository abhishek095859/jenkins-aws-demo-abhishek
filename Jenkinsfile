

pipeline {
    agent {
        label 'ubuntu'
    }

    stages {
        // A stage is a logical block in our pipeline, like 'Build' or 'Test'
        stage('Install Dependencies') {
            steps {
                // 'sh' executes a shell command on the agent
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }
}
