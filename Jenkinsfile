def gv

pipeline {
  agent any 
    stages {
      stage("init") {
        steps {
          script {
            gv = load "script.groovy"
          }
        }
      }

      stage("build") {
        steps {
          script {
            gv.buildApp()
          }
        }
      }

      stage("test") {
        steps {
          echo "testing the application ...."
        }
      }

      stage("deploy") {
        steps {
          echo "deploying the application ...."
        }
      }
    }
}
