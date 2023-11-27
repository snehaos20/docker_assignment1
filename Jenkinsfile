pipeline {
    agent {
        label "built-in"
        customWorkspace "/mnt"
    }
    
    stages  {
        stage("getting git repository"){
            steps {
                rm -rf *
                git clone https://github.com/snehaos20/docker_assignment1.git -b Q123
                echo "clone completed"
                chmod -R 777 /mnt/Q123
                
            }
        }
        stage ("creating container"){
            steps {
                docker run -d --name server -p 80:80 httpd
                docker exec -it server bash
                docker cp /mnt/Q123/index.html server:/usr/local/apache2/htdocs
                
            }
        }
    }
}
