pipeline {
  agent {
    label "ec2"
    }
  stages{
    stage("Verify tooling"){
      steps {
        sh '''
          sudo docker info
          sudo docker version
          sudo docker-compose version
          curl --version
          jq --version
        '''
      }
    }
    stage('Prune docker'){
      steps {
        sh '''
          sudo docker system prune -f -a
        '''
      }
    }
    stage('Start test container') {
      steps {
        sh '''
          sudo docker-compose -f docker-compose-test.yml up -d --no-color --wait
          sudo docker ps
        '''
      }
    }
    stage('Clean'){
      steps {
        sh '''
          sudo docker system prune -f -a
        '''
      }
    }
  }
}