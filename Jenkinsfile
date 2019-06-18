pipeline {
 agent any
 stages {
 stage(“Compile”) {
 steps {
 sh './gradlew compileJava'
 }
 }
 stage(“test”) {
 steps {
 sh “./gradlew test”
 }
 }
 }
