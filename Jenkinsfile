node {
    stage 'Initialize' {
        echo 'Initializing...'
        def node = tool name: 'Node-7.4.0', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
        env.PATH = "${nodeHome}/bin:${env.PATH}"
    }
    stage 'Checkout' {
        echo 'Checking version control...'
        checkout scm
    }
    stage 'Build' {
        echo 'Building dependencies...'
        sh 'npm i'
    }
    stage 'Test' {
        echo 'Testing...'
        sh 'npm test'
    }
}
