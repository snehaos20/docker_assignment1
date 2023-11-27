pipeline {
    agent {
    label{
        label "built-in"
        customWorkspace "/mnt/cloneProject"
    }
    }
    
    stages  {
        stage("getting git repository"){
            steps {
                echo "clone project"
                sh "rm -rf *"
                
            }
        }
        
    }
}
