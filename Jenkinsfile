pipeline   {
    agent any 
    stages {
        stage('clone'){
            steps{
                sh 'echo "clone"'
                sh 'uname -r'
                sh 'cat /etc/os-release'
                sh 'nproc'
            }
        } 
    stage('test'){
        steps{
            sh 'echo "test"'
            sh 'ls'
            sh 'pwd'
        
        }
    }
    stage('create'){
        steps{
            sh 'touch text-$BUILD_ID'
        }
    
    }
    
    }
}