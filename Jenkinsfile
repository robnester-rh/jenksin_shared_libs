#!/usr/bin/env groovy
library "github.com/robnester-rh/jenkins_shared_libs@devel@${params.branch}"

@Library("github.com/robnester-rh/jenkins_shared_libs@devel") _
import org.centos.Utils

def utils = new Utils()

def myWord = 'snake'

node(''){
    stage('check params'){
        echo params.branch

        echo "this is devel branch"

        daFoo {
            word = myWord
        }

        utils.makeItBump(myWord)

    }
}

