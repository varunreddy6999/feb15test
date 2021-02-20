pipeline {
    
  parameters {
    booleanParam(name: 'SAVE', defaultValue: false)
  }

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
        archiveArtifacts artifacts: "*.zip"
      }
    }
    stage('save'){
      when { expression { return params.SAVE } }
      steps {
        sh """#/bin/bash
           echo "saving done"
        """              
      }
    }
  }
}
