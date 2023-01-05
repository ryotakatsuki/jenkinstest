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
      }
    }
  }
}
