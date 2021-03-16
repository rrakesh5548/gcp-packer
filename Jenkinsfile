pipeline {
  
   agent  any
  
    stages {
        stage('checkout') {
            steps {
                 script {
                        dir("gcp-packer")
                        {
                            "https://github.com/ishaqmdgcp/gcp-packer.git"
                        }
                    }
                }
            }

         //stage('packer inspect') {
           // steps {
             //  dir("") 
               // {
                //sh 'packer inspect aws.json'
            //}
        //}
    //}

  }
}
