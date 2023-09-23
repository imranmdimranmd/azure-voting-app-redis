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
                sh "sudo docker run -v /var/run/docker.sock:/var/run/docker.sock -v /home/ec2-user:/imran --privileged=true aquasec/trivy image -f json -o /imran/hospitals.json jenkins"
            }
        }
        // stage('Good Bye') {
        //     steps {
        //         powershell 'Write-Output "hello from powershell"'
        //     }
        // }
        
    }
}
