pipeline {
    agent any 
    stages {
        stage('Checkout'){
            steps{
                sh '''
                cd /home/ec2-user/.jenkins/workspace/Headless_testing/
                deleteDir()
                '''
            }
        }
        stage('Npm install'){
            steps{
                sh '''
                cd /home/ec2-user/.jenkins/workspace/Headless_testing/RideShare
                npm i
                '''
            }
        }
        stage('Test'){
            steps{
                sh '''
                cd /home/ec2-user/.jenkins/workspace/Headless_testing/RideShare
                npm run test-headless
                '''
            }
        }
        // stage('Build') { 
        //   steps {
        //         sh '''
        //         cd /home/ec2-user/.jenkins/workspace/Headless_testing/RideShare
        //         ng build
        //         '''
        //   }
        // }
        // stage('Deploy'){
        //     steps{
        //         sh '''
        //         cd /home/ec2-user/.jenkins/workspace/Headless_testing/RideShare
        //          aws2 s3 cp --recursive ./dist s3://Headless_testing/angular
        //         '''
        //     }
        // }
    }
}