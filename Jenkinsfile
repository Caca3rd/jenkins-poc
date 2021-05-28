pipeline {
    agent any
    stages {
        stage("Checkout"){
            steps {
                echo "checkout"
            }
        }
        stage("Build"){
            steps {
                echo "in Build Stage"
                echo env.BRANCH_NAME
                script{
                    pwd
                    ls
                }
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                    sh "exit 1"
                }
            }
        }
        stage("test"){
            steps{
                script{
                    sh "cat src/1.r"
                }
            }
        }
    }
}
