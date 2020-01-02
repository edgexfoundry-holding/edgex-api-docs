node {
    stage ('Checkout') {
        checkout scm
    }

    stage ('Post document to SwaggerHub'){
        script {
            sh "sh toSwaggerHub.sh ${env.APIKEY} ${env.APIVERSION} ${env.OASVERSION} ${env.ISPRIVATE} ${env.OWNER}"
        }
    }
}
