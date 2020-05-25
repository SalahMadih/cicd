pipeline {
     agent any
     tools {nodejs "nodejs"}    
     stages {
          stage('Prepare') {
               steps {
                   echo 'install g yarn"'
                     sh "npm install -g yarn"

               }
            
          }
           stage('Initantiate') {
             steps {
                echo 'Initantiate'
             }
          }
          stage("Install dependencies") {
               steps {
                   echo 'Install..'
                    sh 'npm install'

               }
          }
          stage("Build") {
               steps {
                    echo 'Building..'
                    sh 'npm build'
               }
          }

            stage("Unit test") {
               steps {
                    echo 'Testing..'
                    sh 'yarn run test --watchAll=false'
               }
          }
     }
}
