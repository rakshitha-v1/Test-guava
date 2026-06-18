pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git 'https://github.com/rakshitha-v1/Test-guava.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean install'
      }
    }
    stage('Create Source FIle'){
      steps{
        sh 'echo "This content will be copied" > source.txt'
      }
    }
    stage('Run Application'){
      steps{
        sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
      }
    }
  }
}
