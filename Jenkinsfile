pipeline {
    agent any
    stages {

        stage('testing pipeline'){
          steps{
		    echo 'test1'
                sh """
                ssh -ttT root@192.168.0.158
                . .env/bin/activate
                if [[ -f preinstall.txt ]]; then
                pip install -r preinstall.txt
                fi
                pip install -r preinstall.txt
                ./manage.py test --noinput
                """
                }
        }
        stage('second testing pipeline'){
          steps{
		    echo 'test2'
                sh 'rm -rf windows'
                sh 'mkdir windows1'
                sh 'touch windows1/test.txt'
                }
        }

}
}




