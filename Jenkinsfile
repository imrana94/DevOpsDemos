pipeline
    agent any
stages {
  stage("run froentend") {
    steps {
         echo "executing yarn..."
      Nodejs("Node-16.17") {
          sh "yarn install"
      }
    }
  }
  stage("run backend") {
    steps {
      echo "executing gradle..."
      withGradle() {
        sh "./gradlew -v"
      }
     }
    }
  }
}
