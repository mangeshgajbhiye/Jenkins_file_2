pipeline {

      agent any

      stages {

           stage ('Checkout') {

              steps {
                checkout scm
              }
           }

           stage ('Build') {

             steps {
                sh '/home/mangesh/Software/apache-maven-3.6.1/bin/mvn install'
             }
           }
         
           stage (' Deploy') {

             steps {

               sh 'sshpass -p "QAserver" scp target/Jhava.war QAserver@172.17.0.2:/home/QAserver/Teast/parameter'
             }
           }
      }
}
