pipeline {
    agent any
    stages {
        stage("Checkout"){
            steps {
                checkout scm
            }
        }
        stage("Build"){
            steps {
                echo "in Build Stage"
                echo env.BRANCH_NAME
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                    sh "ret=`wc -l src/1.r` && echo $ret"
                    sh "exit 1"
                }
            }
        }
        stage("test"){
            steps{
                script{
                    cat src/1.r
                }
            }
        }
    }
}
