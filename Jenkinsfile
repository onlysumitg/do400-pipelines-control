node('nodejs') {
    stage('Checkout') {
        git branch: 'main',
            url: 'https://github.com/YOUR_GITHUB_USER/do400-pipelines-control'
    }
    stage('Backend Tests') {
        sh 'node ./backend/test.js'
    }
    stage('Frontend Tests') {
        sh 'node ./frontend/test.js'
    }
}