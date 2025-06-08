pipeline{
  agent any
  tools{
    maven 'maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'master' url:'https://github.com/Harini-hyd/fgradle.git'
      }
    }
    stage('Build'){
      steps{
        bat 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        bat 'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        bat 'java -jar target/maven6-0.0.1-SNAPSHOT.jar'
      }
    }
  }
}
