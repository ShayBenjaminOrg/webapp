pipeline {
    agent any 
    
    options { 
        timestamps()
    }
    environment {
        PlayGround = "${env.WORKSPACE}/playground/${env.BUILD_NUMBER}"
    }
    
    stages {
        stage('Clone the repo') {
            steps {
                //ansiColor('xterm'){
                    
                echo 'GIT_COMMIT : $GIT_COMMIT'
                echo 'GIT_BRANCH : $GIT_BRANCH'
                    echo "PlayGround : '$PlayGround'"
                    echo "BUILD_NUMBER : '$BUILD_NUMBER'"
                    echo "BUILD_ID : '$BUILD_ID'"
                    echo "BUILD_DISPLAY_NAME : '${BUILD_DISPLAY_NAME}'"
                    echo "JOB_NAME : '${JOB_NAME}'"
                    echo "JOB_BASE_NAME : '${JOB_BASE_NAME}'"
                    echo "BUILD_TAG : '${BUILD_TAG}'"
                    echo "EXECUTOR_NUMBER : '${EXECUTOR_NUMBER}'"
                    echo "NODE_NAME : '${NODE_NAME}'"
                    echo "NODE_LABELS : '${NODE_LABELS}'"
                    echo "WORKSPACE : '${WORKSPACE}'"
                    echo "JENKINS_HOME : '${JENKINS_HOME}'"
                    sh 'printenv | grep GIT'
                    sh 'whoami'
                    sh "mkdir -p '$PlayGround'"
                    sh "cd '$PlayGround'"
                    echo 'clone the app repo'
              //  }
            }
        }
    }
}
