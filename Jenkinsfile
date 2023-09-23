pipeline {
    agent any

    stages {
        stage('Verified Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage("build image") {
            steps {
                sh """
                    cd azure-vote
                    ls
                    pwd
                    docker build -t imran/test:${env.BUILD_ID} .
                """
            }
        }
        stage('Good Bye') {
            steps {
                sh "docker run -v /var/run/docker.sock:/var/run/docker.sock -v /home/ec2-user:/imran --privileged=true aquasec/trivy image -f json -o /imran/hospitals.json httpd"
            }
        }
        // stage('Good Bye') {
        //     steps {
        //         powershell 'Write-Output "hello from powershell"'
        //     }
        // }
        
    }
}
