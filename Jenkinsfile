pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build completed'
      }
    }

    stage('test stages') {
      parallel {
        stage('test 2') {
          steps {
            echo 'running test2'
          }
        }

        stage('test1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        input(message: 'are you sure to deploy', ok: 'yes iam sure')
        echo 'deploy complited'
      }
    }

    stage('notify for new build') {
      steps {
        echo 'build successfully'
      }
    }

  }
}