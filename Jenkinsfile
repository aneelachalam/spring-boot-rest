pipeline {
     agent any
     stages {
         stage('Build') {
             when {
               branch 'POD-6-branch'
             }
             steps {
                 echo 'Building...'
             }
             
         }
         stage('Deploy - Staging') {
             
             steps {
                 echo 'Deploying to Staging from jenkins....,,'
             }
             post {
                 always {
                     jiraSendBuildInfo site : 'pod-wipro.atlassian.net'}
             }
         }
        
        
     }
 }
