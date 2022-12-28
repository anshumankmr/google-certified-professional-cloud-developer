# Section 4: Integrating Google Cloud services

## 4.1 Integrating an application with data and storage services.

Considerations include:

* Read/write data to/from various databases (e.g., SQL)
   * Reading
      * [SQL Quick Reference from W3Schools](https://www.w3schools.com/sql/sql_quickref.asp)
   * Code/Tutorial
      * [CloudSQL (MySQL) Code Samples](https://cloud.google.com/sql/docs/mysql#code-samples)
* Connecting to a data store (e.g., Cloud SQL, Cloud Spanner, Firestore, Cloud Bigtable)
   * Reading
      * [CloudSQL (MySQL) Connecting Overview](https://cloud.google.com/sql/docs/mysql/connect-overview#:~:text=The%20Cloud%20SQL%20proxy%20allows,for%20a%20Cloud%20SQL%20instance.)
   * Code/Tutorials
      * [Cloud Spanner - Connecting from Go](https://cloud.google.com/spanner/docs/getting-started/go#create_a_database_client)
      * [Using Cloud Spanner with Cloud Functions](https://cloud.google.com/spanner/docs/use-cloud-functions)
      * [Initialize Cloud Firestore](https://firebase.google.com/docs/firestore/quickstart#initialize)
      * [Connecting to Cloud Bigtable (Java)](https://cloud.google.com/bigtable/docs/hbase-connecting)
* Writing an application that publishes/consumes data asynchronously (e.g., from Pub/Sub)
   * Code/Tutorials
      * [PubSub - Quickstart: Using Client Libraries](https://cloud.google.com/pubsub/docs/quickstart-client-libraries)
* Storing and retrieving objects from Cloud Storage
   * Code/Tutorials
      * [List the objects in a bucket](https://cloud.google.com/storage/docs/samples/storage-list-files)
      * [Download an object](https://cloud.google.com/storage/docs/samples/storage-download-file)
      * [Uploading objects](https://cloud.google.com/storage/docs/uploading-objects#storage-upload-object-code-sample)

## 4.2 Integrating an application with compute services.

Considerations include:

* Implementing service discovery in GKE and Compute Engine
   * Reading
      * [GKE - Service discovery and DNS](https://cloud.google.com/kubernetes-engine/docs/concepts/service-discovery)
* Reading instance metadata to obtain application configuration
   * Reading
      * [Compute Engine - Storing and retrieving instance metadata](https://cloud.google.com/compute/docs/storing-retrieving-metadata)
   * Code/Tutorial
      * [App Engine - Accessing Instance Metadata (Java)](https://cloud.google.com/appengine/docs/standard/java/accessing-instance-metadata)
* Authenticating users by using OAuth2.0 Web Flow and Identity-Aware Proxy
   * Reading
      * [IAP - Programmatic authentication](https://cloud.google.com/iap/docs/authentication-howto)
   * Code/Tutorial
      * [Understanding OAuth2 and deploying a basic authorization service to Cloud Functions](https://cloud.google.com/community/tutorials/understanding-oauth2-and-deploy-a-basic-auth-srv-to-cloud-functions)
* Authenticating to Cloud APIs with Workload Identity
   * Reading
      * [GKE - Using Workload Identity](https://cloud.google.com/kubernetes-engine/docs/how-to/workload-identity)

## 4.3 Integrating Cloud APIs with applications.

Considerations include:

* Enabling a Cloud API
   * [Cloud APIs - Enabling APIs](https://cloud.google.com/apis/docs/getting-started#enabling_apis)
* Making API calls using supported options (e.g., Cloud Client Library, REST API or gRPC, APIs Explorer) taking into consideration:
   * Batching requests
      * [Cloud Storage - Sending batch requests](https://cloud.google.com/storage/docs/json_api/v1/how-tos/batch)
      * Restricting return data: When making calls, since there are limits and quotas to the number of calls you can make, they should be carefully constructed. However, calls returning large amounts of data (for instance, all files in a bucket where logs are stored), can cause performance issues. Ensure that calls contain filters to get only the data needed. When calling for info about resources, filter with tools like labels to return the resources needed.
         * https://cloud.google.com/docs/quota
         * In the future, it may be helpful know how to implement quotas in something like Cloud Endpoints(https://cloud.google.com/endpoints/docs/openapi/quotas-overview)  though I did not receive any questions on this.
   * Paginating results
      * [BigQuery - Paging through table data](https://cloud.google.com/bigquery/docs/paging-results)
      * [Firestore - Paginating data with query cursors](https://cloud.google.com/firestore/docs/query-data/query-cursors)
   * Caching results
      * [BigQuery - Using cached query results](https://cloud.google.com/bigquery/docs/cached-results)
      * [Firestore - Access data offline](https://firebase.google.com/docs/firestore/manage-data/enable-offline)
      * [Caching data with Memorystore](https://firebase.google.com/docs/firestore/manage-data/enable-offline)
      * [Caching in Cloud Spannner](https://cloud.google.com/spanner/docs/whitepapers/life-of-query#caching)
   * Error handling (e.g., exponential backoff)
      * [Solutions - Rate-limiting strategies and techniques](https://cloud.google.com/solutions/rate-limiting-strategies-techniques)
   * Reading
      * [Cloud APIs - Google Cloud Client Libraries](https://cloud.google.com/apis/docs/cloud-client-libraries)
      * [Cloud APIs - Client Libraries Explained](https://cloud.google.com/apis/docs/client-libraries-explained)
      * [Cloud APIs - API Design Guide](https://cloud.google.com/apis/design)
      * [gRPC](https://grpc.io/)
* Using service accounts to make Cloud API calls
   * Reading
      * [IAM - Service accounts](https://cloud.google.com/iam/docs/service-accounts)
      * [IAM - Understanding service accounts](https://cloud.google.com/iam/docs/understanding-service-accounts)
      