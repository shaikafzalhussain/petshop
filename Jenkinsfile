// This is the simplest possible Declarative Pipeline.
// It focuses only on the initial build steps.
pipeline {
    // 1. AGENT: Defines where the pipeline will run. 
    // 'any' tells Jenkins to use any available worker node.
    agent any

    // 2. STAGES: Defines the sequence of work. 
    stages {
        stage('Application Build') {
            steps {
                // Checkout the code from your connected SCM (e.g., GitHub).
                echo 'Checking out source code...'
                checkout scm

                // Placeholder for your actual build command (e.g., compiling code).
                echo 'Starting the actual build process.'
                sh 'echo "Running build scripts here..."'
            }
        }
    }

    // 3. POST: Optional but good for cleanup.
    // The entire post section (and all its conditions) must be enclosed in one {} block.
    post {
        // The 'always' condition runs every time, successful or not.
        always {
            // Clean up the workspace on the agent after the job is finished.
            cleanWs()
            echo 'Build complete.'
        }
    }
}
