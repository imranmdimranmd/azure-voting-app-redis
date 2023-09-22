pipeline {
    agent any

    stages {
        stage('Verified Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Good Bye') {
            steps {
                sh 'docker images -a'
            }
        }
        // stage('Good Bye') {
        //     steps {
        //         powershell 'Write-Output "hello from powershell"'
        //     }
        // }
        
    }
}
