pipeline {
  agent any
  stages {
    stage("run frontend") {
      steps {
        echo 'executing yarn 2'
        nodejs('Node-10.17') {
          sh 'yarn install'
        }
      }
    }
    stage("run backend") {
      steps {
        echo 'ececuting gradle'
        withGradle() {
          sh './gradlew -v'
        }
      }
    }
  }
}
