pipeline {
    agent any
    stages {

        stage('testing pipeline'){
          steps{
		    echo 'test1'
                sh """
                ssh root@192.169.0.158
                cd /var/www/demoapp
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




