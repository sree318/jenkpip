pipeline {
    agent any
    stages {
        stage('Build Step') {
            steps { 
                bat 'javac pip.java'
            }
             post {
                always {
                    echo "configuring build step"
                }
                 success {
                    echo "Build step ran successfuly"
                }
            }
        }
        stage('Run Step') {
            steps { 
                bat 'java pip'
            }
             post {
                always {
                    echo "running java program"
                }
                 success {
                    echo "Program ran successfully"
                }
            }
        }
    }
    post {
        always {
            echo "This block always runs."
        }
        changed {
            echo "This block runs when the current status is different than the previous one."
        }
        fixed {
            echo "This block runs when the current status is success and the previous one was failed or unstable."
        }
        regression {
            echo "This block runs when the current status is anything except success but the previous one was successful."
        }
        unstable {
            echo "This block runs if the current status is marked unstable."
        }
        aborted {
            echo "This block runs when the build process is aborted."
        }
        failure {
            echo "This block runs when the build is failed."
        }
        success {
            echo "This block runs when the build is succeeded."
        }
        unsuccessful {
            echo "This block runs when the current status is anything except success."
        }
        cleanup {
            echo "This block always runs after other conditions are evaluated."
        }
    }
}
