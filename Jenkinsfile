pipeline{
agent any

stages{

 stage('Checkout'){
  steps{
  checkout scm
  }}

  stage('Build'){
  steps{
  sh 'mvn clean package'
  }}

  stage('Run application'){
  steps{
  sh 'java -jar target/test1.jar'
  }}}

post {
always{
  archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
}}


}}