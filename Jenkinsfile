pipeline {
    agent any
    
    environment {
    SVC_ACCOUNT_KEY = credentials('terraform-auth')
  }
     
    stages {
        stage ('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/ishaqmdgcp/gcp-packer.git'
            }
        }
        
        stage('Set packer path') {
            steps {
                //script {
                    //def tfHome = tool name: 'Packer'
                  //  env.PATH = "${tfHome}:${env.PATH}"
                //}
                sh 'echo $SVC_ACCOUNT_KEY | base64 -d > ./terraform.json'
		        sh 'pwd'
                sh 'packer --version'               
               
            }
        }
        
        stage('packer inspect') {
           steps {
               
                sh 'packer inspect packer.json'
            }
    }
        stage('packer build') {
           steps {
               
                sh 'packer build packer.json'
            }
    }
}
}
