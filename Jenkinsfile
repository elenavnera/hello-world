pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        git(url: 'git@github.com:elenavnera/hello-world.git', branch: 'master', changelog: true, poll: true)
      }
    }
    stage('stage 1-2') {
      steps {
        build(propagate: true, quietPeriod: 300, wait: true, job: 'Bamboo-poll')
      }
    }
  }
}