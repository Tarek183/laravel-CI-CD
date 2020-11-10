pipeline {
 agent 
 stages {
        stage("Build") {
            steps {
                bat 'php --version'
                bat 'composer install'
                bat 'composer --version'
                bat 'copy .env.example .env'
                bat 'php artisan key:generate'
            }
        }
        stage("Unit test") {
            steps {
                bat 'php artisan test'
            }
        }
  }
}
