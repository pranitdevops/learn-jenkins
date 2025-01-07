pipeline{
   agent {
       node {
           label 'AGENT-1'
       }
   }
    options {
        // timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }

   stages {
       stage('build'){
           steps {
               echo "building"
           }     
       }

       stage('test'){
           steps {
               echo "testing"
           }
       }
       stage('deploy'){
         steps {
          echo "deploying"
         }

       }
      
   }
    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'this runs when pipeline is failed, used generally to send some alerts'
        }
        success{
            echo 'I will say Hello when pipeline is success'
        }
    }
}

