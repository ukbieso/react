node {
       stage('Checkout'){
          checkout scm
       }
       stage('Test'){
         env.NODE_ENV = "test"

         print "Environment will be : ${env.NODE_ENV}"

         sh 'node -v'
         sh 'npm install' 
         sh 'npm build'
              
       }
       stage('Build Docker'){

            echo 'docker build stage'
       }
       stage('Deploy'){

         echo 'Push to Repo'
         
         echo 'ssh to web server and tell it to pull new image'
       }

       stage('Cleanup'){
       echo  'cleanup stage'
       }
 }
