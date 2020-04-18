pipeline{
    agent any
    stages{
        stage('Clean Test'){
            steps{
                sh 'mvn clean test'
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