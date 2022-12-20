pipeline {
    agent any

  environment {
    // Adjust variables below
    IMAGE_NAME  = "docker.io/indryad/java-petclinicapp"

    // Do not edit variables below
    TAG         = sh (script: "date +%y%m%d%H%M", returnStdout: true).trim()
    DOCKERHUB_CREDENTIALS = credentials('dockerhub-cred')
  }

  stages {
    stage('Preparation') {
      steps {
        sh "echo App Version = $TAG"
      }
    }
