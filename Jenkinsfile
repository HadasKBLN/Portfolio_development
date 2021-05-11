pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh ' docker-compose up --build -d'
            }
        }

        stage('Unit test'){
            steps {
                sh '''
                 sleep 15
                 docker exec flask pytest -v > testResult.txt 
                 ./test.sh
                 '''
            }
        }

        stage('Tagging'){
            steps{
                sh 'echo jj'

            }

        }

        stage('Publish'){
            steps{
                sh 'echo jj'
                
            }

        }


    }

    post{
        always{
            sh 'docker-compose down -v'
        }
    }
}