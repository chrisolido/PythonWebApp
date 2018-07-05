pipeline {
    agent any
    stages {

        stage('testing pipeline'){
          steps{
		    echo 'test1'
                sh """
                . .env/bin/activate
                if [[ -f requirements/preinstall.txt ]]; then
                pip install -r requirements/preinstall.txt
                fi
                pip install -r requirements/test.txt
                ./manage.py test --noinput
                """
                }
        }
        stage('second testing pipeline'){
          steps{
		    echo 'test2'
                sh 'rm -rf test2'
                sh 'mkdir test2'
                sh 'touch test2/test.txt'
                }
        }
                stage('third testing pipeline'){
          steps{
		    echo 'test3'
                sh 'rm -rf test3'
                sh 'mkdir test3'
                sh 'touch test3
                /test.txt'
                }
        }

}
}




