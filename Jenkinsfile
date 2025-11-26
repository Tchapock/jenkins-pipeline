pipeline   {
    agent any 
    stages {
        stage('clone'){
            steps{
                sh 'echo "clone"'
                sh 'uname -r'
                sh 'cat /etc/os-release'
            }
        } 
    stage('test'){
        steps{
            sh 'echo "test"'
        }
    }
    stage('create'){
        steps{
            sh 'touch text-$BUILD_ID'
        }
    
    }
    
    }
}