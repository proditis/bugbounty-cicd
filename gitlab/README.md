# BugBounty Gitlab Pipelines

* Rename the `pipelines` folder into `.pipelines` and place under your gitlab project root directory
* Rename `dot-gitlab-ci.yml` into `.gitlab.-ci.yml` and place under your gitlab project root directory
* Create a file `domains.list` with your inscope domains
* When the pipeline is started from the web you can bypass certain default settings by passing the following variable from the Gitlab web interface
  * `DOMAINS_LIST`: The file holding the inscope domains (default: `domains.list`)
  * `THREADS`: The limit to the threads that will be applied on those tools that support it (default: `3`)
  * `RATE_LIMIT`: The rate limit to be applied on those tools that support it (default: `5`)
  * `CSP_BASE`: A keyword to search for when we run `cspparse` (default: `example`)
