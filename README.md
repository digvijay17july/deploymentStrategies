## DeploymentStrategies
# Blue-Green Deployment

Blue-Green deployments use two deployment configurations. Both are running, and the one in production depends on the service the route specifies, with each deployment configuration exposed to a different service. You can create a new route to the new version and test it. When ready, change the service in the production route to point to the new service and the new, blue, version is live.
If necessary, you can roll back to the older, green, version by switching service back to the previous version.


# A/B Deployment
A/B deployments generally imply running two (or more) versions of the application code or application configuration at the same time for testing or experimentation purposes.
The simplest form of an A/B deployment is to divide production traffic between two or more distinct shards — a single group of instances with homogeneous configuration and code.
More complicated A/B deployments may involve a specialized proxy or load balancer that assigns traffic to specific shards based on information about the user or application (all "test" users get sent to the B shard, but regular users get sent to the A shard).
A/B deployments can be considered similar to A/B testing, although an A/B deployment implies multiple versions of code and configuration, where as A/B testing often uses one code base with application specific checks.
