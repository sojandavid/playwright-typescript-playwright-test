pipeline {
   // agent { docker { image 'mcr.microsoft.com/playwright:v1.48.1-noble' } }
   options {
        buildDiscarder logRotator(numToKeepStr: '2', artifactNumToKeepStr: '2')
   }

   // environment {
   //          PATH = "/usr/local/bin/npm"
   // }

   tools {
      nodejs "nodejs"
   }

   agent any
   
   stages {
      stage('Playwright Test') {
         steps {
            // sh 'npm ci'
            // sh 'export npm_config_ENV="qa"'
            // sh 'npm install -D @playwright/test@latest'
            sh 'export npm_config_ENV="qa"; npm run test:serial'
      }
      }
   }
}