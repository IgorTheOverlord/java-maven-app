#!/usr/bin/env groovy

pipeline {
  agent none
  stages {
    stage('test') {
      steps {
        script {
          echo 'Testing the app...'
          echo "Executing pipeline for branch ${env.BRANCH_NAME}"
        }
      }
    }
    stage('build') {
      when {
        expression {
          "${env.BRANCH_NAME}" == 'main'
        }
      }
      steps {
        script {
          echo 'Building the app...'
          echo 'Bla-bla-bla'
        }
      }
    }
    stage('deploy') {
      when {
        expression {
          "${env.BRANCH_NAME}" == 'main'
        }
      }
      steps {
        script {
          echo 'Deploying the app...'
        }
      }
    }
  }
}
//asd
