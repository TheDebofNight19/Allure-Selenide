pipeline{
    agent any
    stages{
        stage('Clean'){
            steps{
                bat 'mvn clean'
            }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
    }
    post{
        always{
            script{
                allure includeProperties:false,
                    jdk:'',
                    properties:[],
                    reportBuildPolicy:'ALWAYS',
                    results:[[path:'target/allure-results']]

                                }
                            }
                        }
                    }