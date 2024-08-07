pipeline{
  agent any

  environment{
    MY_VAR_STRING = 'une variable'
    MY_VAR_NUMBER = 123
  }

  stages{
    stage('build'){
      steps{
        echo "Build application ...${}"
        echo "Variable d'environnement native di Jenkins-> BRANCH_NAME: ${ env.BRANCH_NAME}"
        echo "Variable d'environnement native di Jenkins-> BRANCH_IS_PRIMARY: ${ env.BRANCH_IS_PRIMARY}"
        echo "Variable d'environnement native di Jenkins-> CI: ${ env.CI}"
        echo "Variable d'environnement native di Jenkins-> BUILD_NUMBER: ${ env.BUILD_NUMBER}"
        echo "Variable d'environnement native di Jenkins-> JENKINS_URL: ${ env.JENKINS_URL}"
        echo "Variable d'environnement custom -> MY_VAR_STRING: ${ env.MY_VAR_STRING}"
        echo "Variable d'environnement custom -> MY_VAR_NUMBER: ${ env.MY_VAR_NUMBER}"
        sh 'printenv'
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