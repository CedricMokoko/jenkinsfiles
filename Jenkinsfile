pipeline{
  agent any

  // options{
    // timeout(time: 1, unit: "HOURS")
  // }

  triggers{
    //cron('* *  * * *')
    pollSCM('* * * * *')
  }
 

  //J'ai commenté pour pouvoir observer les triggers
  // parameters{
  //   string(name: 'NAME',  defaultValue: 'M. Jenkins', description: 'Qui est ce?')
  //   text(name: 'TEXT',  defaultValue: 'un text', description: 'Une description')
  //   booleanParam(name: 'TOGGLE',  defaultValue: true, description: 'True ou False')
  //   choice(name: 'CHOICE',  choices: ['un', 'deux', 'trois'], description: 'Liste')
  //   password(name: 'PASSWORD', description: 'Un mot de passe')
  // }

  environment{
    MY_VAR_STRING = 'une variable'
    MY_VAR_NUMBER = 123
  }
 
  stages{
    stage('build'){

      options{
        timestamps()
      }

      steps{
        echo "Build application ..."
        echo "Variable d'environnement native di Jenkins-> BRANCH_NAME: ${ env.BRANCH_NAME}"
        echo "Variable d'environnement native di Jenkins-> BRANCH_IS_PRIMARY: ${ env.BRANCH_IS_PRIMARY}"
        echo "Variable d'environnement native di Jenkins-> CI: ${ env.CI}"
        echo "Variable d'environnement native di Jenkins-> BUILD_NUMBER: ${ env.BUILD_NUMBER}"
        echo "Variable d'environnement native di Jenkins-> JENKINS_URL: ${ env.JENKINS_URL}"
        echo "Variable d'environnement custom -> MY_VAR_STRING: ${ env.MY_VAR_STRING}"
        echo "Variable d'environnement custom -> MY_VAR_NUMBER: ${ env.MY_VAR_NUMBER}"
        sh 'printenv'

        // echo "Mon parametre NAME: ${NAME}"
        // echo "Mon parametre TEXTE: ${TEXT}"
        // echo "Mon parametre TOGGLE: ${TOGGLE}"
        // echo "Mon parametre PASSWORD: ${PASSWORD}" //En prod il ne faut pas le faire, c'est pas une bonne pratique
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