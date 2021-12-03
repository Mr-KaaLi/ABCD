pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                    echo "Hello"
            ''' 
      }
    }
    

    stage ('Build') {
      steps {
      sh 'echo "clean package" '
       }
    }
    
    stage ('Deploy-To-Tomcat') {
            steps {
           sshagent(['tomcat']) {
                sh 'echo "Hi"'
              }      
           }       
    }

    
  }
}
