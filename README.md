# AWSBeanstalkDeploymentLock

A configuration file for your amazon elastic beanstalk that automatically sets up a deployment lock while deploying. So you can check for this lockfile to pause your cronjob or display a warning on your server.

## Installation

Just download the source code and copy the `deploy-lock.config` into your `.ebextensions` folder. The final path may be `your-app-root/.ebextensions/deploy-lock.config`.

Everything should work out of the box.

## Usage

In a bash script you can use:

    if [ ! -f /opt/elasticbeanstalk/support/.deployment-in-progress ]; then
        // Do something only when no deployment is running
    fi