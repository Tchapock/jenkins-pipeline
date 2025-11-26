pipeline   {
    agent any 
    stages {
        stage('codeScan'){
            steps{
                sh 'trivy --version'
            }
        }
        stage('dockerImageBuild'){
            steps{
                sh 'docker -v'
            }
        }
        stage('pushImage'){
            steps{
                sh ' docker ps'
            }
        } 
    stage('test'){
        steps{
            sh 'echo "test"'
            sh 'ls'
            sh ' pwd'
            
        
        }
    }
    stage('create'){
        steps{
            sh 'touch text-$BUILD_ID'
        }
    
    }
    
    }
}