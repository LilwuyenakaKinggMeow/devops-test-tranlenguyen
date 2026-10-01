pipeline {


    agent any


    environment {

        PROJECT = "devops-test-nguyen"

        BRANCH = "main"

        URL = "https://devops-test-tranlenguyen.vercel.app"

    }


    stages {


        stage('Checkout') {


            steps {

                echo "Checkout source from GitHub"

            }

        }



        stage('Install Dependencies') {


            steps {

                echo "No dependencies required"

            }

        }




        stage('Build') {


            steps {

                echo "Checking website files..."

                sh 'ls -la'

            }

        }




        stage('Deploy') {


            steps {


                echo "Deploy website to Vercel"


                sh '''

                vercel --prod --yes

                '''


            }

        }


    }



    post {


        success {


            echo """

            ✅ DEPLOY SUCCESS

            Project: ${PROJECT}

            Branch: ${BRANCH}

            URL: ${URL}

            """


        }



        failure {


            echo """

            ❌ DEPLOY FAILED

            Project: ${PROJECT}

            Branch: ${BRANCH}

            Please check Jenkins.

            """

        }


    }


}