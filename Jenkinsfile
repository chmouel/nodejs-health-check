@Library('github.com/chmouel/osio-pipeline@jr') _


osio {
  config runtime: 'node'

  ci {
    def res = processTemplate()
    build resources: res
  }

  cd {
    def res = processTemplate(params: [
      RELEASE_VERSION: "1.0.${env.BUILD_NUMBER}"
    ])

    build resources: res
    deploy resources: res, env: 'stage'
    deploy resources: res, env: 'run'
  }
}
