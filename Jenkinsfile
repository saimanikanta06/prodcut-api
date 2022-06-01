pipeline {

  agent any
  
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "******mvn munit test case Executaion*************"
      }
    }

     stage('Deploy Development') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests -Pdev deploy -DmuleDeploy'
            }
    }
    
  }
}