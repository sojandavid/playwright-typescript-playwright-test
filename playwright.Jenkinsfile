pipeline {
   agent { docker { image 'mcr.microsoft.com/playwright:v1.48.1-noble' } }
   stages {
      stage('Playwright Test') {
         steps {
            sh 'npm ci'
            sh 'npx playwright test Login.test.ts --project=Chrome'
         }
      }
   }
}