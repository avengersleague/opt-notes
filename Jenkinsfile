def isNeedRollback = false

pipeline {
    agent any

    environment {
        deployNode = "10.200.102.74"
        deployDir = "/worker/service/front/opt-notes"
        publicUrl = "http://qc.can-dao.com:6787"
    }

    post {
        failure {
            script {
              if(isNeedRollback){
                  echo "代码需要回滚"
              } else {
                  echo "代码不需要回滚"
              }
            }
        }

        success {
            script {
                echo "部署成功"
			      }
        }
    }

    stages {
        stage('拉取/更新代码') {
            steps {
                echo "拉取/更新代码"
            }
        }

        stage('构建/打包项目') {
            steps {
               echo "构建/打包项目"
               sh "source /etc/profile && gitbook install && gitbook build"
            }
        }

        stage('发布项目') {
          steps {
            script {
              echo "发布项目"
              sh "cd _book/ && tar -cvzf ROOT-opt-notes.tar.gz * --exclude=\".gitignore\" --exclude=\"Jenkinsfile\" --exclude=\"ROOT-opt-notes.tar.gz\""
              sh "ssh -o StrictHostKeyChecking=no ${deployNode} \"rm -rf ${deployDir}.tmp/ && mkdir -p ${deployDir}.tmp/\" "
              sh "scp -o StrictHostKeyChecking=no _book/ROOT-opt-notes.tar.gz ${deployNode}:${deployDir}.tmp/"
              sh "ssh -o StrictHostKeyChecking=no ${deployNode} \"tar -C ${deployDir}.tmp/ -zxvf ${deployDir}.tmp/ROOT-opt-notes.tar.gz && rm -rf ${deployDir}.tmp/ROOT-opt-notes.tar.gz \""
              sh "ssh -o StrictHostKeyChecking=no ${deployNode} \"rm -rf ${deployDir}.bak && mv ${deployDir} ${deployDir}.bak && mv ${deployDir}.tmp ${deployDir}/\" "
            }
          }
        }

        stage('检查是否正常部署') {
            steps {
                script {
                  def exitValue = sh(script: "curl ${publicUrl}", returnStatus: true)
                  echo "return exitValue :${exitValue}"
                  if(exitValue != 0){
                      echo "无法访问"
                      sh 'exit 1'
                  }
                }
            }
        }
    }
}
