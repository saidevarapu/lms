pipeline {
    agent any

    stages {
        stage('LMS-Code-Analysis') {
            steps {
                echo 'Sonar Analysis'
                sh 'cd webapp && sudo docker run --rm -e SONAR_HOST_URL="http://100.26.138.77/:9000" -v ".:/usr/src" -e SONAR_TOKEN="sqp_0ef4d9ff5845b10f00539292a543dadd07c3b4e8" sonarsource/sonar-scanner-cli -Dsonar.projectKey=lms'
                echo 'Analysis Completed'
            }
        }   
    }   
}