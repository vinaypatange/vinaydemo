node {

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {

        sh 'tar -cvf demo.tar.gz ../demo'

        sh 'scp -r demo.tar.gz  ubuntu@3.86.161.73:/home/ubuntu'

        sh 'ssh -o StrictHostKeyChecking=No ubuntu@3.86.161.73 tar -xvf /home/ubuntu/demo.tar.gz'

        sh 'ssh -o StrictHostKeyChecking=No ubuntu@3.86.161.73 /home/ubuntu/demo/setup.sh'
  
           
    }
        
}
