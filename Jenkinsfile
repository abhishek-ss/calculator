pipeline {
 agent any
 stages {
 stage(“Compile”) {
 steps {
 sh './gradlew compileJava'
 }
 }
 stage(“unit test”) {
 steps {
 sh “./gradlew test”
 }
 }
 }
}
