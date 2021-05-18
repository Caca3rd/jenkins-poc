pipeline {
    agent any
    stages {
        stage("Checkout"){
            steps {
                script {
                    sh 'env | sort '
                    echo "${env.BRANCH_NAME}"
                    echo "${env.CHANGE_ID}"
                }
            }
        }
    }
}