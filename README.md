# GCP Developer Summary Notes

Table of Contents:
- [GCP Developer Summary Notes](#gcp-developer-summary-notes)
  - [Cloud Identity-Aware Proxy (Cloud IAP)](#cloud-identity-aware-proxy-cloud-iap)
    - [Summary](#summary)
    - [Features](#features)
    - [Steps](#steps)
    - [Questions](#questions)
      - [What is the use-case for Cloud IAP?](#what-is-the-use-case-for-cloud-iap)
      - [How do you set it up in the network?](#how-do-you-set-it-up-in-the-network)
      - [Where do users connect from?](#where-do-users-connect-from)
  - [Cloud Endpoints](#cloud-endpoints)
    - [Summary](#summary-1)
    - [Features](#features-1)
    - [Steps](#steps-1)
    - [Questions](#questions-1)
      - [What are the services you can use Endpoints with?](#what-are-the-services-you-can-use-endpoints-with)
      - [How do you do authentication/authorization with it?](#how-do-you-do-authenticationauthorization-with-it)
    - [Notes](#notes)
  - [Stackdriver](#stackdriver)
    - [Summary](#summary-2)
    - [Features](#features-2)
    - [Steps](#steps-2)
      - [Monitoring](#monitoring)
      - [Trace](#trace)
    - [Questions](#questions-2)
      - [Tracer vs profiler](#tracer-vs-profiler)
      - [What additional things you get when you install the Monitoring Agent?](#what-additional-things-you-get-when-you-install-the-monitoring-agent)
      - [What API permissions do you need after you install Monitoring Agent?](#what-api-permissions-do-you-need-after-you-install-monitoring-agent)
      - [How do you get data from GKE or GCE into stackdriver logs?](#how-do-you-get-data-from-gke-or-gce-into-stackdriver-logs)
      - [Transparent Transparent Service Level Indicators (SLIs)](#transparent-transparent-service-level-indicators-slis)
      - [How do I check the health of resources?](#how-do-i-check-the-health-of-resources)
  - [IAM](#iam)
    - [Summary](#summary-3)
    - [Features](#features-3)
    - [Steps](#steps-3)
    - [Questions](#questions-3)
      - [What are Roles and how do they work?](#what-are-roles-and-how-do-they-work)
      - [What are Google Groups and how do they work?](#what-are-google-groups-and-how-do-they-work)
      - [What are Service Accounts and how do they work?](#what-are-service-accounts-and-how-do-they-work)
      - [What kind of BigQuery job permissions are there?](#what-kind-of-bigquery-job-permissions-are-there)
    - [Notes](#notes-1)
  - [BigTable](#bigtable)
    - [Summary](#summary-4)
    - [Features](#features-4)
    - [Usage](#usage)
    - [Questions](#questions-4)
      - [What are best practices for a key schema?](#what-are-best-practices-for-a-key-schema)
      - [How to avoid hotspotting?](#how-to-avoid-hotspotting)
  - [BigQuery](#bigquery)
    - [Summary](#summary-5)
    - [Features](#features-5)
    - [Usage](#usage-1)
    - [Questions](#questions-5)
      - [How to do batching?](#how-to-do-batching)
      - [Advantages of batching over single queries?](#advantages-of-batching-over-single-queries)
      - [How do I use arrays and structs. How do you join them?](#how-do-i-use-arrays-and-structs-how-do-you-join-them)
      - [How do you provide/restrict access?](#how-do-you-providerestrict-access)
      - [What are Authorized Views?](#what-are-authorized-views)
      - [What are some of the DML statements you can use and how should they be used?](#what-are-some-of-the-dml-statements-you-can-use-and-how-should-they-be-used)
  - [Cloud Datastore](#cloud-datastore)
    - [Summary](#summary-6)
    - [Features](#features-6)
    - [Usage](#usage-2)
    - [Questions](#questions-6)
      - [How do I work with batches?](#how-do-i-work-with-batches)
      - [How do I optimize insertions and queries?](#how-do-i-optimize-insertions-and-queries)
      - [How do I avoid hotspotting?](#how-do-i-avoid-hotspotting)
      - [How do I work with transactions?](#how-do-i-work-with-transactions)
      - [Is ACID possible with Datastore?](#is-acid-possible-with-datastore)
      - [What is the difference between strong and eventual consistency?](#what-is-the-difference-between-strong-and-eventual-consistency)
      - [What are the use-cases for them and how does it affect your choice of database?](#what-are-the-use-cases-for-them-and-how-does-it-affect-your-choice-of-database)
  - [AppEngine](#appengine)
    - [Summary](#summary-7)
    - [Features](#features-7)
    - [Usage](#usage-3)
    - [Questions](#questions-7)
      - [How can I use Memcache with AppEngine?](#how-can-i-use-memcache-with-appengine)
  - [Memcache](#memcache)
    - [Summary](#summary-8)
    - [Features](#features-8)
    - [Usage](#usage-4)
    - [Questions](#questions-8)
      - [How do you work with memcache and flush it?](#how-do-you-work-with-memcache-and-flush-it)
  - [Cloud SQL Proxy](#cloud-sql-proxy)
    - [Summary](#summary-9)
    - [Features](#features-9)
    - [Usage](#usage-5)
    - [Questions](#questions-9)
      - [When is it used and how?](#when-is-it-used-and-how)
      - [How do you connect from various environments?](#how-do-you-connect-from-various-environments)
  - [Google Kubernetes Engine.](#google-kubernetes-engine)
    - [Summary](#summary-10)
    - [Features](#features-10)
    - [Usage](#usage-6)
    - [Questions](#questions-10)
      - [How do I scale deployments?](#how-do-i-scale-deployments)
      - [How do I check the health of VMs, pods, and services?](#how-do-i-check-the-health-of-vms-pods-and-services)
      - [How do you diagnose pods and containers?](#how-do-you-diagnose-pods-and-containers)
      - [What are the limits of gcloud when it comes to GKE?](#what-are-the-limits-of-gcloud-when-it-comes-to-gke)
      - [What are the things that kubectl can do?](#what-are-the-things-that-kubectl-can-do)
  - [Managed Instance Groups](#managed-instance-groups)
    - [Summary](#summary-11)
    - [Features](#features-11)
    - [Usage](#usage-7)
    - [Questions](#questions-11)
      - [How do you scale and update deployments?](#how-do-you-scale-and-update-deployments)
      - [How do you scale MIGs based on various parameters?](#how-do-you-scale-migs-based-on-various-parameters)
  - [Deployment Manager](#deployment-manager)
    - [Summary](#summary-12)
    - [Features](#features-12)
    - [Usage](#usage-8)
    - [Questions](#questions-12)
      - [How do I create templates?](#how-do-i-create-templates)
      - [How do I use references?](#how-do-i-use-references)
      - [How do I use environment variables?](#how-do-i-use-environment-variables)
  - [General Data Protection Regulation (GDPR)](#general-data-protection-regulation-gdpr)
    - [Summary](#summary-13)
    - [HIPAA](#hipaa)
    - [COPPA](#coppa)
  - [Resource Manager](#resource-manager)
    - [Summary](#summary-14)
    - [Features](#features-13)
    - [Usage](#usage-9)
    - [Questions](#questions-13)
      - [How do I use Resource Manager programmatically?](#how-do-i-use-resource-manager-programmatically)
  - [Data Loss Prevention API](#data-loss-prevention-api)
    - [Summary](#summary-15)
    - [Features](#features-14)
    - [Usage](#usage-10)
    - [Questions](#questions-14)
      - [What are use cases for the Data Loss Prevention API?](#what-are-use-cases-for-the-data-loss-prevention-api)
  - [GSuite](#gsuite)
    - [Summary](#summary-16)
    - [Features](#features-15)
    - [Usage](#usage-11)
    - [Questions](#questions-15)
      - [How do you write an app that has permissions on GSuite products?](#how-do-you-write-an-app-that-has-permissions-on-gsuite-products)
  - [gsutil](#gsutil)
    - [Summary](#summary-17)
    - [Features](#features-16)
    - [Usage](#usage-12)
    - [Questions](#questions-16)
      - [What are all the different commands that can be used with gsutil?](#what-are-all-the-different-commands-that-can-be-used-with-gsutil)
      - [What are recommended practices for gsutil?](#what-are-recommended-practices-for-gsutil)
  - [Cloud Armor](#cloud-armor)
    - [Summary](#summary-18)
    - [Features](#features-17)
    - [Usage](#usage-13)
    - [Questions](#questions-17)
      - [What are the use cases for Cloud Armor?](#what-are-the-use-cases-for-cloud-armor)
      - [What kind of protection does it provide?](#what-kind-of-protection-does-it-provide)
  - [Cloud Security Scanner](#cloud-security-scanner)
    - [Summary](#summary-19)
    - [Features](#features-18)
    - [Usage](#usage-14)
    - [Questions](#questions-18)
      - [What are the use cases for Cloud Security Scanner?](#what-are-the-use-cases-for-cloud-security-scanner)
      - [What kind of protection does it provide?](#what-kind-of-protection-does-it-provide-1)
  - [Cloud Storage](#cloud-storage)
    - [Summary](#summary-20)
    - [Features](#features-19)
    - [Usage](#usage-15)
    - [Questions](#questions-19)
      - [What is standard storage and what are the use cases?](#what-is-standard-storage-and-what-are-the-use-cases)
      - [What is nearline storage and what are the use cases?](#what-is-nearline-storage-and-what-are-the-use-cases)
      - [What is coldline storage and what are the use cases?](#what-is-coldline-storage-and-what-are-the-use-cases)
      - [What are signed urls and what are the use cases?](#what-are-signed-urls-and-what-are-the-use-cases)
      - [How do you use a SSD?](#how-do-you-use-a-ssd)
      - [What are the bucket limitations and quotas?](#what-are-the-bucket-limitations-and-quotas)
      - [How can you optimize for heavy load?](#how-can-you-optimize-for-heavy-load)
      - [What are the best options to transfer different amounts of data?](#what-are-the-best-options-to-transfer-different-amounts-of-data)
  - [Cloud Composer](#cloud-composer)
    - [Summary](#summary-21)
    - [Features](#features-20)
    - [Usage](#usage-16)
    - [Questions](#questions-20)
  - [Cloud Spanner](#cloud-spanner)
    - [Summary](#summary-22)
    - [Features](#features-21)
    - [Usage](#usage-17)
    - [Questions](#questions-21)
      - [Under what circumstances and for what use cases is Cloud Spanner a good fit?](#under-what-circumstances-and-for-what-use-cases-is-cloud-spanner-a-good-fit)
  - [Cloud SQL](#cloud-sql)
    - [Summary](#summary-23)
    - [Features](#features-22)
    - [Usage](#usage-18)
    - [Questions](#questions-22)
      - [How to set up regional instances?](#how-to-set-up-regional-instances)
  - [Cloud CDN](#cloud-cdn)
    - [Summary](#summary-24)
    - [Features](#features-23)
    - [Usage](#usage-19)
    - [Questions](#questions-23)
      - [How do I set it up?](#how-do-i-set-it-up)
      - [How do I cache content?](#how-do-i-cache-content)
      - [How do I delete a cache?](#how-do-i-delete-a-cache)
  - [Cloud Build](#cloud-build)
    - [Summary](#summary-25)
    - [Features](#features-24)
    - [Usage](#usage-20)
    - [Questions](#questions-24)
      - [What is the relation to Container Registry?](#what-is-the-relation-to-container-registry)
      - [How do you set up continous builds?](#how-do-you-set-up-continous-builds)
  - [PubSub](#pubsub)
    - [Summary](#summary-26)
    - [Features](#features-25)
    - [Usage](#usage-21)
    - [Questions](#questions-25)
      - [What are the use cases and preferred architecture for and when using PubSub?](#what-are-the-use-cases-and-preferred-architecture-for-and-when-using-pubsub)
      - [What are the fundamentals of PubSub?](#what-are-the-fundamentals-of-pubsub)
  - [Cloud Tasks](#cloud-tasks)
    - [Summary](#summary-27)
    - [Features](#features-26)
    - [Usage](#usage-22)
    - [Questions](#questions-26)
  - [Key Management Service](#key-management-service)
    - [Summary](#summary-28)
    - [Features](#features-27)
    - [Usage](#usage-23)
    - [Questions](#questions-27)
      - [What is the default key management service that Google uses?](#what-is-the-default-key-management-service-that-google-uses)
      - [What is the customer managed encryption keys service?](#what-is-the-customer-managed-encryption-keys-service)
      - [What are the customer supplied encryption keys?](#what-are-the-customer-supplied-encryption-keys)
  - [Case Studies](#case-studies)

## Cloud Identity-Aware Proxy (Cloud IAP)

[LINK](https://cloud.google.com/iap/)

### Summary

Cloud Identity-Aware Proxy (Cloud IAP) controls access to your cloud applications and VMs running on Google Cloud Platform (GCP). Cloud IAP works by verifying user identity and context of the request to determine if a user should be allowed to access an application or a VM. Cloud IAP is a building block toward BeyondCorp, an enterprise security model that enables every employee to work from untrusted networks without the use of a VPN.

**Simpler for cloud admins**

Add secure web access to an application in less time than it takes to implement a VPN. Let your developers focus on their application logic, while **Cloud IAP takes care of authentication and authorization**. Only authenticated users are granted access to the application.

**Simpler for remote workers**

End users point their web browser to an internet-accessible URL to access Cloud IAP-secured applications. **No VPN client is required**.

**Context-aware access**

Administrators can create granular access control policies for applications hosted on GCP, other clouds, and on-premises based on attributes like user identity, device security status, and IP address. Cloud IAP is a key component in Google Cloud’s context-aware access solution.

**Secure access administration**

Configure a single layer of security to manage user access to cloud applications. Administrators can improve security with **Security Key Enforcement** to prevent phishing.

### Features

**Controls access without VPN**

Manage access to your apps and VMs based on a user’s identity and context of the request (e.g. device status, location) without VPN. Powered by Google Cloud’s context-aware access.

**Works with cloud and on-premises apps**

Cloud IAP can protect access to applications hosted on GCP, other clouds, and on-premises.

**Protects your apps and VMs**


With the new TCP forwarding feature, Cloud IAP can now protect SSH and RDP access to your VMs hosted on GCP. Your VM instances don't even need public IP addresses.


### Steps 

**Securing an App Engine App**

* Deploy App Engine Application
* Go to the Identity-Aware Proxy page
* Select the project to which you deployed the sample application
* Go to the OAuth consent screen. 
* Under Support email, select the email address you want to display as a public contact. This must be your email address, or a Google Group you own.
* Enter the Application name you want to display.
* Click Save.

* Go to the Identity-Aware Proxy page. 
* On the right side panel, next to Access, click Add.
* In the Add members dialog that appears, add the email addresses of groups or individuals to whom you want to grant the IAP-secured Web App User role for the project. **Make sure to add a Google account that you have access to.**
* When you're finished adding members, click Add.

* On the Identity-Aware Proxy page, under HTTPS Resources, find the App Engine app you want to restrict access to. The Published column shows the URL of the app. To turn on Cloud IAP for the app, click Off in the IAP column
* To enable Cloud IAP, you need the appengine.applications.update, clientauthconfig.clients.create, and clientauthconfig.clients.getWithSecret permissions. These permissions are granted by roles such as the Project Editor role.
* To confirm that you want the application to be secured by Cloud IAP, click Turn On in the Turn on IAP window that appears. After you turn it on, Cloud IAP requires login credentials for all connections to your application, and only accounts with the IAP-secured Web App User role on this project will be given access.

### Questions

#### What is the use-case for Cloud IAP?

Use Cloud IAP when you want to enforce access control policies for applications and resources. Cloud IAP works with signed headers or the App Engine standard environment Users API to secure your app. With Cloud IAP, you can set up group-based application access: a resource could be accessible for employees and inaccessible for contractors, or only accessible to a specific department.


#### How do you set it up in the network?

[See Steps](#steps)

#### Where do users connect from?

When Cloud IAP is enabled, the first time a user accesses your app, they're redirected to a consent screen to confirm that they want to share their identity with your app. This occurs even if the user granted consent to this app before you enabled Cloud IAP, and will occur again if you disable Cloud IAP and then re-enable it.

If you're using the Users API, it normally suppresses the consent screen for apps and users that are within the same G Suite domain

## Cloud Endpoints

[LINK](https://cloud.google.com/endpoints/docs/choose-endpoints-option)

### Summary

Develop, deploy, protect and monitor your APIs with Google Cloud Endpoints. An NGINX-based proxy and distributed architecture give unparalleled performance and scalability. Using an Open API Specification or one of our API frameworks, Cloud Endpoints gives you the tools you need for every phase of API development and provides insight with Stackdriver Monitoring, Trace and Logging.

### Features

**Protect Your API**

Control who has access to your API and validate every call with JSON Web Tokens and Google API keys. Integration with Auth0 and Firebase Authentication lets you identify the users of your web or mobile application.

**Lightning Fast**

Extensible Service Proxy delivers security and insight in less than 1ms per call. Deploy your API automatically with Google App Engine and Google Kubernetes Engine, or add our proxy container to your Kubernetes deployment.

**World Class Monitoring**

Monitor critical operations metrics in Google Cloud Platform Console, and gain insight into your users and usage with Stackdriver Trace and Logging, and Google BigQuery.

**Choose Your Own Framework**

Use your favorite API framework and language, or choose our open source Cloud Endpoints Frameworks in Java or Python. Simply upload an Open API specification and deploy our containerized proxy.

**API Keys**

Generate API keys in Google Cloud Platform Console and validate on every API call. Share your API with other developers to allow them to generate their own keys.

### Steps

**Choosing an option**

* Cloud Endpoints for OpenAPI
* Cloud Endpoints for gRPC
* Cloud Endpoints Frameworks for the App Engine standard environment


**Endpoints for OpenAPI**

The OpenAPI Initiative is an industry-wide effort to standardize the description of REST APIs. Endpoints supports APIs that are described using version 2.0 of the OpenAPI Specification (formerly the Swagger Specification). You describe the surface of your API in a JSON or YAML file (referred to as an OpenAPI document). You can implement your API using any publicly available REST framework such as Django or Jersey.

**Endpoints for gRPC**

With gRPC, you define the structure of the data that you want to serialize in a proto file: this is an ordinary text file with a .proto extension. You also define the surface of your API in proto files, with RPC method parameters and return types specified as protocol buffer messages. If you are unfamiliar with gRPC, see What is gRPC? in the gRPC documentation.

**Endpoints Frameworks**

Endpoints Frameworks is a web framework for the App Engine standard Python 2.7 and Java 8 runtime environments. You add metadata (using annotations in Java or decorators in Python) to your source code. The metadata describes the surface of the REST APIs for your application.

### Questions

#### What are the services you can use Endpoints with?

* App Engine standard environment generation 1
* App Engine standard environment generation 2			
* App Engine flexible environment			
* Cloud Functions			
* Cloud Run			
* Compute Engine			
* GKE			
* Kubernetes			
* Other non-GCP

#### How do you do authentication/authorization with it?

Choose an Authentication method:

**API keys**

An API key is a simple encrypted string that identifies a Google Cloud Platform (GCP) project for quota, billing, and monitoring purposes. A developer generates an API key in a project in the GCP Console and embeds that key in every call to your API as a query parameter.

If you specify an API key requirement in your service configuration, ESP uses the API key to look up the GCP project that the API key is associated with. ESP rejects requests unless the API key was generated in your GCP project or within other GCP projects in which your API has been enabled. For more information, see Restricting API access with API keys

Unlike credentials that use short-live tokens or signed requests, API keys are a part of the request and are therefore considered to be vulnerable to man-in-the-middle attacks and therefore less secure. You can use API keys in addition to one of the authentication methods described below. For security reasons, don't use API keys by themselves when API calls contain user data.

If you want to use Endpoints features such as quotas, each request must pass in an API key so that Endpoints can identify the GCP project that the client application is associated with.

**Firebase authentication**

Firebase authentication provides backend services, SDKs, and libraries to authenticate users to a mobile or web app. It authenticates users by using a variety of credentials such as Google, Facebook, Twitter, or GitHub.

The Firebase client library signs a JSON Web Token (JWT) with a private key after the user successfully signs in. ESP validates that the JWT was signed by Firebase and that the iss (issuer) claim in the JWT, which identifies your Firebase application, matches the x-google-issuer setting in the service configuration

We recommend using Firebase when the API calls involve any user data and the API is intended to be used in flows where the user has an user interface for example, from mobile and web apps.

**AuthO**

The client library provided by Auth0 generates and signs a JWT once the user signs in. ESP validates the JWT was signed by Auth0 and that the iss claim in the JWT, which identifies your Auth0 application, matches the x-google-issuer setting in the service configuration.

Auth0 is suited for consumer and enterprise web and mobile apps.

**Google ID token authentication**

Authentication with a Google ID token allows users to authenticate by signing in with a Google account. Once authenticated, the user has access to all Google services. You can use Google ID tokens to make calls to Google APIs and to APIs managed by Endpoints. ESP validates the Google ID token by using the public key and ensures that the iss claim in the JWT is https://accounts.google.com

Authentication with a Google ID token is recommended when all users have Google accounts. You might choose to use Google ID token authentication, for example, if your API accompanies a Google application, such as Google Drive companion. Google ID token authentication allows users to authenticate by signing in with a Google account. Once authenticated, the user has access to all Google services.

**Service Accounts**

To identify a service that sends requests to your API, you use a service account. The calling service uses the service account's private key to sign a secure JSON Web Token (JWT) and sends the signed JWT in the request to your API.

JWTs and service accounts are well suited for microservices.

**Custom authentication**

You can use other authentication platforms to authenticate users as long as it conforms to the JSON Web Token RFC 7519.

### Notes

Endpoints for OpenAPI and Endpoints for gRPC use the Extensible Service Proxy (ESP) as an API gateway. Typically, ESP is deployed as a container in front of your application or as a sidecar with your application. After you deploy your API's backend code, ESP intercepts all requests and performs any necessary checks (such as authentication) before forwarding the request to the API backend. When the backend responds, ESP gathers and reports telemetry using Service Infrastructure.

gRPC APIs aren't supported on App Engine, Cloud Functions, or Cloud Run
gRPC is a remote procedure call (RPC) framework that can run on any environment. With gRPC, a client application can directly call methods in a server application on a different machine as if it were a local object. A core feature of gRPC is bi-directional streaming with HTTP/2-based transport.
Unfortunately, App Engine, Cloud Functions, and Cloud Run don't yet support HTTP/2.

## Stackdriver

[LINK](https://cloud.google.com/stackdriver/)

### Summary

Full observability for your code and applications.
Stackdriver aggregates metrics, logs, and events from infrastructure, giving developers and operators a rich set of observable signals that speed root-cause analysis and reduce mean time to resolution (MTTR). Stackdriver doesn’t require extensive integration or multiple “panes of glass,” and it won’t lock developers into using a particular cloud provider.

**Works with multiple clouds and on-premises infrastructure**

Stackdriver is built from the ground up for cloud-powered applications. Whether you’re running on Google Cloud Platform, Amazon Web Services, on-premises infrastructure, or with hybrid clouds, Stackdriver combines metrics, logs, and metadata from all of your cloud accounts and projects into a single comprehensive view of your environment, so you can quickly understand service behavior and take action.

**Find and fix issues fast**

Rich visualization and advanced alerting help you identify issues quickly, even hard-to-diagnose issues like host contention, cloud provider throttling, and degraded hardware. Integration with popular services like PagerDuty and Slack provide for rapid incident response. Integrated logging, tracing, and error reporting enable rapid drill-down and root-cause analysis.

**Full-stack insights**

Stackdriver gives you access to logs, metrics, traces, and other signals from your infrastructure platform(s), virtual machines, containers, middleware, and application tier, so that you can track issues all the way from your end user to your backend services and infrastructure. Native support for distributed systems, auto-scaling, ephemeral resources, and application performance management means that your monitoring works seamlessly with your modern architecture.

**Native Google integration and mor**e

Native integration with Google Cloud data tools BigQuery, Cloud Pub/Sub, Cloud Storage,Cloud Datalab, and out-of-the-box integration with all your other application components.

### Features

**Debugger**

Stackdriver Debugger connects your application’s production data to your source code by inspecting the state of your application at any code location in production without stopping or slowing down your requests.

**Error reporting**

Stackdriver Error Reporting analyzes and aggregates the errors in your cloud applications. Notifies you when new errors are detected.

**Rapid discovery**

Discovers cloud resources and application services automatically based on deep integration with Cloud Platform and Amazon Web Services. Discovers and maintains relationships between key application components and identifies functional groups and clusters.

**Uptime monitoring**

Stackdriver Monitoring provides endpoint checks to web applications and other internet-accessible services running on your cloud environment. You can configure uptime checks associated with URLs, groups, or resources, such as instances and load balancers.

**Integrations**

Our growing Google Stackdriver integrations and tools to make working with Stackdriver even easier.

**Smart defaults**

Thanks to Stackdriver smart defaults, you can get up and running with core visibility into your cloud platform in under two minutes. As you deploy our open source agents, additional metrics and logs are automatically incorporated into the service.

**Alerts**

Allows you to create alerting policies to notify you when metrics, health check results, and uptime check results meet specified criteria. Integrated with a wide variety of notification channels, including Slack and PagerDuty.

**Tracing**

Stackdriver Trace provides latency sampling and reporting for Google App Engine, including per-URL statistics and latency distributions.

**Logging**

Stackdriver Logging provides you with the ability to filter, search, and view logs from your cloud and open source application services. Allows you to define metrics based on log contents that are incorporated into dashboards and alerts. Enables you to export logs to BigQuery, Google Cloud Storage, and Pub/Sub.

**Dashboards**

Provides you with default dashboards for cloud and open source application services. Allows you to define custom dashboards with powerful visualization tools to suit your needs.

**Profiling**

Stackdriver Profiler provides continuous profiling of resource consumption in your production applications, helping you identify and eliminate potential performance issues.

### Steps

#### Monitoring

* Create a Compute Engine Instance
* Install the Stackdriver Monitoring agent on the Compute Engine Instance (ssh)
* Install the Stackdriver Logging agent on the Compute Engine Instance (ssh)

*Create an Uptime Check*

* Go to the Stackdriver Monitoring console
* If you see the invitation **Create an Uptime Check** on the dashboard, then click it. Otherwise, go to **Uptime Checks > Uptime Checks** Overview and then click **Add Uptime Check** or **Create an Uptime Check**
* In the Resource Type drop-down list, select **Instance**
* In the Applies To field, enter *Single, [YOUR VM NAME]*
* Verify uptime check is working by clicking **Test**

*Create an alerting policy*

* In the Uptime Check Created pane, click Create Alerting Policy
* In the Untitled Condition field, enter a title for the alert policy condition. All other fields are in the conditions pane are automatically populated from the uptime check you created
* Save the alerting policy
* Select a Notification Channel Type
* Enter details for the Notification Channel
* Save the policy

*Create a dashboard and chart*

* In the Stackdriver Monitoring console, go to **Dashboards > Create dashboard**
* In the upper-right hand corner, click Add Chart
* In the Add Chart window, click the Metric tab
* Under Find resource type and metric heading, in the instance, cpu, usage, etc. field,  enter CPU, and then select CPU load(1m) from the drop-down list. Leave the other       fields with their default values
* Click Save
* In the new dashboard, change Untitled Dashboard to *you dashboard name*

*View your logs*

* In the Stackdriver Monitoring console, click Logging
* Change the Logs Viewer settings to see the logs you want:
  * In the first drop-down list, select G​C​E VM Instance, *your instance name*
  * In the second drop-down list, select syslog, and click OK
  * Leave the other fields with their default values. The logs from your VM instance     display
* Return to the Stackdriver Monitoring console. To view your logs, in one of your       charts, click the menu icon, and then click View logs.


#### Trace

Go to Stackdriver > Trace

*Find a trace*

* Go to the Trace list page to view a list of recent requests to your application. The trace list allows you to browse and filter all associated traces by URI, module, version, time range, and other parameters. You can use the trace list to find traces whose details you want to view
* Click the URI of any displayed trace in the trace list. The trace details appear in the Google Cloud Platform Console
* The detail view shows a summary of details about the request, a graphical timeline that shows the root span for the end-to-end request and subspans for any RPC calls, and a detailed view of latency data collected for the spans

*Create an analysis report*

* In the navigation panel, click Analysis reports. If you have any reports, they are listed
* At the top of the analysis-reports page, click + New Report
* To include all requests in the report, enter the root span name into the Request filter field. In the previous figure, the root span name is /. You can also enter filter terms in this field to select a subset of traces for the analysis report. See Analysis reports for more information
* Accept the remainder of the default settings for the report. For the time span, the default is the hour previous to when the report was created
* Click Submit to create the report. The new report appears in the analysis report list

### Questions

#### Tracer vs profiler

Profiler allows you to analyze code execution in production. You can use it to see what resource impact your logic has. Use Case: Improve scalability by finding bottleneck areas in your application.

Trace allows you to follow execution in your app from request to the result. Used to determine latency and propogation through the application. Use Case: Determine how long it takes from request to response for a user. 

#### What additional things you get when you install the Monitoring Agent?

Using the Monitoring agent is optional but recommended. Monitoring can access some instance metrics without the Monitoring agent, including CPU utilization, some disk traffic metrics, network traffic, and uptime information. Monitoring uses the Monitoring agent to access additional system resources and application services in virtual machine (VM) instances. If you want these additional capabilities, you should install the Monitoring agent

After installing the Monitoring agent, you can monitor supported third-party applications by adding application-specific collectd configurations. See [Monitoring third-party applications](https://cloud.google.com/monitoring/agent/plugins/) for details.

[Additional metrics you get when installing Monitoring Agent](https://cloud.google.com/monitoring/api/metrics_agent#agent-agent)

#### What API permissions do you need after you install Monitoring Agent?

***Running the agent requires access to the following DNS names:***

OAuth2 token server: `www.googleapis.com` (full URL: `https://www.googleapis.com/oauth2/v3/token`)

Monitoring APIs: `monitoring.googleapis.com`

***Installing the agent requires access to the following DNS names:***

(Linux) Google Cloud package repository: `packages.cloud.google.com`

(Windows) Google download server: `dl.google.com`

#### How do you get data from GKE or GCE into stackdriver logs?

Ensure that you have enabled the Google Kubernetes Engine API.

***GKE***

You can create a cluster with Logging enabled, or enable Logging in an existing cluster.

When you create a cluster, the `--enable-cloud-logging` flag is automatically set, which enables Logging in the cluster.

To disable this default behavior, set the `--no-enable-cloud-logging` flag

To enable logging on an existing cluster:

`gcloud container clusters update [CLUSTER_NAME] --logging-service logging.googleapis.com`

***GCE***

Install the Stackdriver Logging agent on the VM.

Configure the agent

The agent comes preconfigured to monitor certain known log locations. On Linux, those locations are described in the package google-fluentd-catch-all-config, which is automatically pulled in by the installation script. On Windows, the agent monitors the Windows Event Log by default


#### Transparent Transparent Service Level Indicators (SLIs)

A comprehensive, metrics-driven approach is now a baseline objective for most IT ops teams. Many businesses now measure IT on service availability and performance. But for IT teams that depend on cloud services, it can be hard to get solid data on services that are provided by an outside cloud provider. If there is a problem, where is it? With your stack or with the service provider? Transparent SLIs help you monitor Google Cloud services and their effects on your workloads, so you can get the complete picture

To help IT understand the performance of all your services components, Google provides detailed API level metrics for over 130 Google Cloud services. These metrics show you the error counts and latency for your applications' requests to each Google service. This lets you see correlations and side effects between your applications and the services they depend on, helping to speed root-cause analysis and time to resolution

SLIs go far beyond traditional notions of “service health.” You can see the specific interactions between services and correlate those to environmental data. This allows you to cross tab service metrics by a variety of attributes such as location of the service, credential of the app calling the service, version and response code to help you explore relationships and determine causes and effects

* If all calls to a service are failing for one user but not any other, chances are there is something wrong with that account that you can easily fix yourself.

* If you're troubleshooting a problem with your app and notice a correlation between your application's degraded performance and a sustained increase in latency for a critical GCP service, this is a sign to call us and get us to help.

* If the latencies for a GCP service report look good and unchanged from before, but your in-app metrics report that the latency on calls to the service is abnormally high, that tells you that there could be some trouble in the network. Call your network provider (in some cases, Google) to get the debugging process started.

#### How do I check the health of resources?

## IAM

### Summary

Google Cloud Platform (GCP) offers Cloud IAM, which lets you manage access control by defining who (identity) has what access (role) for which resource.

With Cloud IAM you can grant granular access to specific GCP resources and prevent unwanted access to other resources. Cloud IAM lets you adopt the security principle of least privilege, so you grant only the necessary access to your resources.

In Cloud IAM, you grant access to members. Members can be of the following types:

* Google account
* Service account
* Google group
* G Suite domain
* Cloud Identity domain

**Resource**
You can grant access to users for a GCP resource. Some examples of resources are projects, Compute Engine instances, and Cloud Storage buckets.

Some services, such as Compute Engine and Cloud Storage, support granting Cloud IAM permissions at a granularity finer than the project level. For example, you can grant the Storage Admin (roles/storage.admin) role to a user for a particular Cloud Storage bucket, or you can grant the Compute Instance Admin (roles/compute.instanceAdmin) role to a user for a specific Compute Engine instance.

In other cases, you can grant Cloud IAM permissions at the project level. The permissions are then inherited by all resources within that project. For example, to grant access to all Cloud Storage buckets in a project, grant access to the project instead of each individual bucket. Or to grant access to all Compute Engine instances in a project, grant access to the project rather than each individual instance.

**Permissions**
Permissions determine what operations are allowed on a resource. In the Cloud IAM world, permissions are represented in the form of `<service>.<resource>.<verb>`, for example pubsub.subscriptions.consume.

Permissions usually, but not always, correspond 1:1 with REST methods. That is, each GCP service has an associated set of permissions for each REST method that it exposes. The caller of that method needs those permissions to call that method. For example, the caller of Publisher.Publish() needs the pubsub.topics.publish permission.

You don't assign permissions to users directly. Instead, you assign them a Role which contains one or more permissions.

**Roles**
A role is a collection of permissions. You cannot assign a permission to the user directly; instead you grant them a role. When you grant a role to a user, you grant them all the permissions that the role contains.

**IAM Policy**

You can grant roles to users by creating a Cloud IAM policy, which is a collection of statements that define who has what type of access. A policy is attached to a resource and is used to enforce access control whenever that resource is accessed.



### Features

**Single access control interface**

Cloud IAM provides a simple and consistent access control interface for all Google Cloud Platform services. Learn one access control interface and apply that knowledge to all GCP resources.

**Fine-grained control**

Grant access to users at a resource level of granularity, rather than just project level. For example, you can create a Cloud IAM access-control policy that grants the Subscriber role to a user for a particular Cloud Pub/Sub topic.

**Context-aware access**

Control access to resources based on contextual attributes like device security status, IP address, resource type, and date/time. Sign up for the Cloud IAM conditions private beta here.

**Flexible roles**

Prior to Cloud IAM, you could only grant Owner, Editor, or Viewer roles to users. A wide range of services and resources now surface additional Cloud IAM roles out of the box. For example, the Cloud Pub/Sub service exposes Publisher and Subscriber roles in addition to the Owner, Editor, and Viewer roles.

**Web, programmatic, and command-line access**

Create and manage Cloud IAM policies using the Google Cloud Platform Console, the Cloud IAM methods, and the gcloud tool.

**Built-in audit trail**

To ease compliance processes for your organization, a full audit trail is made available to admins without any additional effort.

**Support for Cloud Identity**

Cloud IAM supports standard Google accounts. Create Cloud IAM policies granting permission to a Google group, a Google-hosted domain, a service account, or specific Google account holders using Cloud Identity. Centrally manage users and groups through the Cloud Identity Admin Console.

**Free of charge**

Cloud IAM is offered at no additional charge for all Google Cloud Platform customers. You will be charged only for use of other GCP services.

### Steps

Add a project member and grant them an IAM role

* Open the IAM page in the GCP console
* Click Select a project.
* Select a project and click Open.
* Click Add.
* Enter the email address of a new member to whom you have not granted any Cloud IAM role previously.
* Select one of the following roles from the drop-down menu, depending on the GCP service you use:
  * If you are a Stackdriver Logging user, select Logging and then Logs Viewer.
  * If you are a Compute Engine user, select Compute Engine and then Compute Instance Admin.
  * If you are an App Engine user, select App Engine and then App Engine Admin.
  * If you are a Cloud Storage user, select Storage and then Storage Admin.
  * Click Save.
  * Verify that the member and the corresponding role is listed in the Cloud IAM page

### Questions

#### What are Roles and how do they work?

There are three types of roles in Cloud IAM:

* **Primitive roles**, which include the Owner, Editor, and Viewer roles that existed prior to the introduction of Cloud IAM
* **Predefined roles**, which provide granular access for a specific service and are managed by GCP
* **Custom roles**, which provide granular access according to a user-specified list of permissions

To determine if one or more permissions are included in a primitive, predefined, or custom role, you can use one of the following methods:

* The gcloud iam roles describe command
* The roles.get() API

[Granular permission Roles for many of the GCP Services](https://cloud.google.com/iam/docs/understanding-roles)

#### What are Google Groups and how do they work?

A Google group is a named collection of Google accounts and service accounts. Every group has a unique email address that is associated with the group. You can find the email address that is associated with a Google group by clicking About on the homepage of any Google group. For more information about Google groups, see the Google groups homepage.

Google groups are a convenient way to apply an access policy to a collection of users. You can grant and change access controls for a whole group at once instead of granting or changing access controls one-at-a-time for individual users or service accounts. You can also easily add members to and remove members from a Google group instead of updating a Cloud IAM policy to add or remove users.

Note that Google groups don't have login credentials, and you cannot use Google groups to establish identity to make a request to access a resource

#### What are Service Accounts and how do they work?

A service account is a special Google account that belongs to your application or a virtual machine (VM), instead of to an individual end user. Your application uses the service account to call the Google API of a service, so that the users aren't directly involved.

A service account is identified by its email address, which is unique to the account

* Service accounts do not have passwords, and cannot log in via browsers or cookies.
* Service accounts are associated with private/public RSA key-pairs that are used for authentication to Google.
* Cloud IAM permissions can be granted to allow other users (or other service accounts to impersonate a service account.
* Service accounts offer higher service-level objectives (SLOs) than user accounts when authenticating to GCP, ensuring reliable service for applications that use them.
* Service accounts are not members of your G Suite domain, unlike user accounts. For example, if you share assets with all members in your G Suite domain, they will not be shared with service accounts. Similarly, any assets created by a service account cannot be owned or managed by G Suite admins

#### What kind of BigQuery job permissions are there?

|Permission|Description|
|----------|-----------|
|`bigquery.jobs.create`|	Create new jobs.|
|`bigquery.jobs.listAll`|	List all jobs and retrieve metadata on any job submitted by any user.*|
|`bigquery.jobs.list`|	List all jobs and retrieve metadata on any job submitted by any user.* For jobs submitted by other users, details and metadata are redacted.|
|`bigquery.jobs.get`|	Get data and metadata on any job.*|
|`bigquery.jobs.update`|	Cancel any job.*|

### Notes

Cloud IAM predefined roles:

* [Google Cloud Platform project](https://cloud.google.com/resource-manager/docs/access-control-proj)
* [GCP Organization](https://cloud.google.com/resource-manager/docs/access-control-org)
* [Compute Engine](https://cloud.google.com/compute/docs/access/iam)
* [Cloud Source Repositories](https://cloud.google.com/source-repositories/docs/configure-access-control)
* [App Engine](https://cloud.google.com/appengine/docs/java/console/access-control)
* [Cloud Storage](https://cloud.google.com/storage/docs/iam)
* [BigQuery](https://cloud.google.com/bigquery/docs/access-control)
* [Cloud Bigtable](https://cloud.google.com/bigtable/docs/access-control)
* [IAM for Cloud SQL](https://cloud.google.com/sql/docs/project-access-control)
* [Stackdriver Debugger](https://cloud.google.com/debugger/docs/iam)
* [Cloud Deployment Manager](https://cloud.google.com/deployment-manager/docs/access-control)
* [Cloud Genomics](https://cloud.google.com/genomics/reference/rest/v1/datasets/setIamPolicy)
* [Cloud Key Management Service](https://cloud.google.com/kms/docs/iam)
* [Cloud Pub/Sub](https://cloud.google.com/pubsub/access_control)
* [AI Platform](https://cloud.google.com/ml-engine/docs/access-control)
* [Cloud Spanner](https://cloud.google.com/spanner/docs/iam)
* [Stackdriver Logging](https://cloud.google.com/logging/docs/access-control)
* [Cloud IAM for Stackdriver Monitoring](https://cloud.google.com/monitoring/access-control)
* [Cloud Dataflow](https://cloud.google.com/dataflow/access-control)
* [Cloud IAM for Cloud Datastore](https://cloud.google.com/datastore/docs/access/iam)
* [Cloud IAM for Cloud Dataproc](https://cloud.google.com/dataproc/docs/concepts/iam)
* [Cloud IAM for Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine/docs/how-to/iam)
* [Cloud IAM for Cloud DNS](https://cloud.google.com/dns/access-control)
* [Cloud IAM for Stackdriver Trace](https://cloud.google.com/trace/docs/iam)
* [Cloud IAM for Cloud Billing API](https://cloud.google.com/billing/v1/how-tos/access-control)
* [Cloud IAM for Service Management](https://cloud.google.com/service-management/access-control)

## BigTable

### Summary

A petabyte-scale, fully managed NoSQL database service for large analytical and operational workloads.

Cloud Bigtable is Google's NoSQL Big Data database service. It's the same database that powers many core Google services, including Search, Analytics, Maps, and Gmail.

### Features

* Low latency, massively scalable NoSQL
* Consistent sub-10ms latency
* Replication provides higher availability, higher durability, and resilience in the face of zonal failures
* Ideal for Ad Tech, Fintech, and IoT
* Storage engine for machine learning applications
* Easy integration with open source big data tools

**Fast and performant**

Use Cloud Bigtable as the storage engine for large-scale, low-latency applications as well as throughput-intensive data processing and analytics.

**Seamless scaling and replication**
Provision and scale to hundreds of petabytes, and smoothly handle millions of operations per second. Changes to the deployment configuration are immediate, so there’s no downtime during reconfiguration. Replication adds high availability for live serving apps, and workload isolation for serving vs. analytics.

**Simple and integrated**
Cloud Bigtable integrates easily with popular big data tools like Hadoop, Cloud Dataflow, and Cloud Dataproc. Plus, Cloud Bigtable supports the open source industry standard HBase API, which makes it easy for your development teams to get started.

**Fully managed**
Because we manage the database and handle the configuring and tuning, you can focus on developing applications.

### Usage

Command line tool for BigTable is `cbt`

For example:

`gcloud components install cbt`

`cbt createtable my-table`

### Questions

#### What are best practices for a key schema?

Concepts to keep in mind:

* **Each table has only one index, the row key**. There are no secondary indices.
* **Rows are sorted lexicographically by row key**, from the lowest to the highest byte string. Row keys are sorted in big-endian, or network, byte order, the binary equivalent of alphabetical order.
* **Columns are grouped by column family and sorted in lexicographic order within the column family.**
* **All operations are atomic at the row level**. For example, if you update two rows in a table, it's possible that one row will be updated successfully and the other update will fail. Avoid schema designs that require atomicity across rows.
* **Ideally, both reads and writes should be distributed evenly** across the row space of the table.
* **In general, keep all information for an entity in a single row**. An entity that doesn't need atomic updates and reads can be split across multiple rows. Splitting across multiple rows is recommended if the entity data is large (hundreds of MB).
* **Related entities should be stored in adjacent rows**, which makes reads more efficient.
* **Cloud Bigtable tables are sparse**. Empty columns don't take up any space. As a result, it often makes sense to create a very large number of columns, even if most columns are empty in most rows.

***Size limits***

Cloud Bigtable places size limits on the data that you store within your tables. Make sure you consider these limits as you design your schema.

Because Cloud Bigtable reads rows atomically, it's especially important to limit the total amount of data that you store in a single row. As a best practice, store a maximum of 10 MB in a single cell and 100 MB in a single row. You must also stay below the hard limits on data size within cells and rows.

These size limits are measured in binary megabytes (MB), where 1 MB is 220 bytes. This unit of measurement is also known as a mebibyte (MiB).

***Row Keys***

To get the best performance out of Cloud Bigtable, it's essential to think carefully about how you compose your row key. That's because the most efficient Cloud Bigtable queries use the row key, a row key prefix, or a row range to retrieve the data. Other types of queries trigger a full table scan, which is much less efficient. By choosing the correct row key now, you can avoid a painful data-migration process later.

* **User information**: Do you need quick access to information about connections between users (for example, whether user A follows user B)?
* **User-generated content**: If you show users a sample of a large amount of user-generated content, such as status updates, how will you decide which status updates to display to a given user?
* **Time series data**: Will you often need to retrieve the most recent N records, or records that fall within a certain time range? If you're storing data for several kinds of events, will you need to filter based on the type of event?

If you're storing data about entities that can be represented as domain names, consider using a reverse domain name (for example, com.company.product) as the row key. Using a reverse domain name is an especially good idea if each row's data tends to overlap with adjacent rows. In this case, Cloud Bigtable can compress your data more efficiently.

If you're storing data about entities that can be identified with a simple string (for example, user IDs), you might want to use the string identifier as the row key, or as a portion of the row key.

Use human-readable values instead of hashing the row key. Also, if your row key includes multiple values, separate those values with a delimiter. These practices make it much easier to use the Key Visualizer tool to troubleshoot issues with Cloud Bigtable.

If you often need to retrieve data based on the time when it was recorded, it's a good idea to include a timestamp as part of your row key. Using the timestamp by itself as the row key is not recommended, as most writes would be pushed onto a single node. For the same reason, avoid placing a timestamp at the start of the row key.

If you usually retrieve the most recent records first, you can use a reversed timestamp in the row key by subtracting the timestamp from your programming language's maximum value for long integers (in Java, java.lang.Long.MAX_VALUE). With a reversed timestamp, the records will be ordered from most recent to least recent.

Because the only way to query Cloud Bigtable efficiently is by row key, it's often useful to include multiple identifiers in your row key. When your row key includes multiple values, it's especially important to have a clear understanding of how you'll use your data.

The first value in a multi-value row key is called a row key prefix. Well-planned row key prefixes let you take advantage of Cloud Bigtable's sorting order to store related data in contiguous rows. Storing related data in contiguous rows enables you to access related data as a range of rows, rather than running inefficient table scans.

Row key prefixes provide a scalable solution for a "multitenancy" use case, a scenario in which you store similar data, using the same data model, on behalf of multiple clients. Using one table for all tenants is usually the most performant way to store and access multitenant data. In contrast, if you stored data on behalf of each company in its own table, you would be much more likely to experience performance and scalability issues, and you could inadvertently exceed Cloud Bigtable's limit of 1,000 tables per instance.

***Row keys to avoid***

Avoid using standard, non-reversed domain names as row keys. Using standard domain names makes it inefficient to retrieve all of the rows within a portion of the domain (for example, all rows that relate to company.com will be in separate row ranges like services.company.com, product.company.com and so on)

Suppose your system assigns a numeric ID to each of your application's users. You might be tempted to use the user's numeric ID as the row key for your table. However, because new users are more likely to be active users, this approach is likely to push most of your traffic to a small number of nodes. A safer approach is to use a reversed version of the user's numeric ID, which spreads traffic more evenly across all of the nodes for your Cloud Bigtable table.

Avoid using a single row key to identify a value that must be updated very frequently. For example, if you store memory-usage data once per second, do not use a single row key named memusage and update the row repeatedly. This type of operation overloads the tablet that stores the frequently used row. It can also cause a row to exceed its size limit, because a cell's previous values take up space for a while.

Instead, store one value per row, using a row key that contains the type of metric, a delimiter, and a timestamp. For example, to track memory usage over time, you could use row keys similar to memusage#1423523569918. This strategy is efficient because in Cloud Bigtable, creating a new row takes no more time than creating a new cell. In addition, this strategy enables you to quickly read data from a specific date range by calculating the appropriate start and end keys.

For values that change very frequently, such as a counter that is updated hundreds of times each minute, it's best to simply keep the data in memory, at the application layer, and write new rows to Cloud Bigtable periodically.

***Column families and qualifiers***

*Column families*

In Cloud Bigtable, unlike in HBase, you can use up to about 100 column families while maintaining excellent performance. As a result, whenever a row contains multiple values that are related to one another, it's a good practice to group those values into the same column family. Grouping data into column families enables you to retrieve data from a single family, or multiple families, rather than retrieving all of the data in each row. Group data as closely as you can to get just the information that you need, but no more, in your most frequent API calls.

Also, the names of your column families should be short, because they're included in the data that is transferred for each request.

*Column qualifiers*

Because Cloud Bigtable tables are sparse, you can create as many column qualifiers as you need in each row. There is no space penalty for empty cells in a row. As a result, it often makes sense to treat column qualifiers as data. For example, if your table is storing user posts, you could use the unique identifier for each post as the column qualifier.

That said, you should avoid splitting your data across more column qualifiers than necessary, which can result in rows that have a very large number of non-empty cells. It takes time for Cloud Bigtable to process each cell in a row. Also, each cell adds some overhead to the amount of data that's stored in your table and sent over the network. For example, if you're storing 1 KB (1,024 bytes) of data, it's much more space-efficient to store that data in a single cell, rather than spreading the data across 1,024 cells that each contain 1 byte. If you normally read or write a few related values all at once, consider storing all of those values together in one cell, using a format that makes it easy to extract the individual values later (such as the protocol buffer binary format).

#### How to avoid hotspotting?

The most common issue for time series in Cloud Bigtable is hotspotting. This issue can affect any type of row key that contains a monotonically increasing value.

In brief, when a row key for a time series includes a timestamp, all of your writes will target a single node; fill that node; and then move onto the next node in the cluster, resulting in hotspotting. For example, if you're storing a cell phone's battery status, and your row key consists of the word "BATTERY" plus a timestamp (as shown below), the row key will always increase in sequence. Because Cloud Bigtable stores adjacent row keys on the same server node, all writes will focus only on one node until that node is full, at which point writes will move to the next node in the cluster.

***There are a few ways to solve this problem:***

**Field promotion.** Move fields from the column data into the row key to make writes non-contiguous.

The advantage of **field promotion** is that it often makes your queries more efficient as well, making this strategy a clear winner. The (slight) disadvantage is that your queries are constrained by your promoted fields, leading to rework if you don't promote the right fields.

**Salting.** Add an additional calculated element to the row key to artificially make writes non-contiguous.

The advantage of salting is its simplicity—it's essentially a simple hashing function. One disadvantage is that when you query for time ranges, you'll have to do multiple scans—one scan per salt value—and combine the results in your own code. Another disadvantage is that it's difficult to choose a salt value that both distributes activity across nodes and operates well as you scale your system up or down. Because of these disadvantages, and because it's best to use human-readable row keys, avoid salting unless you can find no other way to prevent hotspotting.

**By default**, prefer field promotion. Field promotion avoids hotspotting in almost all cases, and it tends to make it easier to design a row key that facilitates queries.

Use salting only where field promotion does not resolve hotspotting. In the rare case where you apply a salting function, be careful not to make too many assumptions about the underlying size of the cluster. The example above uses a salting function that assumes there are 3 nodes in the cluster; this assumption is safe because it would scale to the limited number of nodes that can exist in a Cloud Bigtable cluster. If you could create clusters with hundreds of nodes, you would want to use a different salting function.

## BigQuery

### Summary

BigQuery, Google's serverless, highly scalable enterprise data warehouse, is designed to make data analysts more productive with unmatched price-performance. Because there is no infrastructure to manage, you can focus on uncovering meaningful insights using familiar SQL without the need for a database administrator.

Analyze all your batch and streaming data by creating a logical data warehouse over managed columnar storage, as well as data from object storage and spreadsheets. Create blazing-fast dashboards and reports with the in-memory BI Engine. Build and operationalize machine learning solutions or carry out geospatial analysis using simple SQL. Securely share insights within your organization and beyond as datasets, queries, spreadsheets, and reports. BigQuery’s powerful streaming ingestion captures and analyzes data in real time, ensuring insights are always current. Plus, you can analyze up to 1 TB of data and store 10 GB of data for free each month.

### Features

**Serverless**

With serverless data warehousing, Google does all resource provisioning behind the scenes, so you can focus on data and analysis rather than worrying about upgrading, securing, or managing the infrastructure.

**Real-time analytics**

BigQuery’s high-speed streaming insertion API provides a powerful foundation for real-time analytics, making your latest business data immediately available for analysis.

**Automatic high availability**

BigQuery transparently and automatically provides highly durable, replicated storage in multiple locations and high availability with no extra charge and no additional setup.

**Standard SQL**	

BigQuery supports a standard SQL dialect which is ANSI:2011 compliant, which thereby reduces the need for code rewrites. BigQuery also provides ODBC and JDBC drivers at no cost to ensure your current applications can interact with its powerful engine.

**Federated query and logical data warehousing**	

Through powerful federated query, BigQuery can process external data sources in object storage (Cloud Storage), transactional databases (Cloud Bigtable), or spreadsheets in Drive — all without duplicating data.

**Storage and compute separation**	

With BigQuery’s separated storage and compute, you have the option to choose the storage and processing solutions that make sense for your business and control access and costs for each.

**Automatic backup and easy restore**	

BigQuery automatically replicates data and keeps a seven-day history of changes, allowing you to easily restore and compare data from different times.

**Geospatial data types and functions**	

BigQuery GIS brings SQL support for arbitrary points, lines, polygons, and multi-polygons in WKT and GeoJSON format. You can simplify your geospatial analyses, see your location-based data in new ways, or unlock entirely new lines of business.

**Data transfer service**	

The BigQuery Data Transfer Service automatically transfers data from external data sources, like Google Marketing Platform, Google Ads, YouTube, and partner SaaS applications to BigQuery on a scheduled and fully managed basis. Users can also easily transfer data from Teradata and Amazon S3 to BigQuery.

**Big data ecosystem integration**	

With Cloud Dataproc and Cloud Dataflow, BigQuery provides integration with the Apache Big Data ecosystem, allowing existing Hadoop/Spark and Beam workloads to read or write data directly from BigQuery.

**Petabyte scale**	

Get great performance on your data, while knowing you can scale seamlessly to store and analyze petabytes more without having to buy more capacity.

**Flexible pricing models**	

On-demand pricing lets you pay only for the storage and compute that you use. Flat-rate pricing enables high-volume users or enterprises to choose a stable monthly cost. For more information, see BigQuery pricing or cost controls.

**Data governance and security**	

BigQuery makes it easy to maintain strong security with fine-grained identity and access management with Cloud Identity and Access Management, and your data is always encrypted at rest and in transit.

**Geoexpansion**	

BigQuery gives you the option of geographic data control (in US, Asia, and European locations), without the headaches of setting up and managing clusters and other computing resources in region.

**Foundation for AI**	

Besides bringing ML to your data with BigQuery ML, integrations with Cloud ML Engine and TensorFlow enable you to train powerful models on structured data in minutes with just SQL.

**Foundation for BI**

BigQuery forms the data warehousing backbone for modern BI solutions and enables seamless data integration, transformation, analysis, visualization, and reporting with tools from Google and our technology partners.

**Flexible data ingestion**

Load your data from Cloud Storage or stream it into BigQuery at thousands of rows per second to enable real-time analysis of your data. Use familiar data integration tools like Informatica, Talend, and others out of the box.

**Programmatic interaction**	

BigQuery provides a REST API for easy programmatic access and application integration. Client libraries are available in Java, Python, Node.js, C#, Go, Ruby, and PHP. Business users can use Google Apps Script to access BigQuery from Sheets.

**Rich monitoring and logging with Stackdriver**	

BigQuery provides rich monitoring, logging, and alerting through Stackdriver Audit Logs and it can serve as a repository for logs from any application or service using Stackdriver Logging.

### Usage

* Web UI in the GCP Console
* CLI
* Client Libraries

BigQuery is automatically enabled in new projects. To activate BigQuery in a pre-existing project, go to Enable the BigQuery API.

Use bq help to get detailed information about the bq command-line tool:

`bq help`

Running a query:

```bash
bq query --use_legacy_sql=false \
'SELECT
   word,
   SUM(word_count) AS count
 FROM
   `bigquery-public-data`.samples.shakespeare
 WHERE
   word LIKE "%raisin%"
 GROUP BY
   word'
```

### Questions

#### How to do batching?

A batch request consists of multiple API calls combined into one HTTP request, which can be sent to the `batchPath` specified in the API discovery document. The default path is `/batch/api_name/api_version`. This section describes the batch syntax in detail; later, there's an example.

***Format of a batch request***

A batch request is a single standard HTTP request containing multiple Google BigQuery API calls, using the `multipart/mixed` content type. Within that main HTTP request, each of the parts contains a nested HTTP request.

Each part begins with its own Content-Type: `application/http` HTTP header. It can also have an optional `Content-ID` header. However, the part headers are just there to mark the beginning of the part; they're separate from the nested request. After the server unwraps the batch request into separate requests, the part headers are ignored.

The body of each part is itself a complete HTTP request, with its own verb, URL, headers, and body. The HTTP request must only contain the path portion of the URL; full URLs are not allowed in batch requests.

The HTTP headers for the outer batch request, except for the Content- headers such as `Content-Type`, apply to every request in the batch. If you specify a given HTTP header in both the outer request and an individual call, then the individual call header's value overrides the outer batch request header's value. The headers for an individual call apply only to that call.

For example, if you provide an Authorization header for a specific call, then that header applies only to that call. If you provide an Authorization header for the outer request, then that header applies to all of the individual calls unless they override it with Authorization headers of their own.

When the server receives the batched request, it applies the outer request's query parameters and headers (as appropriate) to each part, and then treats each part as if it were a separate HTTP request.

***Response to a batch request***

The server's response is a single standard HTTP response with a `multipart/mixed` content type; each part is the response to one of the requests in the batched request, in the same order as the requests.

Like the parts in the request, each response part contains a complete HTTP response, including a status code, headers, and body. And like the parts in the request, each response part is preceded by a Content-Type header that marks the beginning of the part.

If a given part of the request had a Content-ID header, then the corresponding part of the response has a matching Content-ID header, with the original value preceded by the string response-, as shown in the following example.

***Example batch request:***

```
POST /batch/farm/v1 HTTP/1.1
Authorization: Bearer your_auth_token
Host: www.googleapis.com
Content-Type: multipart/mixed; boundary=batch_foobarbaz
Content-Length: total_content_length

--batch_foobarbaz
Content-Type: application/http
Content-ID: <item1:12930812@barnyard.example.com>

GET /farm/v1/animals/pony

--batch_foobarbaz
Content-Type: application/http
Content-ID: <item2:12930812@barnyard.example.com>

PUT /farm/v1/animals/sheep
Content-Type: application/json
Content-Length: part_content_length
If-Match: "etag/sheep"

{
  "animalName": "sheep",
  "animalAge": "5"
  "peltColor": "green",
}

--batch_foobarbaz
Content-Type: application/http
Content-ID: <item3:12930812@barnyard.example.com>

GET /farm/v1/animals
If-None-Match: "etag/animals"

--batch_foobarbaz--
```

***Example batch response:***

```
HTTP/1.1 200
Content-Length: response_total_content_length
Content-Type: multipart/mixed; boundary=batch_foobarbaz

--batch_foobarbaz
Content-Type: application/http
Content-ID: <response-item1:12930812@barnyard.example.com>

HTTP/1.1 200 OK
Content-Type application/json
Content-Length: response_part_1_content_length
ETag: "etag/pony"

{
  "kind": "farm#animal",
  "etag": "etag/pony",
  "selfLink": "/farm/v1/animals/pony",
  "animalName": "pony",
  "animalAge": 34,
  "peltColor": "white"
}

--batch_foobarbaz
Content-Type: application/http
Content-ID: <response-item2:12930812@barnyard.example.com>

HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: response_part_2_content_length
ETag: "etag/sheep"

{
  "kind": "farm#animal",
  "etag": "etag/sheep",
  "selfLink": "/farm/v1/animals/sheep",
  "animalName": "sheep",
  "animalAge": 5,
  "peltColor": "green"
}

--batch_foobarbaz
Content-Type: application/http
Content-ID: <response-item3:12930812@barnyard.example.com>

HTTP/1.1 304 Not Modified
ETag: "etag/animals"

--batch_foobarbaz--
```

#### Advantages of batching over single queries?

Each HTTP connection that your client makes results in a certain amount of overhead. The Google BigQuery API supports batching, to allow your client to put several API calls into a single HTTP request.

#### How do I use arrays and structs. How do you join them?

#### How do you provide/restrict access? 

Remember that you cannot restrict access at table level. It is only at dataset level. 

#### What are Authorized Views?

#### What are some of the DML statements you can use and how should they be used?

## Cloud Datastore

### Summary

### Features

### Usage

### Questions

#### How do I work with batches?

#### How do I optimize insertions and queries?

#### How do I avoid hotspotting?

#### How do I work with transactions?

#### Is ACID possible with Datastore?

#### What is the difference between strong and eventual consistency?

#### What are the use-cases for them and how does it affect your choice of database?

## AppEngine

### Summary

### Features

### Usage

### Questions

#### How can I use Memcache with AppEngine?

## Memcache

### Summary

### Features

### Usage

### Questions

#### How do you work with memcache and flush it?

## Cloud SQL Proxy

### Summary

### Features

### Usage

### Questions

#### When is it used and how?

#### How do you connect from various environments?

## Google Kubernetes Engine. 

### Summary

### Features

### Usage

### Questions

#### How do I scale deployments?

#### How do I check the health of VMs, pods, and services?

#### How do you diagnose pods and containers?

#### What are the limits of gcloud when it comes to GKE? 

#### What are the things that kubectl can do?

## Managed Instance Groups

### Summary

### Features

### Usage

### Questions

#### How do you scale and update deployments?

#### How do you scale MIGs based on various parameters?

## Deployment Manager

### Summary

### Features

### Usage

### Questions

#### How do I create templates?

#### How do I use references?

#### How do I use environment variables?

## General Data Protection Regulation (GDPR)

### Summary

### HIPAA

### COPPA

## Resource Manager

### Summary

### Features

### Usage

### Questions

#### How do I use Resource Manager programmatically?

## Data Loss Prevention API

### Summary

### Features

### Usage

### Questions

#### What are use cases for the Data Loss Prevention API?

## GSuite 

### Summary

### Features

### Usage

### Questions

#### How do you write an app that has permissions on GSuite products?

## gsutil

### Summary

### Features

### Usage

### Questions

#### What are all the different commands that can be used with gsutil?

#### What are recommended practices for gsutil?

## Cloud Armor

### Summary

### Features

### Usage

### Questions

#### What are the use cases for Cloud Armor?

#### What kind of protection does it provide?

## Cloud Security Scanner

### Summary

### Features

### Usage

### Questions

#### What are the use cases for Cloud Security Scanner?

#### What kind of protection does it provide?

## Cloud Storage

### Summary

### Features

### Usage

### Questions

#### What is standard storage and what are the use cases?

#### What is nearline storage and what are the use cases?

#### What is coldline storage and what are the use cases?

#### What are signed urls and what are the use cases?

#### How do you use a SSD?

#### What are the bucket limitations and quotas?

#### How can you optimize for heavy load?

#### What are the best options to transfer different amounts of data?

## Cloud Composer

### Summary

### Features

### Usage

### Questions

## Cloud Spanner

### Summary

### Features

### Usage

### Questions

#### Under what circumstances and for what use cases is Cloud Spanner a good fit?

## Cloud SQL

### Summary

### Features

### Usage

### Questions

#### How to set up regional instances?

## Cloud CDN

### Summary

### Features

### Usage

### Questions

#### How do I set it up?

#### How do I cache content?

#### How do I delete a cache?

## Cloud Build

### Summary

### Features

### Usage

### Questions

#### What is the relation to Container Registry?

#### How do you set up continous builds?

## PubSub

### Summary

### Features

### Usage

### Questions

#### What are the use cases and preferred architecture for and when using PubSub?

#### What are the fundamentals of PubSub?

## Cloud Tasks

### Summary

### Features

### Usage

### Questions

## Key Management Service

### Summary

### Features

### Usage

### Questions

#### What is the default key management service that Google uses?

#### What is the customer managed encryption keys service?

#### What are the customer supplied encryption keys?

## Case Studies

Placeholder for case studies




