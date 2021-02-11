# Reproducible workflows

Prerequisites:
- [docker](../computing/more/docker.md)
- [local minikube environment](../computing/more/kubernetes.md)

To-do:
- Have a look at a simplified, but typical physics analysis workflow consisting of two phases
   - first writing the original datasets to a smaller format: [producer](http://opendata.cern.ch/record/12340) 
   - then running the actual analysis on this smaller format: [analyzer](http://opendata.cern.ch/record/12350) (no need to worry about the details of the physics description)
- Have a look how an automated test run of the first part is implemented as [a GitHub action workflow](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/.github/workflows/main.yml) 
  - What is needed is the container (with the sw installed) where the job is run, and the commands which are passed in [a script](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/commands.sh) [here](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/.github/workflows/main.yml#L20)
  - you can read  [the introduction to github actions](https://docs.github.com/en/actions/learn-github-actions/introduction-to-github-actions), but no need to go in details now
- To put together different steps in analysis, workflow engines will be used. This can be done in a kubernetes cluster using [argo workflow](https://argoproj.github.io/projects/argo/)
  - try the single-step example above using argo in your local minikube environment: 
    - you need these two files [volumes.yaml](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/volumes.yaml) and [argo-workflow.yaml](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/argo-workflow.yaml)
    - see the commands needed after `run:` statements [here](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool/blob/master/.github/workflows/main_argo.yml)
  