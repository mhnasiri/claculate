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
            echo '''
                ${currentBild.fullDisplayName} your build compalted.${env.BUILD_URL}

            '''
        }
    }
}