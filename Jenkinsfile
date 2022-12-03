pipeline {
  agent any
    
  tools {nodejs "nodejs"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SirineMben/frontCI']]])
        
      }
    }
    stage('install dependencies') {
      steps {
        //sh 'npm config ls'
        
         sh 'npm install'
      }
    }
    stage('test') {
      steps {
        //sh 'npm config ls'
        
         sh 'npm start'
      }
    }
      }
    }   
    
