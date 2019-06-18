pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "./gradlew compileJava"
               }
          }
          stage("Unit test") {
               steps {
                    sh "./gradlew test"
               }
          }
     
    
stage("Package") {
     steps {
          sh "./gradlew build"
     }
}

stage("Docker build") {
     steps {
      
          sh "docker build -t ssabhishek/calculator_1 ."
     }
}

stage("Docker push") {
     steps {
   sh "docker login -u ssabhishek -p abhi@671"

sh "docker push ssabhishek/calculator_1"
     }
}
stage("Deploy to staging") {
     steps {
 
          sh "docker run -d -p 8765:8080 --name calculator_1 ssabhishek/calculator_1"
     }
}

     }
  post {
     always {
          echo "Build Success"
     }
}
}
