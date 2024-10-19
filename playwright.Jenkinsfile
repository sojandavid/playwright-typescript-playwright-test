pipeline {
   // agent { docker { image 'mcr.microsoft.com/playwright:v1.48.1-noble' } }
   options {
        buildDiscarder logRotator(numToKeepStr: '2', artifactNumToKeepStr: '2')
   }

   environment {
            PATH = "/usr/local/bin/npm"
    }

   agent any
   
   stages {
      stage('Playwright Test') {
         steps {
            sh 'npm ci'
            sh 'npx playwright test Login.test.ts --project=Chrome'
         }
      }
   }
}