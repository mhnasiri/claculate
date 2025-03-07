pipeline{
    agent any
    stages{
        stage('compile'){
            steps{
                sh '''
                    python3 test2.py
                '''
            }
        }
    }
    post{
        always{
             
            echo "Build result: ${currentBuild.result}"
            echo "Build duration: ${currentBuild.duration} ms"
            echo "${currentBuild.fullDisplayName}"
            echo "${env.BUILD_URL}"
            
        }
    }
}