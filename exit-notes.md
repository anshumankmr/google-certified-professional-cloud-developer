# Exam Exit Notes

Hot tips from those who have done the exam - things that were top of their mind as they exited the exam room. Were there any themes or clusters of questions around certain topics, any *must know* topics that were not highly emphasized in the exam guide etc.

* Understand the differences and use cases between canary, blue-green and A/B testing
* WorkloadIdentity and how it is established and used in GKE
* Horizontal vs Vertical scaling (https://cloud.google.com/kubernetes-engine/docs/concepts/verticalpodautoscaler) in GKE
(At a future point in time, it may be beneficial to know about Multidimensional Pod Autoscaling, though I did not receive any questions about this: https://cloud.google.com/kubernetes-engine/docs/how-to/multidimensional-pod-autoscaling)
* Cost optimization options for web workloads that can scale to zero (AppEngine vs CloudRun etc)
* Key optimization best practices in BigTable and Spanner, including avoiding hotspots
* Optimizing Queries in Cloud Spanner: https://cloud.google.com/spanner/docs/sql-best-practices, like the use of secondary indices
* Benefits and Caveats of using Interleaving/Foreign keys in Cloud Spanner (https://cloud.google.com/spanner/docs/schema-and-data-model)
* Management of GCP API credentials on GCE and GKE - e.g. how to get credentials to call the GCP API in code running from these environments
* Customizing how GCE instances behaved based on the project they are running in (e.g. dev vs prod project) - best way to pass info to the VM to change its behavior
* Downloading account credentials
