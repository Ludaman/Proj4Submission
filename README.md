# Jeff Choate's AWS developer project submission

This is my project submission for lesson 4.

## All images should be included in the screenshots directory

## Existing issues:
I was not able to get the reverse proxy working perfectly.  It is able to route traffic to the backend API, but not to the frontend; i would like assistance with the config file for that if able.

I was not able to get the ionic website to successfully call the cloud APIs; I am able to call them via CURL requests from my local machine as well as when I 'lubectl exec' into one of the K8 machines.  The error I get from the webpage says unknown error against the API call, but the API call works when I paste it directly in the browser.

## Deploy strategy

Each of the 4 projects have their own deployment pipelines to allow me to swap them out individually.  If there are ways to combine the travis-yaml, git repos, or deployment.yaml files I would love to know that.

## Accessing the webpage
Currently, as of 20210115, you can hit the reverse proxy via this URL: aa8f8595f95bb4202803e536c6a0dfd1-1235067813.us-west-1.elb.amazonaws.com:8080/api/v0 

I will keep that URL and K8 cluster up until 20210117 at noon PST.  

That URL will sucecssfully route you to the backend API, the frontend provides issues I was unable to troubleshoot and would love assistance with. 

## Security and password
I utilized the K8 secrets feature to set the environment variables for each of the pods, this allows me to manage the secure information directly without pushing that into any git repos or docker repos in the cloud.

