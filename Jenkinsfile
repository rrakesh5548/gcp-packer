pipeline {
    agent any
     
    stages {
        stage ('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/ishaqmdgcp/gcp-packer.git'
            }
        }
        
        stage('packer inspect') {
           steps {
               
                sh 'packer inspect packer.json'
            }
    }
}
}
