pipeline {
    agent {
        label 'java-node'
    }
    stages {
        stage ("Build stage"){
            steps {
                echo "Build stage  completed: "
            }
        }
        stage ("DEV deploy"){
            steps {
                echo " Deploy to dev completed  successfully:"
            }
        }
        stage ("STAGE deploy"){
            when {
                branch 'release/*'
            }
            steps{
                echo "Deploy to stage  completed"
            }
        }
        stage("Deploy to prod"){
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "Prasad Reddy"

            }
            steps {
                echo "Deploy to production: "
            }
        }
    }
}
