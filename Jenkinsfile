pipeline {
    agent any

        stages {
 
            stage ('test') {
                steps {
                    bat "mvn clean compile test"
                }
            }

            stage ('Build application') {
                steps {
                    bat "mvn -f pom.xml clean install -Dmaven.test.skip=true"   
                }
            }
  
            stage ('Production Phase') {
                steps {
                 echo "Pasando a produccion"
                }

            }
        }
}
