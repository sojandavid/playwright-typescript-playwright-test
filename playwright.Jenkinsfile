pipeline {
   // agent { docker { image 'mcr.microsoft.com/playwright:v1.48.1-noble' } }
   options {
        buildDiscarder logRotator(numToKeepStr: '2', artifactNumToKeepStr: '2')
   }

   agent any
   
   stages {
      stage('Playwright Test') {
         steps {
            sh '/usr/local/bin/npm'
            sh 'npm ci'
            sh 'npx playwright test Login.test.ts --project=Chrome'
         }
      }
   }
}