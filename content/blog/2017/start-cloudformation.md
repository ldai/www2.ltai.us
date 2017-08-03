title=Using Cloudformation
date=2017-07-30
type=post
tags=blog cloudformation aws
status=published
~~~~~~

I'm not going to so a Cloudformat Get-Started tutorial, one can get that from AWS doc site easily.
What I'm trying here now is to use cloudformat to meet the needs of my work:

    1. create an API resource with methods GET, POST and or PUT, the resource is connected/wired to (proxy integration) 
        a lambda function with a particular alias designated by the stage variable in a stage that API is deployed to. 
        The lambda functions used here are in us-east-1 for now.
    2. assign the permission to the execute of lambda function (w/alias mapping to different stage/env) to the API.
    3. create stages for API to deploy to, and add stageVariables. Configure the logging and caching of API
    4. custom domain with base path mapping to api:stage which is equivalent to cloudfront/cdn distributions
    