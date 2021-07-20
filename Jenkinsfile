pipeline {
  agent {
    label 'master'
  }

  stages {
    stage('Build') {
      steps {
        echo "BUILD_NUMBER=${env.BUILD_NUMBER}"
        echo "BRANCH_NAME=${env.BRANCH_NAME}"
        echo 'Cleaning Workspace...'
        echo "Branch Name: ${params.branch}"
        bat "mvn clean"
      }
    }

    stage('Test') {
      steps {
        echo 'Test....'
        bat "mvn test"
      }
    }
    stage('Install') {

      steps {

        echo 'install'
        bat "mvn install "
      }

    }
  }

}

        


    


