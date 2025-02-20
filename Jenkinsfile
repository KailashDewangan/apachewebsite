pipeline{
  agent any 
  stages {
    stage(clone Repository') {
          steps {
            git 'https://github.com/KailashDewangan/apachewebsite.git'
          }
          }
          stage('Install Apache'){
            steps { 
              sh'''
              sudo apt update
              sudo apt install apache2 -y
              '''
            }
          }
          stage('Deploy Application'){
            steps{
              sh'''
              sudo rm -rf/var/www/html/*
              sudo cp -r * /var/www/html/
              sudo systemctl restart apache2
              '''
            }
          }
          }
          }
