pipeline {
    agent any

        stages {
 
            stage ('test') {
                steps {
                    sh "mvn clean compile test"
                }
            }

            stage ('Build application') {
                steps {
                    sh "mvn -f pom.xml clean install -Dmaven.test.skip=true"   
                }
            }
  
            stage ('Production Phase') {
                steps {
                 echo "Pasando a produccion"
                }

            }
        }
}
