pipeline{
  agent {
    docker {
      image:'node:22-alpine' //image node verion 22-alpine prise sur dockerhub

    }
  }


  stages {
    stage('build'){
      steps {
        sh 'npm -v'
      }
    }
    
    stage('tests'){
      steps {
        echo "Exécution tests ..."
      }
    }

    stage('deployment'){
      steps {
        echo "Deploy application ..."
      }
    }

  }

  post {
    always {
      echo 'always !'
    }

    success {
      echo 'success !'
    }
  }
}