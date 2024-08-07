pipeline{
  agent any

  stages{
    stage('build'){
      steps{
        echo "Build application ...${}"
        echo "Variable d'environnement -> BRANCH_NAME: ${ env.BRANCH_NAME}"
        echo "Variable d'environnement -> BRANCH_IS_PRIMARY: ${ env.BRANCH_IS_PRIMARY}"
        echo "Variable d'environnement -> CI: ${ env.CI}"
        echo "Variable d'environnement -> BUILD_NUMBER: ${ env.BUILD_NUMBER}"
        echo "Variable d'environnement -> JENKINS_URL: ${ env.JENKINS_URL}"
      }
    }
    
    stage('tests'){
      steps{
        echo "Exécution tests ..."
      }
    }

    stage('deployment'){
      steps{
        echo "Deploy application ..."
      }
    }

  }
}