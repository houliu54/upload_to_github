pipeline{
    agent any
    stages{
        stage('autotest_pipeline'){
            steps{
                bat 'python pipeline_test.py'
            }
        }
         stage('show demo'){
            steps{
                bat 'show me.....'
            }  
        }
    }
    post{
        always{
            emailext body: '''<!DOCTYPE html>
            <html>
            <head>
            <meta charset="UTF-8">
            <title>构建邮箱</title>
            </head>
            <body leftmargin="8" marginwidth="0" topmargin="8" marginheight="4" offset="0">
              <h1>${JENKINS_URL}---中pipeline模块</h1>
            </body>
            </html>''', subject: 'pipeline_using', to: '2019106279@qq.com'
        }
    }
}
