pipeline   {
    agent any 
    stages {
        stage('codeScan'){
            steps{
                sh 'trivy fs . -o result.html'
                sh 'cat result.html'
            }
        }
        stage('dockerLogin'){
            steps{
                sh'aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 440744242159.dkr.ecr.us-east-1.amazonaws.com'
            }
        }
        stage('dockerImageBuild'){
            steps{
                sh 'docker build -t devops .'
            }
        }
        stage('dockerImageTag'){
            steps{
                sh 'docker tag devops:latest 440744242159.dkr.ecr.us-east-1.amazonaws.com/devops:v.4'
            }
        }


        stage('pushImage'){
            steps{
                sh 'docker push 440744242159.dkr.ecr.us-east-1.amazonaws.com/devops:v.4'
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


