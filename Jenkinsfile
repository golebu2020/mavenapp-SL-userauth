#!/usr/bin/env groovy

@Library('jenkins-shared-library')
def gv
// @Library('jenkins-shared-library')_

pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage ("init"){
            steps{
                script{
                    gv = load "script.groovy"
                }
            }
        }

        stage ("build jar"){
            steps{
                script{
                    buildJar()
                }
            }
        }

        stage ("build image"){
            steps{
                script{
                    buildImage "golebu2020/maven-repo:jma-4.0"
                }
            }
        }
        
        stage ("deploy"){
            steps{
                script{
                    gv.deployApp()
                }
            }
        }
    }
}