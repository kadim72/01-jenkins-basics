stages {
    stage('Parallel Execution') {
        steps {
            parallel (
                "Setup": {
                    echo "setup ..."
                    sh 'sleep 30'
                },
                "Test": {
                    echo "test ..."
                    sh 'sleep 30'
                    }
                }
            )
        }
    }
}
