pipeline {
    agent any
    //agent  = VM where the build will run
    // any = run on any availanle agent = run on current vm
    tools {
        maven 'maven_new'
    }   
    stages {
        stage('Checkout code from Github') {
            steps {
                 git branch: 'master', url: 'https://github.com/pappuhedaoo244/DevOpsCodeDemo.git'
            }
        }
        stage('Compile the code') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Review the code') {
            steps {
                sh 'mvn pmd:pmd'
            }
        }
        stage('Test the code') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package the code') {
            steps {
                sh 'mvn package'
            }
        }  
    }
}