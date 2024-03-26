pipeline{
    agent any
    environment {
    FIREBASE_DEPLOY_TOKEN = credentials('Firebase-Token')
    }

 stages{
       
        stage('Testing Environment'){
            steps{
            sh 'firebase deploy -P final-test-bf28d --token "$FIREBASE_DEPLOY_TOKEN"'
            
            }
        } 
        stage('Staging Environment'){
            steps{

          sh 'firebase deploy -P final-stage-200bb --token "$FIREBASE_DEPLOY_TOKEN"'

         

             echo  'Building'
            }
        } 
        stage('Production Environment'){
            steps{
            sh 'firebase deploy -P final-production-cbc00 --token "$FIREBASE_DEPLOY_TOKEN"'
            echo 'Production'
            }
        } 
    }

}
