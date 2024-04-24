//#!/usr/bin/env groovy

//@Library(value = "devops@master", changelog = false) _

//def AISERA_TAG = "UNKNOWN"

pipeline {
    agent any
    // options {
    //     skipDefaultCheckout(true)
    // }
    stages {
        stage('test') {
            steps {
                script {
                  echo "running..."
                  echo "running..."

                }
            }
        }      

        // stage('Checkout') {
        //     steps {
        //         script {
        //             myparams = configureBuildParameters()
        //             GIT_REPO_NAME = 'rag'
        //             def scmVars = aiseraCI.checkoutAiseraRepo(GIT_REPO_NAME, myparams.branch)
        //             AISERA_TAG = aiseraCI.generateTag(myparams.release, scmVars.GIT_COMMIT)
        //             IMAGE_NAME = GIT_REPO_NAME
        //             IMAGE_VERSION_TAG = myparams.branch.replaceAll("[^A-Za-z0-9]", "_")
        //         }
        //     }
        // }

        // stage('Build Docker Images') {
        //     environment {
        //         DOCKER_BUILDKIT = "1"
        //     }
        //     steps {
        //         script {
        //             withRegistryAccess('aws-dev') {
        //                 withCredentials([ usernamePassword(credentialsId: 'db7cd3c3-ea63-4889-b54e-040b8e012ab5', usernameVariable: 'JFROG_USER', passwordVariable: 'JFROG_PASSWORD') ]) {
        //                     PIP_EXTRA_INDEX_URL = 'https://${JFROG_USER}:${JFROG_PASSWORD}@aisera.jfrog.io/artifactory/api/pypi/ds-common/simple'
        //                     sh "docker build --build-arg PIP_EXTRA_INDEX_URL=${PIP_EXTRA_INDEX_URL} -t ${IMAGE_NAME}:${IMAGE_VERSION_TAG} -f docker/Dockerfile ."
        //                 }
        //             }
        //         }
        //     }
        // }

        // stage('Run unit tests') {
        //     steps {
        //         script {
        //             sh "docker run --rm --entrypoint ./entrypoints/tests/unit.sh ${IMAGE_NAME}:${IMAGE_VERSION_TAG}"
        //         }
        //     }
        // }

        // stage('CVE Scan') {
        //     steps {
        //         script {
        //             microserviceCI.cveScan(
        //                 GIT_REPO_NAME,
        //                 IMAGE_NAME,
        //                 IMAGE_VERSION_TAG
        //             )
        //         }
        //     }
        // }

        // stage('Push to ECR') {
        //     steps {
        //         script {
        //             withRegistryAccess('aws-dev') { registry ->
        //                 pushToRegistry(
        //                         "${IMAGE_NAME}:${IMAGE_VERSION_TAG}",
        //                         registry.imageName(IMAGE_NAME, AISERA_TAG)
        //                 )
        //             }
        //             aiseraCI.addTagAsArtifact(AISERA_TAG)
        //         }
        //     }
        // }

        // stage('Service Deployment') {
        //     steps {
        //         script {
        //             microserviceCI.deploy(
        //                 myparams.environment,
        //                 myparams.get('devops_branch', 'master'),
        //                 'llm-rag-rest-service',
        //                 AISERA_TAG,
        //                 true,
        //                 false
        //             )
        //         }
        //     }
        // }

    }

    // post {
    //     failure {
    //         emailext body: '''${SCRIPT, template="groovy-html.template"}''',
    //                 subject: "Jenkins Build ${currentBuild.currentResult}: Job ${env.JOB_NAME}",
    //                 to: 'polykarpos.meladianos@aisera.com',
    //                 mimeType: 'text/html'
    //     }
    // }
}
