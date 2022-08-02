pipeline {
  agent any
  stages {
    stage('stage 1') {
      steps {
        git(url: 'https://github.com/Ruchika-Munde/pipeline-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('stage 2') {
      steps {
        sh '''sudo apt-get install apache2 -y
sudo service apache2 start'''
      }
    }

    stage('stage 3') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}