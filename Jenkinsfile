pipeline{
    tools{
        maven 'mymaven'
    }
    agent {
        label 'linux_node'
    }
    
    stages{
        
        stage(job1){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        
        stage('parallel stage execution') {
            
            parallel {
                
        stage('job2'){
            steps{
                sh 'mvn compile'
               
            }
        }
        stage('job3'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
}
        }
    }    
    
}
