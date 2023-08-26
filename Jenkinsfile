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
        when {
          expression {
            BRANCH_NAME == 'main'
          }
        }
        steps {
          script {
            gv.buildApp()
          }
        }
      }

      stage("test") {
        steps {
          echo "testing the application .... 222"
          echo "Executing pipeline for $BRANCH_NAME"
        }
      }

      stage("deploy") {
        when {
          expression {
            BRANCH_NAME == 'main'
          }
        }
        steps {
          echo "deploying the application ...."
        }
      }
    }
}
