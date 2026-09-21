// pipeline {
//     agent any

//     stages {
//         stage('检出代码') {
//             steps {
//                 echo "当前分支: ${env.GIT_BRANCH}"
//                 echo "提交记录: ${env.GIT_COMMIT}"
//             }
//         }

//         stage('检查环境') {
//             steps {
//                 sh 'python3 --version'
//             }
//         }

//         stage('运行测试') {
//             steps {
//                 sh 'python3 demo.py'
//             }
//         }
//     }

//     post {
//         success {
//             echo '构建成功'
//         }
//         failure {
//             echo '构建失败'
//         }
//         always {
//             echo '流程结束'
//         }
//     }
// }


// pipeline {
//     agent any

//     stages {
//         stage('检出信息') {
//             steps {
//                 echo "分支: ${env.GIT_BRANCH}"
//                 echo "提交: ${env.GIT_COMMIT}"
//             }
//         }

//         stage('读取文件') {
//             steps {
//                 sh 'cat demo.py'
//             }
//         }
//     }

//     post {
//         success { echo '构建成功' }
//         failure { echo '构建失败' }
//     }
// }


pipeline {
    agent any
    stages {
        stage('时间检查') {
            steps {
                sh 'date; cat /etc/timezone 2>/dev/null || echo "无 timezone 文件"'
            }
        }
    }
}
