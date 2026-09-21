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


pipeline {
    agent any

    stages {
        stage('诊断环境') {
            steps {
                sh '''
                    echo "=== 系统信息 ==="
                    cat /etc/os-release | head -3
                    echo "=== 查找 python ==="
                    ls /usr/bin/ | grep -i python || echo "无 python"
                    which python python3 python2 2>/dev/null || echo "python 都不在 PATH"
                    echo "=== 可用工具 ==="
                    which git curl wget sh bash java node npm 2>/dev/null
                    echo "=== 包管理器 ==="
                    which apt apt-get yum apk 2>/dev/null
                '''
            }
        }
    }
}
