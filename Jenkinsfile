pipeline {
    agent any
    stages {

        stage('testing pipeline'){
          steps{
		    echo 'test1'
                sh """
                cd /var/www/demoapp
                . .env/bin/activate
                if [[ -f preinstall.txt ]]; then
                pip install -r preinstall.txt
                fi
                pip install -r test.txt
                ./manage.py test --noinput
                """
                }
        }
        stage('second testing pipeline'){
          steps{
		    echo 'test2'
                sh 'rm -rf test2'
                sh 'mkdir windows'
                sh 'touch windows/test.txt'
                }
        }

}
}




