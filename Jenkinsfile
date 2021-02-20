pipeline {

  agent {
    label 'master'
  }
  
  stages {
    stage('build') {
      steps {
        sh """#!/bin/bash
           ls
        """
      }
    }
    stage('package') {
      steps {
        sh """#!/bin/bash
           tar -cvzf holly.zip hollywood
        """
      }
        archiveArtifacts artifacts: "*.zip"
    }
  }
}
