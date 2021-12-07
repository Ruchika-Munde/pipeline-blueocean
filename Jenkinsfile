pipeline {
  agent any
  stages {
    stage('Fetch code from Git') {
      steps {
        git(url: 'https://github.com/Ruchika-Munde/pipeline-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('Install and start apache') {
      steps {
        sh '''sudo apt-get install apache2 -y
sudo service apache2 start'''
      }
    }

    stage('Deploy code on apache') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}
