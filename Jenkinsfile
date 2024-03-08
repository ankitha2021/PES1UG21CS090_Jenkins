pipeline{
    agent any
    stages{
        stage('build'){
            steps {
                build 'PES1UG21CS090-1'
                sh 'g++ prgm2.cpp -o output'
            }

        }
        stage('test'){
            steps{
                sh './output'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
            failure{
                error 'pipeline failed'
            }
    }
}
