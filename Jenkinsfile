pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
        parameters {
            booleanParam(name: "RUN_FRONTEND_TESTS", defaultValue: false)
        }
    stages {
              stage('Run Tests') {
                  stages {
                      stage('Backend Tests') {
                        input {
                            message "Continue?"
                        }
                          steps {
                              sh 'node ./backend/test.js'
                          }
                      }
                      stage('Frontend Tests') {
                          when { expression { params.RUN_FRONTEND_TESTS } }

                          steps {
                              sh 'node ./frontend/test.js'
                          }
                      }
                                     stage('FINAL ECHO') {

                                                steps {
                                                    echo "FINAL ECHO>>"
                                                }
                                            }
                  }
              }
              stage('Run ECHO 2>>>>>>>') {
                   steps {
                                                                  echo "FINAL ECHO>>"
                                                              }}

    }
}