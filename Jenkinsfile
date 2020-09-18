pipeline {
     agent none

stages {
  stage ('STAGE 1') {
       agent {label 'C-node'}   
       steps {
               sh 'sleep 10'
  }
  }
  stage ('STAGE 2') {
       agent {label 'Java-node'}
       steps {
               sh 'sleep 10'
  }
  }
  stage ('STAGE 3') {
       agent {label 'Java-node'}
       steps {
               sh 'sleep 30'
  }
  }
  stage ('STAGE 4') {
       agent {label 'master'}
       steps {
               sh 'sleep 30'
  }
  }
}
}
