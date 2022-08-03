pipeline{
    agent{
            node { 
                label "built-in"
                customWorkspace "/media/project1"
            }
            }
    stages{
        stage ('master-branch'){
            steps {
                sh "rm -rf /media/project1/*"
                sh "chmod -R 777 /media/project1/new-app"
                sh "docker cp /media/project1/new-app/index.html 7887a5bd5514:/usr/local/apache2/htdocs/"
            }
        }
    }
}

