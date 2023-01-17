properties([
  parameters([
    string(name: "mybranch", description: "branch to use"),
  ])
])

pipeline {
  agent any
    
  stages {
    stage('build') {
      steps {
        sh 'echo Hello World!'
        script {
          withCredentials([string(credentialsId: 'newrelic-api-key', variable: 'TOKEN')]) {
    sh '''
      set +x
      curl -H "Token: $TOKEN" http://demo7287122.mockable.io/
    '''
  }
        }
      }
    }
  }
}
