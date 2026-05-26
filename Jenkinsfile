pipeline { 
 
 agent any
  stages { 
 
  stage('Clone') { 
   steps { 
    git 'https://github.com/Harni20-ai/node-app.git' 
   } 
  } 
 
  stage('Install Dependencies') { 
   steps { 
    bat 'npm install' 
   } 
  } 
 
  stage('Run Application') { 
   steps { 
    bat 'node app.js' 
   } 
  } 
 
  stage('Run Tests') { 
   steps { 
    bat 'npm test' 
   } 
  } 
 
  stage('Build Docker Image') { 
   steps { 
    bat 'docker build -t 7 .' 
   } 
  } 
 
  stage('Run Docker Container') { 
   steps { 
    bat 'docker run -d -p 3000:3000 --name ci-container ci-node' 
   } 
  } 
 
 } 
 
} 