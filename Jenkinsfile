node {
    stage ('Checkout') {
        checkout scm
    }

    withCredentials([string(credentialsId: 'swaggerhub-api-key', variable: 'APIKEY')]) {
        echo "APIKEY: ${APIKEY}"
        sh "sh toSwaggerHub.sh ${APIKEY} ${env.APIVERSION} ${env.OASVERSION} ${env.ISPRIVATE} ${env.OWNER}"
    }
}
