#!/usr/bin/groovy

@Library('github.com/chmouel/osio-pipeline-helpers@master')

def canaryVersion = "1.0.${env.BUILD_NUMBER}"
def utils = new io.fabric8.Utils()
def stashName = "buildpod.${env.JOB_NAME}.${env.BUILD_NUMBER}".replace('-', '_').replace('/', '_')
def envStage = utils.environmentNamespace('stage')
def envProd = utils.environmentNamespace('run')
def setupScript = null

node {
  checkout scm

}
