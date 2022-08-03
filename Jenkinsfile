pipeline{
    agent{
            node { 
                label "built-in"
                customWorkspace "/media/project2"
            }
            }
    stages{
        stage ('master-branch'){
            steps {
                sh "rm -rf /media/project2/*"
                sh "chmod -R 777 /media/project2/new-app"
                sh "docker cp /media/project2/new-app/index.html ae8b4d4ee4fe:/usr/local/apache2/htdocs/"
            }
        }
    }
}

