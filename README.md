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
      - [How do you flush memcache?](#how-do-you-flush-memcache)
  - [Cloud SQL Proxy](#cloud-sql-proxy)
    - [Summary](#summary-8)
    - [Questions](#questions-8)
      - [When is it used and how?](#when-is-it-used-and-how)
      - [How do you connect from various environments?](#how-do-you-connect-from-various-environments)
  - [Google Kubernetes Engine](#google-kubernetes-engine)
    - [Summary](#summary-9)
    - [Features](#features-8)
    - [Usage](#usage-4)
      - [How do I use environment variables?](#how-do-i-use-environment-variables)
  - [General Data Protection Regulation (GDPR)](#general-data-protection-regulation-gdpr)
    - [Summary](#summary-10)
    - [HIPAA (Health Insurance Portability and Accountability Act)](#hipaa-health-insurance-portability-and-accountability-act)
    - [COPPA](#coppa)
  - [Resource Manager](#resource-manager)
    - [Summary](#summary-11)
    - [Features](#features-9)
    - [Usage](#usage-5)
    - [Questions](#questions-9)
      - [How do I use Resource Manager programmatically?](#how-do-i-use-resource-manager-programmatically)
  - [Data Loss Prevention API](#data-loss-prevention-api)
    - [Summary](#summary-12)
    - [Features](#features-10)
    - [Usage](#usage-6)
    - [Questions](#questions-10)
      - [What are use cases for the Data Loss Prevention API?](#what-are-use-cases-for-the-data-loss-prevention-api)
  - [GSuite](#gsuite)
    - [Questions](#questions-11)
      - [How do you write an app that has permissions on GSuite products?](#how-do-you-write-an-app-that-has-permissions-on-gsuite-products)
  - [gsutil](#gsutil)
    - [Questions](#questions-12)
      - [What are all the different commands that can be used with gsutil?](#what-are-all-the-different-commands-that-can-be-used-with-gsutil)
  - [Cloud Armor](#cloud-armor)
    - [Summary](#summary-13)
    - [Features](#features-11)
    - [Questions](#questions-13)
      - [What are the use cases for Cloud Armor and what protection does it provide?](#what-are-the-use-cases-for-cloud-armor-and-what-protection-does-it-provide)
  - [Cloud Security Scanner](#cloud-security-scanner)
    - [Summary](#summary-14)
    - [Features](#features-12)
    - [Questions](#questions-14)
      - [What are the use cases for Cloud Security Scanner and what protection does it provide?](#what-are-the-use-cases-for-cloud-security-scanner-and-what-protection-does-it-provide)
  - [Cloud Storage](#cloud-storage)
    - [Summary](#summary-15)
    - [Features](#features-13)
    - [Usage](#usage-7)
    - [Questions](#questions-15)
      - [What is standard storage and what are the use cases?](#what-is-standard-storage-and-what-are-the-use-cases)
      - [What is nearline storage and what are the use cases?](#what-is-nearline-storage-and-what-are-the-use-cases)
      - [What is coldline storage and what are the use cases?](#what-is-coldline-storage-and-what-are-the-use-cases)
      - [What are signed urls and what are the use cases?](#what-are-signed-urls-and-what-are-the-use-cases)
      - [How do I set policies?](#how-do-i-set-policies)
      - [What are the bucket limitations and quotas?](#what-are-the-bucket-limitations-and-quotas)
      - [How can you optimize for heavy load?](#how-can-you-optimize-for-heavy-load)
  - [Cloud Composer](#cloud-composer)
    - [Summary](#summary-16)
    - [Features](#features-14)
    - [Questions](#questions-16)
      - [How does it work?](#how-does-it-work)
  - [Cloud Spanner](#cloud-spanner)
    - [Summary](#summary-17)
    - [Features](#features-15)
    - [Usage](#usage-8)
    - [Questions](#questions-17)
      - [Under what circumstances and for what use cases is Cloud Spanner a good fit?](#under-what-circumstances-and-for-what-use-cases-is-cloud-spanner-a-good-fit)
  - [Cloud SQL](#cloud-sql)
    - [Summary](#summary-18)
    - [Features](#features-16)
    - [Usage](#usage-9)
    - [Questions](#questions-18)
      - [How to set up regional instances?](#how-to-set-up-regional-instances)
  - [Cloud CDN](#cloud-cdn)
    - [Summary](#summary-19)
    - [Features](#features-17)
    - [Usage](#usage-10)
    - [Questions](#questions-19)
      - [How do I set it up?](#how-do-i-set-it-up)
      - [How do I cache content?](#how-do-i-cache-content)
      - [How do I delete a cache?](#how-do-i-delete-a-cache)
  - [Cloud Build](#cloud-build)
    - [Summary](#summary-20)
    - [Features](#features-18)
    - [Usage](#usage-11)
    - [Questions](#questions-20)
      - [What is the relation to Container Registry?](#what-is-the-relation-to-container-registry)
      - [How do you set up continous builds?](#how-do-you-set-up-continous-builds)
  - [PubSub](#pubsub)
    - [Summary](#summary-21)
    - [Features](#features-19)
    - [Usage](#usage-12)
    - [Questions](#questions-21)
      - [What are the use cases and preferred architecture for and when using PubSub?](#what-are-the-use-cases-and-preferred-architecture-for-and-when-using-pubsub)
      - [What are the fundamentals of PubSub?](#what-are-the-fundamentals-of-pubsub)
  - [Cloud Tasks](#cloud-tasks)
    - [Summary](#summary-22)
    - [Features](#features-20)
    - [Usage](#usage-13)
    - [Questions](#questions-22)
  - [Key Management Service](#key-management-service)
    - [Summary](#summary-23)
    - [Features](#features-21)
    - [Usage](#usage-14)
    - [Questions](#questions-23)
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

1. Your use of uptime checks is affected by any firewalls protecting your service.
   * If the resource you are checking isn't publicly available, you must configure the resource's firewall to permit incoming traffic from the uptime-check servers. See Getting IP addresses to download a list of the IP addresses.
   * If the resource you are checking doesn't have an external IP address, uptime checks are unable to reach it.
2. The uptime check doesn't load page assets or run JavaScript. The default configuration of an uptime check doesn't include authentication. You can enable authentication using the Advanced options.
For HTTP and HTTPS, the uptime check issues a GET command and retrieves the raw data. If the GET response is a redirection to another URL, the check retrieves the data from that URL. Lastly, the uptime check evaluates the data to determine if the check succeeded or failed. To succeed, two conditions must be met:

   * The HTTP status is Success.
   * The data has no required content or the required content is present. Required content is specified using the Advanced options.

***Creating uptime checks using Console***

1. In the Stackdriver Monitoring console, go to Uptime checks > Uptime checks overview:
1. In the top-right corner, click Add uptime check.
1. In the New uptime check window, fill in the fields for the check, as described in 
1. Optionally, to access configuration for port, custom headers, and authentication click Advanced options. For details, see Advanced options on this page.
1. To see the result of your uptime check, click Test. If the result isn't what you expect, see the Check failures section below, correct your configuration, and repeat the test.
1. Click Save. You cannot save an uptime check if any required field is missing. If the Save button is disabled, check for missing values. You must enter a value in the Hostname field.


***Creating uptime checks using Python***
```py
def create_uptime_check_config(project_name, host_name=None,
                               display_name=None):
    config = monitoring_v3.types.uptime_pb2.UptimeCheckConfig()
    config.display_name = display_name or 'New uptime check'
    config.monitored_resource.type = 'uptime_url'
    config.monitored_resource.labels.update(
        {'host': host_name or 'example.com'})
    config.http_check.path = '/'
    config.http_check.port = 80
    config.timeout.seconds = 10
    config.period.seconds = 300

    client = monitoring_v3.UptimeCheckServiceClient()
    new_config = client.create_uptime_check_config(project_name, config)
    pprint.pprint(new_config)
    return new_config
```

***Basic options***

To create a new uptime check, you specify values for the uptime check's configuration. When creating the uptime check in the Stackdriver Monitoring console, you fill in a form. When creating the uptime check in the API, you supply the corresponding parameters to an UptimeCheckConfig object.

1. Title: A name to identify your check. For example, Example.com uptime check.
1. Check Type: Select an HTTP, HTTPS, or TCP protocol. If you select HTTPS, the service attempts to connect over HTTPS, but doesn't validate the SSL certificate. For example, expired or self-signed certificates won't cause a check to fail.
2. Resource type: Choose one of the following resource types:
   * App Engine: App Engine applications (modules).
   * Elastic Load Balancer: AWS load balancer.
   * Instance: Compute Engine or AWS EC2 instances. In the API, this is split into gce_instance and aws_ec2_instance.
   * URL: Any IPv4 address or hostname. Path and port are entered separately.
3. Complete the connection information, depending on your check type and resource type:
   * Applies to (App Engine, ELB, or Instance): You can apply your uptime check to a single resource or to a group of resources, such as All instances. If you choose a single resource, pick one from your existing resources listed in the menu. If you use the API, fill in the monitored resource with the required resource labels, as described in the Monitored resource list.
   * Module (App Engine): Specify your application module.
   * Hostname (All except for App Engine): Specify your service's host name. For example, enter example.com.
   * Path (HTTP, HTTPS): Enter a path within your host or resource or use the default path. For example, to probe example.com, leave this field blank. To probe example.com/tester, enter /tester. Do not include the prefix example.com. In the API, leave this field blank to use the default value, /.
   * Port: Choose a port for the connection.
   * For HTTP and HTTPS checks, this option is under Advanced Options.
   * In the API, leave this field blank to use the default value: 80 for TCP or HTTP checks, and 443 for HTTPS checks.
   * Response content contains the text: Fill in a string (max 1024 bytes) whose presence in the check response indicates success. The check will fail if the string does not appear anywhere in the response. For HTTP and HTTPS check, this field appears under Advanced Options.
   * Response content does not contain the text: Fill in a string (max 1024 bytes) whose presence in the check response is a condition for success. The check will fail if the string appears anywhere in the response. For HTTP and HTTPS check, this field appears under Advanced Options.
     * In the API, this is the ContentMatcher object.
4. Check every: 1, 5, 10, or 15 minutes. For example, if you select 5 minutes, each geographic location attempts to reach your service once in every 5 minute period. Using the default 6 locations, and checking every 5 minutes, your service sees an average of 1.2 requests per minute. Checking every 1 minute, your service sees an average of 6 requests per minute.

***Advanced options***
The Advanced options section applies to HTTP, HTTPS, and TCP check types.

For HTTP and HTTPS, the uptime check issues a GET command and retrieves the raw data. If the GET response is a redirection to another URL, the check retrieves the data from that URL. Lastly, the uptime check evaluates the data to determine if the check succeeded or failed.

To succeed, two conditions must be met:

1. The HTTP status is Success.
1. The data has no required content or the required content is present. Required content is specified using the Advanced options.

These settings are optional and vary by check type:

* **HTTP Host Header**: Fill this field in to check virtual hosts. This field isn't available for TCP checks.
* **Port**: Specify a port number. For TCP checks, this field appears in Basic Options.
* **Response content contains the text**: Fill in a string (max 1024 bytes) whose presence in the check response is a condition for success. For TCP checks, this field appears under Basic Options.
* **Response content does not contain the text**: Fill in a string (max 1024 bytes) whose presence in the check response is a condition for success. For TCP checks, this field appears under Basic Options.
* **Response content matches regex**: Fill in a regex expression in the textbox. If content matches the regex expression, the uptime check succeeds. This option is only available for HTTP and HTTPS checks.
* **Response content does not match regex**: Fill in a regex expression in the textbox. If content does not match the regex expression, the uptime check succeeds. This option is only available for HTTP and HTTPS checks.
* **Locations**: Select the applicable geographic regions where your check is to receive requests. You need to select enough regions to have at least three active locations. When creating a check, the locations in each region are listed below the name of the region. New checker locations in selected regions automatically send requests to the configured destinations. To always send requests from all available locations, select Global. To send requests from all location in existing regions, but not new locations in new regions, select all the existing regions but don't select Global.
* **Custom Headers**: Supply custom headers, and encrypt them if necessary. Encryption hides the headers' values in the form. Use encryption for headers related to authentication that you don't want other members of your team to see. This field isn't available for TCP checks.
* **Healthcheck Timeout**: Specify a timeout, from 1 to 60 seconds. An uptime check fails if healthchecks from more than one location don't get a response within the configured timeout period. If only one healthcheck doesn't get a response, then the uptime check doesn't fail.
* **Authentication**: Provide a single username and password. These values are sent as an Authorization header. If you set values here, don't set a separate Authorization header; if you set an Authorization header, don't set values here. Passwords are always hidden in the form. This field isn't available for TCP checks.
* **SSL Certificate Validation**: Select Validate SSL certificates checkbox. An uptime check fails if a URL has an invalid certificate. Reasons for an invalid certificate include an expired certificate, a certificate with a domain-name mismatch, or a self-signed certificate. SSL certificate validation is only available for HTTPS checks on URL resources.

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

n BigQuery, an array is an ordered list consisting of zero or more values of the same data type. You can construct arrays of simple data types, such as `INT64`, and complex data types, such as STRUCTs. The current exception to this is the `ARRAY` data type: arrays of arrays are not supported.

With BigQuery, you can construct array literals, build arrays from subqueries using the `ARRAY` function, and aggregate values into an array using the `ARRAY_AGG` function.

You can combine arrays using functions like `ARRAY_CONCAT()`, and convert arrays to strings using `ARRAY_TO_STRING()`.

***Using array literals***

You can build an array literal in BigQuery using brackets ([ and ]). Each element in an array is separated by a comma.

```sql
SELECT [1, 2, 3] as numbers;

SELECT ["apple", "pear", "orange"] as fruit;

SELECT [true, false, true] as booleans;
```

You can also create arrays from any expressions that have compatible types. For example:

```sql
SELECT [a, b, c]
FROM
  (SELECT 5 AS a,
          37 AS b,
          406 AS c);

SELECT [a, b, c]
FROM
  (SELECT CAST(5 AS INT64) AS a,
          CAST(37 AS FLOAT64) AS b,
          406 AS c);
```

To declare a specific data type for an array, use angle brackets (< and >). For example:

```sql
SELECT ARRAY<FLOAT64>[1, 2, 3] as floats;
```

***Generating arrays of integers***

`GENERATE_ARRAY` generates an array of values from a starting and ending value and a step value. For example, the following query generates an array that contains all of the odd integers from 11 to 33, inclusive:

```sql
SELECT GENERATE_ARRAY(11, 33, 2) AS odds;

+--------------------------------------------------+
| odds                                             |
+--------------------------------------------------+
| [11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33] |
+--------------------------------------------------+
```

***Generating arrays of dates***

`GENERATE_DATE_ARRAY` generates an array of `DATEs` from a starting and ending `DATE` and a step `INTERVAL`.

You can generate a set of `DATE` values using `GENERATE_DATE_ARRAY`. For example, this query returns the current `DATE` and the following `DATEs` at 1 `WEEK` intervals up to and including a later `DATE`:

```sql
SELECT
  GENERATE_DATE_ARRAY('2017-11-21', '2017-12-31', INTERVAL 1 WEEK)
    AS date_array;
+--------------------------------------------------------------------------+
| date_array                                                               |
+--------------------------------------------------------------------------+
| [2017-11-21, 2017-11-28, 2017-12-05, 2017-12-12, 2017-12-19, 2017-12-26] |
+--------------------------------------------------------------------------+
```

***Accessing Array Elements***

Consider the following table, `sequences`:

```sql
+---------------------+
| some_numbers        |
+---------------------+
| [0, 1, 1, 2, 3, 5]  |
| [2, 4, 8, 16, 32]   |
| [5, 10]             |
+---------------------+
```

This table contains the column some_numbers of the ARRAY data type. To access elements from the arrays in this column, you must specify which type of indexing you want to use: either `OFFSET`, for zero-based indexes, or `ORDINAL`, for one-based indexes.

```sql
WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers
   UNION ALL SELECT [2, 4, 8, 16, 32] AS some_numbers
   UNION ALL SELECT [5, 10] AS some_numbers)
SELECT some_numbers,
       some_numbers[OFFSET(1)] AS offset_1,
       some_numbers[ORDINAL(1)] AS ordinal_1
FROM sequences;

+--------------------+----------+-----------+
| some_numbers       | offset_1 | ordinal_1 |
+--------------------+----------+-----------+
| [0, 1, 1, 2, 3, 5] | 1        | 0         |
| [2, 4, 8, 16, 32]  | 4        | 2         |
| [5, 10]            | 10       | 5         |
+--------------------+----------+-----------+
```

***Finding Lengths***

The `ARRAY_LENGTH()` function returns the length of an array.

```sql
WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers
   UNION ALL SELECT [2, 4, 8, 16, 32] AS some_numbers
   UNION ALL SELECT [5, 10] AS some_numbers)
SELECT some_numbers,
       ARRAY_LENGTH(some_numbers) AS len
FROM sequences;

+--------------------+--------+
| some_numbers       | len    |
+--------------------+--------+
| [0, 1, 1, 2, 3, 5] | 6      |
| [2, 4, 8, 16, 32]  | 5      |
| [5, 10]            | 2      |
+--------------------+--------+
```

***Flattening arrays***

To convert an `ARRAY` into a set of rows, also known as "flattening," use the `UNNEST` operator. `UNNEST` takes an `ARRAY` and returns a table with a single row for each element in the `ARRAY`.

Because `UNNEST` destroys the order of the `ARRAY` elements, you may wish to restore order to the table. To do so, use the optional `WITH OFFSET` clause to return an additional column with the offset for each array element, then use the `ORDER BY` clause to order the rows by their offset.

```sql
SELECT *
FROM UNNEST(['foo', 'bar', 'baz', 'qux', 'corge', 'garply', 'waldo', 'fred'])
  AS element
WITH OFFSET AS offset
ORDER BY offset;

+----------+--------+
| element  | offset |
+----------+--------+
| foo      | 0      |
| bar      | 1      |
| baz      | 2      |
| qux      | 3      |
| corge    | 4      |
| garply   | 5      |
| waldo    | 6      |
| fred     | 7      |
+----------+--------+
```

To flatten an entire column of ARRAYs while preserving the values of the other columns in each row, use a `CROSS JOIN` to join the table containing the `ARRAY` column to the `UNNEST` output of that `ARRAY` column.

This is a correlated cross join: the `UNNEST` operator references the column of ARRAYs from each row in the source table, which appears previously in the `FROM` clause. For each row N in the source table, `UNNEST` flattens the `ARRAY` from row N into a set of rows containing the ARRAY elements, and then the CROSS JOIN joins this new set of rows with the single row N from the source table.

Example

The following example uses `UNNEST` to return a row for each element in the array column. Because of the CROSS JOIN, the id column contains the id values for the row in sequences that contains each number.

```sql
WITH sequences AS
  (SELECT 1 AS id, [0, 1, 1, 2, 3, 5] AS some_numbers
   UNION ALL SELECT 2 AS id, [2, 4, 8, 16, 32] AS some_numbers
   UNION ALL SELECT 3 AS id, [5, 10] AS some_numbers)
SELECT id, flattened_numbers
FROM sequences
CROSS JOIN UNNEST(sequences.some_numbers) AS flattened_numbers;

+------+-------------------+
| id   | flattened_numbers |
+------+-------------------+
|    1 |                 0 |
|    1 |                 1 |
|    1 |                 1 |
|    1 |                 2 |
|    1 |                 3 |
|    1 |                 5 |
|    2 |                 2 |
|    2 |                 4 |
|    2 |                 8 |
|    2 |                16 |
|    2 |                32 |
|    3 |                 5 |
|    3 |                10 |
+------+-------------------+
```

***Querying Nested Arrays***

If a table contains an `ARRAY` of `STRUCTs`, you can flatten the `ARRAY` to query the fields of the `STRUCT`. You can also flatten `ARRAY` type fields of `STRUCT` values.

Querying `STRUCT` elements in an `ARRAY`

The following example uses `UNNEST` with `CROSS JOIN` to flatten an `ARRAY` of `STRUCTs`.

```sql
WITH races AS (
  SELECT "800M" AS race,
    [STRUCT("Rudisha" as name, [23.4, 26.3, 26.4, 26.1] as splits),
     STRUCT("Makhloufi" as name, [24.5, 25.4, 26.6, 26.1] as splits),
     STRUCT("Murphy" as name, [23.9, 26.0, 27.0, 26.0] as splits),
     STRUCT("Bosse" as name, [23.6, 26.2, 26.5, 27.1] as splits),
     STRUCT("Rotich" as name, [24.7, 25.6, 26.9, 26.4] as splits),
     STRUCT("Lewandowski" as name, [25.0, 25.7, 26.3, 27.2] as splits),
     STRUCT("Kipketer" as name, [23.2, 26.1, 27.3, 29.4] as splits),
     STRUCT("Berian" as name, [23.7, 26.1, 27.0, 29.3] as splits)]
       AS participants)
SELECT
  race,
  participant
FROM races r
CROSS JOIN UNNEST(r.participants) as participant;

+------+---------------------------------------+
| race | participant                           |
+------+---------------------------------------+
| 800M | {Rudisha, [23.4, 26.3, 26.4, 26.1]}   |
| 800M | {Makhloufi, [24.5, 25.4, 26.6, 26.1]} |
| 800M | {Murphy, [23.9, 26, 27, 26]}          |
| 800M | {Bosse, [23.6, 26.2, 26.5, 27.1]}     |
| 800M | {Rotich, [24.7, 25.6, 26.9, 26.4]}    |
| 800M | {Lewandowski, [25, 25.7, 26.3, 27.2]} |
| 800M | {Kipketer, [23.2, 26.1, 27.3, 29.4]}  |
| 800M | {Berian, [23.7, 26.1, 27, 29.3]}      |
+------+---------------------------------------+
```

Note that flattening arrays with a `CROSS JOIN` **excludes rows that have empty or NULL arrays**. If you want to include these rows, use a `LEFT JOIN`

***Creating Arrays From Subqueries***

A common task when working with arrays is turning a subquery result into an array. In BigQuery, you can accomplish this using the `ARRAY()` function.

For example, consider the following operation on the sequences table:

```sql
WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers
  UNION ALL SELECT [2, 4, 8, 16, 32] AS some_numbers
  UNION ALL SELECT [5, 10] AS some_numbers)
SELECT some_numbers,
  ARRAY(SELECT x * 2
        FROM UNNEST(some_numbers) AS x) AS doubled
FROM sequences;

+--------------------+---------------------+
| some_numbers       | doubled             |
+--------------------+---------------------+
| [0, 1, 1, 2, 3, 5] | [0, 2, 2, 4, 6, 10] |
| [2, 4, 8, 16, 32]  | [4, 8, 16, 32, 64]  |
| [5, 10]            | [10, 20]            |
+--------------------+---------------------+
```

***Filtering Arrays***

The following example uses a `WHERE` clause in the `ARRAY()` operator's subquery to filter the returned rows.

```sql

WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers
   UNION ALL SELECT [2, 4, 8, 16, 32] AS some_numbers
   UNION ALL SELECT [5, 10] AS some_numbers)
SELECT
  ARRAY(SELECT x * 2
        FROM UNNEST(some_numbers) AS x
        WHERE x < 5) AS doubled_less_than_five
FROM sequences;

+------------------------+
| doubled_less_than_five |
+------------------------+
| [0, 2, 2, 4, 6]        |
| [4, 8]                 |
| []                     |
+------------------------+

```

Notice that the third row contains an empty array, because the elements in the corresponding original row ([5, 10]) did not meet the filter requirement of x < 5.

You can also filter arrays by using `SELECT DISTINCT` to return only unique elements within an array.

```sql
WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers)
SELECT ARRAY(SELECT DISTINCT x
             FROM UNNEST(some_numbers) AS x) AS unique_numbers
FROM sequences;

+-----------------+
| unique_numbers  |
+-----------------+
| [0, 1, 2, 3, 5] |
+-----------------+
```

***Scanning Arrays***

To check if an array contains a specific value, use the IN operator with UNNEST. To check if an array contains a value matching a condition, use the EXISTS function with UNNEST.

Scanning for specific values
To scan an array for a specific value, use the IN operator with UNNEST.

Example

The following example returns true if the array contains the number 2.

```sql

SELECT 2 IN UNNEST([0, 1, 1, 2, 3, 5]) AS contains_value;

+----------------+
| contains_value |
+----------------+
| true           |
+----------------+
```

***Arrays and Aggregation***

With BigQuery, you can aggregate values into an array using `ARRAY_AGG()`.

```sql
WITH fruits AS
  (SELECT "apple" AS fruit
   UNION ALL SELECT "pear" AS fruit
   UNION ALL SELECT "banana" AS fruit)
SELECT ARRAY_AGG(fruit) AS fruit_basket
FROM fruits;

+-----------------------+
| fruit_basket          |
+-----------------------+
| [apple, pear, banana] |
+-----------------------+
```

The array returned by `ARRAY_AGG()` is in an arbitrary order, since the order in which the function concatenates values is not guaranteed. To order the array elements, use `ORDER BY`. For example:

You can also apply aggregate functions such as `SUM()` to the elements in an array. For example, the following query returns the sum of array elements for each row of the sequences table.

```sql
WITH sequences AS
  (SELECT [0, 1, 1, 2, 3, 5] AS some_numbers
   UNION ALL SELECT [2, 4, 8, 16, 32] AS some_numbers
   UNION ALL SELECT [5, 10] AS some_numbers)
SELECT some_numbers,
  (SELECT SUM(x)
   FROM UNNEST(s.some_numbers) x) AS sums
FROM sequences s;

+--------------------+------+
| some_numbers       | sums |
+--------------------+------+
| [0, 1, 1, 2, 3, 5] | 12   |
| [2, 4, 8, 16, 32]  | 62   |
| [5, 10]            | 15   |
+--------------------+------+
```

BigQuery also supports an aggregate function, `ARRAY_CONCAT_AGG()`, which concatenates the elements of an array column across rows.

```sql
WITH aggregate_example AS
  (SELECT [1,2] AS numbers
   UNION ALL SELECT [3,4] AS numbers
   UNION ALL SELECT [5, 6] AS numbers)
SELECT ARRAY_CONCAT_AGG(numbers) AS count_to_six_agg
FROM aggregate_example;

+--------------------------------------------------+
| count_to_six_agg                                 |
+--------------------------------------------------+
| [1, 2, 3, 4, 5, 6]                               |
+--------------------------------------------------+
```

***Converting Arrays to Strings***

The `ARRAY_TO_STRING()` function allows you to convert an `ARRAY<STRING>` to a single `STRING` value or an `ARRAY<BYTES>` to a single `BYTES` value where the resulting value is the ordered concatenation of the array elements.

The second argument is the separator that the function will insert between inputs to produce the output; this second argument must be of the same type as the elements of the first argument.

Example:

```sql
WITH greetings AS
  (SELECT ["Hello", "World"] AS greeting)
SELECT ARRAY_TO_STRING(greeting, " ") AS greetings
FROM greetings;


+-------------+
| greetings   |
+-------------+
| Hello World |
+-------------+
```

The optional third argument takes the place of NULL values in the input array.

* If you omit this argument, then the function ignores NULL array elements.
* If you provide an empty string, the function inserts a separator for NULL array elements.

***Building arrays of arrays***

BigQuery does not support building arrays of arrays directly. Instead, you must create an array of structs, with each struct containing a field of type `ARRAY`. To illustrate this, consider the following points table:

```sql
+----------+
| point    |
+----------+
| [1, 5]   |
| [2, 8]   |
| [3, 7]   |
| [4, 1]   |
| [5, 7]   |
+----------+
```

Now, let's say you wanted to create an array consisting of each point in the points table. To accomplish this, wrap the array returned from each row in a `STRUCT`, as shown below.

```sql
WITH points AS
  (SELECT [1, 5] as point
   UNION ALL SELECT [2, 8] as point
   UNION ALL SELECT [3, 7] as point
   UNION ALL SELECT [4, 1] as point
   UNION ALL SELECT [5, 7] as point)
SELECT ARRAY(
  SELECT STRUCT(point)
  FROM points)
  AS coordinates;

+----------------------------------------------------+
| coordinates                                        |
+----------------------------------------------------+
| [{[1, 5]}, {[2, 8]}, {[3, 7]}, {[4, 1]}, {[5, 7]}] |
+----------------------------------------------------+
```

#### How do you provide/restrict access? 

Remember that you cannot restrict access at table level. It is only at dataset level. 

To grant access to a BigQuery resource, assign one or more roles to a user, group, or service account. When you assign roles at the organization and project level, you provide permission to run BigQuery jobs or to manage all of a project's BigQuery resources.

You can also assign roles at the dataset level to provide access only to one or more datasets. In the Cloud IAM policy hierarchy, BigQuery datasets are child resources of projects. Tables and views are child resources of datasets — they inherit permissions from their parent dataset.

For more information on assigning roles at the dataset level, see Controlling access to datasets.

[Source](https://cloud.google.com/bigquery/docs/access-control)

BigQuery permissions
The following table describes the permissions available in BigQuery.

<table>
  <tbody><tr>
    <th width="40%">Permission</th>
    <th width="60%">Description</th>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>jobs.<wbr>create</span></code></td>
    <td>Create new jobs.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>jobs.<wbr>listAll</span></code></td>
    <td>List all jobs and retrieve metadata on any job submitted by any user.*</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>jobs.<wbr>list</span></code></td>
    <td>List all jobs and retrieve metadata on any job submitted by any user.*
      For jobs submitted by other users, details and metadata are redacted.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>jobs.<wbr>get</span></code></td>
    <td>Get data and metadata on any job.*</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>jobs.<wbr>update</span></code></td>
    <td>Cancel any job.*</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>datasets.<wbr>create</span></code></td>
    <td>Create new empty datasets.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>datasets.<wbr>delete</span></code></td>
    <td>Delete a dataset.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>datasets.<wbr>get</span></code></td>
    <td>Get metadata about a dataset.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>datasets.<wbr>update</span></code></td>
    <td>Update metadata for a dataset.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>create</span></code></td>
    <td>Create new tables.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>list</span></code></td>
    <td>List tables and metadata on tables.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>delete</span></code></td>
    <td>Delete tables.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>get</span></code></td>
    <td>Get table metadata. <br>To get table data, you need
      <code><span>bigquery.<wbr>tables.<wbr>getData</span></code>.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>getData</span></code></td>
    <td>Get table data. <br>To get table metadata, you need
      <code><span>bigquery.<wbr>tables.<wbr>get</span></code>.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>export</span></code></td>
    <td>Export table data out of BigQuery.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>update</span></code></td>
    <td><p>Update table metadata.<br>To update table data, you need
      <code>bigquery.tables.updateData</code>.</p></td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>tables.<wbr>updateData</span></code></td>
    <td><p>Update table data.<br>To update table metadata, you need
      <code>bigquery.tables.update</code>.</p></td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>routines.<wbr>create</span></code> (beta)</td>
    <td>Create new routines (functions and stored procedures).</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>routines.<wbr>list</span></code> (beta)</td>
    <td>List routines and metadata on routines.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>routines.<wbr>delete</span></code> (beta)</td>
    <td>Delete routines.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>routines.<wbr>get</span></code> (beta)</td>
    <td>Get routine definitions and metadata.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>routines.<wbr>update</span></code> (beta)</td>
    <td><p>Update routine definitions and metadata.</p></td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>transfers.<wbr>get</span></code></td>
    <td>Get transfer metadata.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>transfers.<wbr>update</span></code></td>
    <td>Create, update, and delete transfers.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>savedqueries.<wbr>create</span></code></td>
    <td>Create saved queries.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>savedqueries.<wbr>get</span></code></td>
    <td>Get metadata on saved queries.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>savedqueries.<wbr>list</span></code></td>
    <td>List saved queries.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>savedqueries.<wbr>update</span></code></td>
    <td>Update saved queries.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>savedqueries.<wbr>delete</span></code></td>
    <td>Delete saved queries.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>readsessions.<wbr>create</span></code> (beta)</td>
    <td>Create a new read session via the BigQuery
      BigQuery Storage API.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>create</span></code> (beta)</td>
    <td>Create new connections in a project.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>get</span></code> (beta)</td>
    <td>Get connection metadata. Credentials are excluded.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>list</span></code> (beta)</td>
    <td>List connections in a project.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>use</span></code> (beta)</td>
    <td>Use a connection configuration to connect to a remote data source.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>update</span></code> (beta)</td>
    <td>Update a connection and its credentials.</td>
  </tr>
  <tr>
    <td><code><span>bigquery.<wbr>connections.<wbr>delete</span></code> (beta)</td>
    <td>Delete a connection.</td>
  </tr>
</tbody></table>

* For any job you create, you automatically have the equivalent of the bigquery.jobs.get and bigquery.jobs.update permissions for that job.

BigQuery predefined Cloud IAM roles
The following table lists the predefined BigQuery Cloud IAM roles with a corresponding list of all the permissions each role includes. Note that every permission is applicable to a particular resource type.

BigQuery roles

<table>
<thead>
<tr>
<th style="width:15%;">Role</th>
<th>Title</th>
<th>Description</th>
<th>Permissions</th>
<th style="width:15%;">Lowest resource</th>
</tr>
</thead>
<tbody>
<tr id="bigquery.admin">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>admin</span></code></td>
<td class="role-title">
BigQuery Admin
</td>
<td class="role-description">
Provides permissions to manage all resources within the project. Can manage
all data within the project, and can cancel jobs from other users running
within the project.
</td>
<td class="role-permissions">
bigquery.*<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Project
</td>
</tr>
<tr id="bigquery.connectionAdmin">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>connectionAdmin</span></code></td>
<td class="role-title">
BigQuery Connection Admin
<sup><font color="red">Beta</font></sup>
</td>
<td class="role-description">
</td>
<td class="role-permissions">
bigquery.connections.*<br>
</td>
<td class="role-lowest-resource">
</td>
</tr>
<tr id="bigquery.connectionUser">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>connectionUser</span></code></td>
<td class="role-title">
BigQuery Connection User
<sup><font color="red">Beta</font></sup>
</td>
<td class="role-description">
</td>
<td class="role-permissions">
bigquery.connections.get<br>
bigquery.connections.getIamPolicy<br>
bigquery.connections.list<br>
bigquery.connections.use<br>
</td>
<td class="role-lowest-resource">
</td>
</tr>
<tr id="bigquery.dataEditor">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>dataEditor</span></code></td>
<td class="role-title">
BigQuery Data Editor
</td>
<td class="role-description">
<p>When applied to a dataset, dataEditor provides permissions to:</p>
<ul>
<li>Read the dataset's metadata and to list tables in the dataset.</li>
<li>Create, update, get, and delete the dataset's tables.</li>
</ul>
<p>
When applied at the project or organization level, this role can also
create new datasets.
</p>
</td>
<td class="role-permissions">
bigquery.datasets.create<br>
bigquery.datasets.get<br>
bigquery.datasets.getIamPolicy<br>
bigquery.datasets.updateTag<br>
bigquery.models.*<br>
bigquery.routines.*<br>
bigquery.tables.*<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Dataset
</td>
</tr>
<tr id="bigquery.dataOwner">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>dataOwner</span></code></td>
<td class="role-title">
BigQuery Data Owner
</td>
<td class="role-description">
<p>When applied to a dataset, dataOwner provides permissions to:</p>
<ul>
<li>Read, update, and delete the dataset.</li>
<li>Create, update, get, and delete the dataset's tables.</li>
</ul>
<p>
When applied at the project or organization level, this role can also
create new datasets.
</p>
</td>
<td class="role-permissions">
bigquery.datasets.*<br>
bigquery.models.*<br>
bigquery.routines.*<br>
bigquery.tables.*<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Dataset
</td>
</tr>

<!-- WARNING: PARTIALLY AUTO-GENERATED. -->
<!-- Only edit the "Description" and "Lowest Resource" cells. -->


<tr id="bigquery.dataViewer">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>dataViewer</span></code></td>
<td class="role-title">
BigQuery Data Viewer
</td>
<td class="role-description">
<p>When applied to a dataset, dataViewer provides permissions to:</p>
<ul>
<li>Read the dataset's metadata and to list tables in the dataset.</li>
<li>Read data and metadata from the dataset's tables.</li>
</ul>
<p>
When applied at the project or organization level, this role can also
enumerate all datasets in the project. Additional roles, however, are
necessary to allow the running of jobs.
</p>
</td>
<td class="role-permissions">
bigquery.datasets.get<br>
bigquery.datasets.getIamPolicy<br>
bigquery.models.getData<br>
bigquery.models.getMetadata<br>
bigquery.models.list<br>
bigquery.routines.get<br>
bigquery.routines.list<br>
bigquery.tables.export<br>
bigquery.tables.get<br>
bigquery.tables.getData<br>
bigquery.tables.list<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Dataset
</td>
</tr>
<tr id="bigquery.jobUser">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>jobUser</span></code></td>
<td class="role-title">
BigQuery Job User
</td>
<td class="role-description">
Provides permissions to run jobs, including queries, within the project. The
jobUser role can enumerate their own jobs and cancel their own jobs.
</td>
<td class="role-permissions">
bigquery.jobs.create<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Project
</td>
</tr>
<tr id="bigquery.metadataViewer">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>metadataViewer</span></code></td>
<td class="role-title">
BigQuery Metadata Viewer
</td>
<td class="role-description">
<p>When applied at the project or organization level, metadataViewer
provides permissions to:</p>
<ul>
<li>List all datasets and read metadata for all datasets in the project.</li>
<li>List all tables and views and read metadata for all tables and views
in the project.</li>
</ul>
<p>
Additional roles are necessary to allow the running of jobs.
</p>
</td>
<td class="role-permissions">
bigquery.datasets.get<br>
bigquery.datasets.getIamPolicy<br>
bigquery.models.getMetadata<br>
bigquery.models.list<br>
bigquery.routines.get<br>
bigquery.routines.list<br>
bigquery.tables.get<br>
bigquery.tables.list<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Project
</td>
</tr>
<tr id="bigquery.readSessionUser">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>readSessionUser</span></code></td>
<td class="role-title">
BigQuery Read Session User
<sup><font color="red">Beta</font></sup>
</td>
<td class="role-description">
Access to create and use read sessions
</td>
<td class="role-permissions">
bigquery.readsessions.*<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
</td>
</tr>
<tr id="bigquery.user">
<td class="role-name"><code><span>roles/</span><br><span>bigquery.<wbr>user</span></code></td>
<td class="role-title">
BigQuery User
</td>
<td class="role-description">
Provides permissions to run jobs, including queries, within the project. The
user role can enumerate their own jobs, cancel their own jobs, and enumerate
datasets within a project. Additionally, allows the creation of new datasets
within the project; the creator is granted the
<code><span>bigquery.<wbr>dataOwner</span></code> role for these new datasets.
</td>
<td class="role-permissions">
bigquery.config.get<br>
bigquery.datasets.create<br>
bigquery.datasets.get<br>
bigquery.datasets.getIamPolicy<br>
bigquery.jobs.create<br>
bigquery.jobs.list<br>
bigquery.models.list<br>
bigquery.readsessions.*<br>
bigquery.routines.list<br>
bigquery.savedqueries.get<br>
bigquery.savedqueries.list<br>
bigquery.tables.list<br>
bigquery.transfers.get<br>
resourcemanager.projects.get<br>
resourcemanager.projects.list<br>
</td>
<td class="role-lowest-resource">
Project
</td>
</tr>
</tbody>
</table>

#### What are Authorized Views?

Authorized Views can help organize and control access to your sensitive data. They don’t require you to change your logical dataset design and still enable your applications and analysts to use the full power of BigQuery.

Let’s assume you have dataset that contains tables with customer transactions. Included in the transaction record are several nested products, including product details, prices and discounts. It also includes a column with customer information. This is a table design that makes perfect sense, as BigQuery performs best when your data is denormalized.

With an authorized view, you can create a SQL view on the source data that excludes the private data, and authorize that view. If you put this view in a separate dataset (or even project), you can then set permissions for your user to access the view, without exposing the private data. If you change the view, you need to authorize it again. As a view is just a SQL query, you have the option to restrict columns or aggregate data to protect sensitive information.

#### What are some of the DML statements you can use and how should they be used?

DML - Data Manipulation Language

The BigQuery Data Manipulation Language (DML) enables you to update, insert, and delete data from your BigQuery tables.

You can execute DML statements just as you would a SELECT statement, with the following conditions:

* You must use standard SQL. To enable standard SQL, see Enabling Standard SQL.
* You cannot specify a destination table. For example, in the web UI you must have Destination Table set to No table selected.

Limitations:

* Each DML statement initiates an implicit transaction, which means that changes made by the statement are automatically committed at the end of each successful DML statement. There is no support for multi-statement transactions.

* Only the following combinations of DML statements are allowed to run concurrently on a table: 
  * UPDATE and INSERT
  * DELETE and INSERT
  * INSERT and INSERT

  Otherwise, one of the DML statements will be aborted. For example, if two UPDATE statements execute simultaneously against the table then only one of them will succeed.

* Rows that were written to a table recently via streaming (using the tabledata.insertall method) cannot be modified using UPDATE, DELETE, or MERGE statements. Recent writes are typically those that occur within the last 30 minutes. Note that all other rows in the table remain modifiable by using UPDATE, DELETE, or MERGE statements.

* Correlated subqueries within a when_clause, search_condition, merge_update_clause or merge_insert_clause are not supported for MERGE statements.

* If there are only INSERT clauses (there can be more than one), the MERGE statement behaves like an INSERT statement. An INSERT-only MERGE statement can run concurrently with other DML statements (INSERT, UPDATE, DELETE, or MERGE).

  If the MERGE statement is not limited to INSERT clauses (it has one or more UPDATE or DELETE clauses), the statement cannot run concurrently with other MERGE statements containing UPDATE or DELETE clauses. The statement also cannot run concurrently with any other DELETE or UPDATE statements.

* Queries that contain Data Manipulation Language (DML) statements cannot use a wildcard table as the target of the query. For example, a wildcard table may be used in the FROM clause of an UPDATE query, but a wildcard table cannot be used as the target of the UPDATE operation.

Syntax:

INSERT using explicit values

```sql
INSERT dataset.Inventory (product, quantity)
VALUES('top load washer', 10),
      ('front load washer', 20),
      ('dryer', 30),
      ('refrigerator', 10),
      ('microwave', 20),
      ('dishwasher', 30),
      ('oven', 5)

+-------------------+----------+--------------------+
|      product      | quantity | supply_constrained |
+-------------------+----------+--------------------+
| dishwasher        |       30 |               NULL |
| dryer             |       30 |               NULL |
| front load washer |       20 |               NULL |
| microwave         |       20 |               NULL |
| oven              |        5 |               NULL |
| refrigerator      |       10 |               NULL |
| top load washer   |       10 |               NULL |
+-------------------+----------+--------------------+
```

## Cloud Datastore

### Summary

Cloud Datastore is a highly-scalable NoSQL database for your web and mobile applications.

Cloud Datastore is a highly-scalable NoSQL database for your applications. Cloud Datastore automatically handles sharding and replication, providing you with a highly available and durable database that scales automatically to handle your applications' load. Cloud Datastore provides a myriad of capabilities such as ACID transactions, SQL-like queries, indexes and much more.

With Cloud Datastore's RESTful interface, data can easily be accessed by any deployment target. You can build solutions that span across App Engine and Compute Engine, and rely on Cloud Datastore as the integration point.

Focus on building your applications without worrying about provisioning and load anticipation. Cloud Datastore scales seamlessly and automatically with your data allowing applications to maintain high performance as they receive more traffic.

Datastore is a schemaless database, which allows you to worry less about making changes to your underlying data structure as your application evolves. Datastore provides a powerful query engine that allows you to search for data across multiple properties and sort as needed.

### Features

**Rich Admin Dashboard**

View entity statistics, query your database, view indexes, and backup/restore your data.

**Multiple Access Methods**

Access your data via our JSON API, open-source clients, or community maintained ORMs (Objectify, NDB).

**Fully Managed**

Cloud Datastore is fully managed, which means Google automatically handles sharding and replication in order to provide you with a highly available and consistent database.

**Diverse Data Types**

Datastore supports a variety of data types, including integers, floating-point numbers, strings, dates, and binary data among others.

**ACID Transactions**

Ensure the integrity of your data by executing multiple datastore operations in a single transaction with ACID characteristics, so all the grouped operations succeed or all fail.

### Usage

### Questions

#### How do I work with batches?

Cloud Firestore in Datastore mode supports batch versions of the operations which allow it to operate on multiple objects in a single Datastore mode call.

Such batch calls are faster than making separate calls for each individual entity because they incur the overhead for only one service call. If multiple entity groups are involved, the work for all the groups is performed in parallel on the server side.

***Upsert Multiple***

```python
task1 = datastore.Entity(client.key('Task', 1))

task1.update({
    'category': 'Personal',
    'done': False,
    'priority': 4,
    'description': 'Learn Cloud Datastore'
})

task2 = datastore.Entity(client.key('Task', 2))

task2.update({
    'category': 'Work',
    'done': False,
    'priority': 8,
    'description': 'Integrate Cloud Datastore'
})

client.put_multi([task1, task2])
```

***Get multiple***

```python
tasks = client.get_multi(keys)
```

***Delete multiple***

```python
client.delete_multi(keys)
```

#### How do I optimize insertions and queries?

***API Calls***

Use batch operations for your reads, writes, and deletes instead of single operations. Batch operations are more efficient because they perform multiple operations with the same overhead as a single operation.

Use asynchronous calls where available instead of synchronous calls. Asynchronous calls minimize latency impact. For example, consider an application that needs the result of a synchronous lookup() and the results of a query before it can render a response. If the lookup() and the query do not have a data dependency, there is no need to synchronously wait until the lookup() completes before initiating the query.

***Entities***

Group highly related data in entity groups. Entity groups enable ancestor queries, which return strongly consistent results. Ancestor queries also rapidly scan an entity group with minimal I/O because the entities in an entity group are stored at physically close places on Cloud Datastore servers.

Avoid writing to an entity group more than once per second. Writing at a sustained rate above that limit makes eventually consistent reads more eventual, leads to time outs for strongly consistent reads, and results in slower overall performance of your application. A batch or transactional write to an entity group counts as only a single write against this limit.

Do not include the same entity (by key) multiple times in the same commit. Including the same entity multiple times in the same commit could impact Cloud Datastore latency.

***Keys***

If you assign your own manual numeric ID or custom name to the entities you create, do not use monotonically increasing values such as:

```
1, 2, 3, …,
"Customer1", "Customer2", "Customer3", ….
"Product 1", "Product 2", "Product 3", ….
```

If an application generates large traffic, such sequential numbering could lead to hotspots that impact Cloud Datastore latency. To avoid the issue of sequential numeric IDs, obtain numeric IDs from the allocateIds() method. The allocateIds() method generates well-distributed sequences of numeric IDs.

By specifying a key or storing the generated name, you can later perform a consistent lookup() on that entity without needing issue a query to find the entity.

***Indexes***

If a property will never be needed for a query, exclude the property from indexes. Unnecessarily indexing a property could result in increased latency to achieve consistency, and increased storage costs of index entries.

Avoid having too many composite indexes. Excessive use of composite indexes could result in increased latency to achieve consistency, and increased storage costs of index entries. If you need to execute ad hoc queries on large datasets without previously defined indexes, use Google BigQuery.

Do not index properties with monotonically increasing values (such as a NOW() timestamp). Maintaining such an index could lead to hotspots that impact Cloud Datastore latency for applications with high read and write rates. For further guidance on dealing with monotonic properties, see High read/write rates for a narrow key range below.

***Queries***

If you need to access only the key from query results, use a keys-only query. A keys-only query returns results at lower latency and cost than retrieving entire entities.

If you need to access only specific properties from an entity, use a projection query. A projection query returns results at lower latency and cost than retrieving entire entities.

Likewise, if you need to access only the properties that are included in the query filter (for example, those listed in an **order by clause**), use a projection query.

Do not use offsets. Instead use cursors. Using an offset only avoids returning the skipped entities to your application, but these entities are still retrieved internally. The skipped entities affect the latency of the query, and your application is billed for the read operations required to retrieve them.

If you need strong consistency for your queries, use an ancestor query. (To use ancestor queries, you first need to structure your data for strong consistency.) An ancestor query returns strongly consistent results. Note that a non-ancestor keys-only query followed by a lookup() does not return strong results, because the non-ancestor keys-only query could get results from an index that is not consistent at the time of the query.

#### How do I avoid hotspotting?

Do not index properties with monotonically increasing values (such as a NOW() timestamp). Maintaining such an index could lead to hotspots that impact Cloud Datastore latency for applications with high read and write rates. 

By default, Cloud Datastore allocates keys using a scattered algorithm. Thus you will not normally encounter hotspotting on Cloud Datastore writes if you create new entities at a high write rate using the default ID allocation policy. There are some corner cases where you can hit this problem:

* If you create new entities at a very high rate using the legacy sequential ID allocation policy.
* If you create new entities at a very high rate and you are allocating your own IDs which are monotonically increasing.
* If you create new entities at a very high rate for a kind which previously had very few existing entities. Bigtable will start off with all entities on the same tablet server and will take some time to split the range of keys onto separate tablet servers.
* You will also see this problem if you create new entities at a high rate with a monotonically increasing indexed property like a timestamp, because these properties are the keys for rows in the index tables in Bigtable.
* Cloud Datastore prepends the namespace and the kind of the root entity group to the Bigtable row key. You can hit a hotspot if you start to write to a new namespace or kind without gradually ramping up traffic.

If you do have a key or indexed property that will be monotonically increasing then you can prepend a random hash to ensure that the keys are sharded onto multiple tablets.

Cloud Datastore prepends the namespace and the kind of the root entity group to the Bigtable row key. You can hit a hotspot if you start to write to a new namespace or kind without gradually ramping up traffic.

Read from the old entity or key first. If it is missing, then you could read from the new entity or key. A high rate of reads of non-existent entities can lead to hotspotting, so you need to be sure to gradually increase load. A better strategy is to copy the old entity to the new then delete the old. Ramp up parallel reads gradually to ensure that the new key space is well split.

Your batch job should avoid writes to sequential keys in order to prevent Bigtable hotspots. When the batch job is complete, you can read only from the new location.

Sharding using a time prefix. When the time rolls over to the next prefix then the new unsplit portion becomes a hotspot. Instead, you should gradually roll over a portion of your writes to the new prefix.

Sharding just the hottest entities. If you shard a small proportion of the total number of entities then there might not be sufficient rows between the hot entities to ensure that they stay on different splits.


#### How do I work with transactions?

Transactions have a maximum duration of 60 seconds with a 10 second idle expiration time after 30 seconds.

An operation may fail when:

* Too many concurrent modifications are attempted on the same entity.
* The transaction exceeds a resource limit.
* The Datastore mode database encounters an internal error.

Example:

```python
def transfer_funds(client, from_key, to_key, amount):
    with client.transaction():
        from_account = client.get(from_key)
        to_account = client.get(to_key)

        from_account['balance'] -= amount
        to_account['balance'] += amount

        client.put_multi([from_account, to_account])
```

Note that in order to keep our examples more succinct we sometimes omit the rollback if the transaction fails. In production code, it is important to ensure that every transaction is either explicitly committed or rolled back.

Transactions can query or lookup any number of entities. You can create, update, or delete up to 500 entities in each transaction. The maximum size of a transaction is 10 MiB.

Serializable isolation is enforced in Datastore mode databases. This means that data read or modified by a transaction cannot be concurrently modified.

One use of transactions is updating an entity with a new property value relative to its current value. The transferFunds example above does that for two entities, by withdrawing money from one account and transferring it to another. The Cloud Datastore API does not automatically retry transactions, but you can add your own logic to retry them, for instance to handle conflicts when another request updates the same entity at the same time.

As before, a transaction is necessary to handle the case where another user is attempting to create or update an entity with the same string ID. Without a transaction, if the entity does not exist and two users attempt to create it, the second overwrites the first without knowing that it happened.

Finally, you can use a transaction to read a consistent snapshot of the database. This can be useful when you need multiple reads to render a page or to export data that must be consistent. You can create read-only transaction for these cases.

Read-only transactions cannot modify entities, but in return, they do not contend with any other transactions and do not need to be retried. If you perform only reads in a regular, read-write transaction, then that transaction may contend with transaction that modify the same data.

#### Is ACID possible with Datastore?

Yes. Transactions provide ACID principles.

#### What is the difference between strong and eventual consistency?

#### What are the use-cases for them and how does it affect your choice of database?

## AppEngine

### Summary

Build highly scalable applications on a fully managed serverless platform.

Build and deploy applications on a fully managed platform. Scale your applications seamlessly from zero to planet scale without having to worry about managing the underlying infrastructure. With zero server management and zero configuration deployments, developers can focus only on building great applications without the management overhead. App Engine enables developers to stay more productive and agile by supporting popular development languages and a wide range of developer tools.

Quickly build and deploy applications using many of the popular languages like Java, PHP, Node.js, Python, C#, .Net, Ruby and Go or bring your own language runtimes and frameworks if you choose. Get started quickly with zero configuration deployments in App Engine. Manage resources from the command line, debug source code in production and run API backends easily using industry leading tools such as Cloud SDK, Cloud Source Repositories, IntelliJ IDEA, Visual Studio and PowerShell.

Focus just on writing code, without the worry of managing the underlying infrastructure. With capabilities such as automatic scaling-up and scaling-down of your application between zero and planet scale, fully managed patching and management of your servers, you can offload all your infrastructure concerns to Google. Protect your applications from security threats using App Engine firewall capabilities, Identity and Access Management (IAM) rules, and managed SSL/ TLS certificates.

Choose to run your applications in a serverless environment without the worry of over or under provisioning. App Engine automatically scales depending on your application traffic and consumes resources only when your code is running. You will only need to pay for the resources you consume.

### Features

**Popular Languages**

Build your application in Node.js, Java, Ruby, C#, Go, Python, or PHP—or bring your own language runtime

**Open & Flexible**

Custom runtimes allow you to bring any library and framework to App Engine by supplying a Docker container

**Fully Managed**

A fully managed environment lets you focus on code while App Engine manages infrastructure concerns

**Monitoring, Logging & Diagnostics**

Google Stackdriver gives you powerful application diagnostics to debug and monitor the health and performance of your app

**Application Versioning**

Easily host different versions of your app, easily create development, test, staging, and production environments

**Traffic Splitting**

Route incoming requests to different app versions, A/B test and do incremental feature rollouts

**Application Security**

Help safeguard your application by defining access rules with App Engine firewall and leverage managed SSL/TLS certificates* by default on your custom domain at no additional cost

**Services Ecosystem**

Tap a growing ecosystem of GCP services from your app including an excellent suite of cloud developer tools

### Usage

### Questions

#### How can I use Memcache with AppEngine?

App Engine supports two levels of the memcache service:

**Shared memcache** is the free default for App Engine applications. It provides cache capacity on a best-effort basis and is subject to the overall demand of all the App Engine applications using the shared memcache service.

**Dedicated memcache** provides a fixed cache capacity assigned exclusively to your application. It's billed by the GB-hour of cache size and requires billing to be enabled. Having control over cache size means your app can perform more predictably and with fewer reads from more costly durable storage.

Following are some **best practices** for using memcache:

* Handle memcache API failures gracefully. Memcache operations can fail for various reasons. Applications should be designed to catch failed operations without exposing these errors to end users. This guidance applies especially to Set operations.
* Use the batching capability of the API when possible, especially for small items. Doing so increases the performance and efficiency of your app.
* Distribute load across your memcache keyspace. Having a single or small set of memcache items represent a disproportionate amount of traffic will hinder your app from scaling. This guidance applies to both operations/sec and bandwidth. You can often alleviate this problem by explicitly sharding your data.
* For example, you can split a frequently updated counter among several keys, reading them back and summing only when you need a total. Likewise, you can split a 500K piece of data that must be read on every HTTP request across multiple keys and read them back using a single batch API call. (Even better would be to cache the value in instance memory.) For dedicated memcache, the peak access rate on a single key should be 1-2 orders of magnitude less than the per-GB rating.

It is simpler to use Memcache where data is only read because there is no risk of inconsistency between Memcache and the data store.

When using Memcache for data that is both read and modified, use the Python NDB Client Library. This is a good practice because the NDB platform code handles concurrent access coordination and error conditions robustly. As a result, your application code will be simplified.

The `incr()` and `decr()` functions are provided for atomic execution of the increment and decrement operations. Use the atomic Memcache functions where possible, including `incr()`, `decr()`, and use the `cas()` function for coordinating concurrent access. Use the Python NDB Client Library if the application uses Memcache as a way to optimize reading and writing to Cloud Datastore.

Additional resources:

[best-practices-for-app-engine-memcache](https://cloud.google.com/appengine/articles/best-practices-for-app-engine-memcache)

[app-engine-using-memcache](https://cloud.google.com/appengine/docs/standard/python/memcache/using#configuring_memcache)

#### How do you flush memcache?

You can flush it using the Google Cloud Console or you can do it programmatically using the AppEngine client library. The two methods that are available are:

* `flush_all()`
* `flush_all_async()`


## Cloud SQL Proxy

### Summary

The Cloud SQL Proxy provides secure access to your Cloud SQL Second Generation instances without having to whitelist IP addresses or configure SSL.

Accessing your Cloud SQL instance using the Cloud SQL Proxy offers these advantages:

* **Secure connections**: The proxy automatically encrypts traffic to and from the database using TLS 1.2 with a 128-bit AES cipher; SSL certificates are used to verify client and server identities.
* **Easier connection management**: The proxy handles authentication with Cloud SQL, removing the need to provide static IP addresses.

The proxy does not provide a new connectivity path; it relies on existing IP connectivity. For example, you cannot use the proxy to connect with an instance using Private IP unless the proxy is using a VPC network that has been configured for private services access.

The Cloud SQL Proxy works by having a local client, called the proxy, running in the local environment. Your application communicates with the proxy with the standard database protocol used by your database. The proxy uses a secure tunnel to communicate with its companion process running on the server.

To use the proxy, you must meet the following requirements:

* The Cloud SQL Admin API must be enabled.
* You must provide the proxy with GCP authentication credentials.
* You must provide the proxy with a valid database user account and password.
* The instance must either have a public IPv4 address, or be configured to use private IP.

The public IP address does not need to be accessible to any external address (whitelisted).

### Questions

#### When is it used and how?

Cloud SQL Proxy is used when you want to have a secure connection to a cloud database instance without having to deal with maintenance and setup.

* Install the proxy on the machine that will need to connect to the database instance.
* Configure the proxy startup options 

Credentials can be supplied in a few different ways:

* Credentials supplied in the proxy invocation command
* Credentials supplied by the local environment
* Credentials associated with the Compute Engine instance
* Credentials from an authenticated Cloud SDK client

You can use one local proxy client to connect to multiple Cloud SQL instances. The way you do this depends on whether you are using Unix sockets or TCP.

#### How do you connect from various environments?

[See the **Connecting to instances section**](https://cloud.google.com/sql/docs/mysql/how-to)

## Google Kubernetes Engine

### Summary

Kubernetes Engine (GKE) is a managed, production-ready environment for deploying containerized applications. It brings our latest innovations in developer productivity, resource efficiency, automated operations, and open source flexibility to accelerate your time to market.

Launched in 2015, Kubernetes Engine **builds** on Google's experience of running services like Gmail and YouTube in containers for over 12 years. Kubernetes Engine allows you to get up and running with Kubernetes in no time, by completely eliminating the need to install, manage, and operate your own Kubernetes clusters.

Kubernetes Engine enables rapid application development and iteration by making it easy to deploy, update, and manage your applications and services. Kubernetes Engine isn't just for stateless applications either; you can attach persistent storage, and even run a database in your cluster. Simply describe the compute, memory, and storage resources your application containers require, and Kubernetes Engine provisions and manages the underlying cloud resources automatically. Support for hardware accelerators makes it easy to run Machine Learning, General Purpose GPU, High-Performance Computing, and other workloads that benefit from specialized hardware accelerators.

Control your environment from the built-in Kubernetes Engine dashboard in Google Cloud console. Use routine health checks to detect and replace hung, or crashed, applications inside your deployments.Container replication strategies, monitoring, and automated repairs help ensure that your services are highly available and offer a seamless experience to your users. Google Site Reliability Engineers (SREs) constantly monitor your cluster and its compute, networking, and storage resources so you don't have to, giving you back time to focus on your applications.

Go from a single machine to thousands: Kubernetes Engine autoscaling allows you to handle increased user demand for your services, keeping them available when it matters most. Then, scale back in the quiet periods to save money, or schedule low-priority batch jobs to use up spare cycles. Kubernetes Engine helps you get the most out of your resource pool.

Connect to and isolate clusters no matter where you are with fine-grained network policies using Global Virtual Private Cloud (VPC) in Google Cloud. Use public services behind a single global anycast IP address for seamless load balancing. Protect against DOS and other types of edge attacks on your containers.

Kubernetes Engine runs Certified Kubernetes ensuring portability across clouds and on-premises. There's no vendor lock-in: you're free to take your applications out of Kubernetes Engine and run them anywhere Kubernetes is supported, including on your own on-premises servers. You can tailor integrations such as monitoring, logging, and CI/CD using Google Cloud Platform (GCP) and third party solutions in the ecosystem.

### Features

**Identity & Access Management**

Control access in the cluster with your Google accounts and role permissions.

**Hybrid Networking**

Reserve an IP address range for your cluster, allowing your cluster IPs to coexist with private network IPs via Google Cloud VPN.

**Security and Compliance**

Kubernetes Engine is backed by Google security team of over 750 experts and is both HIPAA and PCI DSS 3.1 compliant.

**Integrated Logging & Monitoring**

Enable Stackdriver Logging and Stackdriver Monitoring with simple checkbox configurations, making it easy to gain insight into how your application is running.

**Auto Scale**

Automatically scale your application deployment up and down based on resource utilization (CPU, memory).

**Auto Upgrade**

Automatically keep your cluster up to date with the latest release version of Kubernetes. Kubernetes release updates are quickly made available within Kubernetes Engine.

**Auto Repair**

When auto repair is enabled, if a node fails a health check Kubernetes Engine initiates a repair process for that node.

**Resource Limits**

Kubernetes allows you to specify how much CPU and memory (RAM) each Container needs, 
which is used to better organize workloads within your cluster.

**Container Isolation**

Use GKE Sandbox for a second layer of defense between containerized workloads on Google Kubernetes Engine (GKE) for enhanced workload security.

**Stateful Application Support**

Kubernetes Engine isn't just for 12-factor apps. You can attach persistent storage to containers, and even host complete databases.

**Docker Image Support**

Kubernetes Engine supports the common Docker container format.

**Fully Managed**

Kubernetes Engine clusters are fully managed by Google Site Reliability Engineers (SREs), ensuring your cluster is available and up-to-date.

**OS Built for Containers**

Kubernetes Engine runs on Container-Optimized OS, a hardened OS built and managed by Google.

**Private Container Registry**

Integrating with Google Container Registry makes it easy to store and access your private Docker images.

**Fast Consistent Builds**

Use Google Cloud Build to reliably deploy your containers on Kubernetes Engine without needing to setup authentication.

**Workload Portability, on-premises and cloud**

Kubernetes Engine runs Certified Kubernetes, enabling workload portability to other Kubernetes platforms across clouds and on-premises.

**GPU support**

Kubernetes Engine supports GPU and makes it easy to run ML, GPGPU, HPC, and other workloads that benefit from specialized hardware accelerators.

**Built-in dashboard**

GCP Console offers useful dashboards for your project's clusters and their resources. You can use these dashboards to view, inspect, manage, and delete resources in your clusters.

### Usage

To create a cluster, run the following command:

```gcloud container clusters create [CLUSTER_NAME]```

After creating your cluster, you need to get authentication credentials to interact with the cluster.

To authenticate for the cluster, run the following command:

```gcloud container clusters get-credentials [CLUSTER_NAME]```

To run hello-app in your cluster, run the following command:

```kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0```

### Questions

#### How do I scale deployments?

You can scale a Deployment by using the following command:

```kubectl scale deployment.v1.apps/nginx-deployment --replicas=10```

Assuming horizontal Pod autoscaling is enabled in your cluster, you can setup an autoscaler for your Deployment and choose the minimum and maximum number of Pods you want to run based on the CPU utilization of your existing Pods.

```kubectl autoscale deployment.v1.apps/nginx-deployment --min=10 --max=15 --cpu-percent=80```

RollingUpdate Deployments support running multiple versions of an application at the same time. When you or an autoscaler scales a RollingUpdate Deployment that is in the middle of a rollout (either in progress or paused), the Deployment controller balances the additional replicas in the existing active ReplicaSets (ReplicaSets with Pods) in order to mitigate risk. This is called proportional scaling.

For example, you are running a Deployment with 10 replicas, maxSurge=3, and maxUnavailable=2.

#### How do I check the health of VMs, pods, and services?

***Define a liveness command***

The kubelet uses liveness probes to know when to restart a Container. For example, liveness probes could catch a deadlock, where an application is running, but unable to make progress. Restarting a Container in such a state can help to make the application more available despite bugs.

The kubelet uses readiness probes to know when a Container is ready to start accepting traffic. A Pod is considered ready when all of its Containers are ready. One use of this signal is to control which Pods are used as backends for Services. When a Pod is not ready, it is removed from Service load balancers.

Many applications running for long periods of time eventually transition to broken states, and cannot recover except by being restarted. Kubernetes provides liveness probes to detect and remedy such situations.

In this exercise, you create a Pod that runs a Container based on the `k8s.gcr.io/busybox` image. Here is the configuration file for the Pod:

```yaml
apiVersion: v1
kind: Pod
metadata:
  labels:
    test: liveness
  name: liveness-exec
spec:
  containers:
  - name: liveness
    image: k8s.gcr.io/busybox
    args:
    - /bin/sh
    - -c
    - touch /tmp/healthy; sleep 30; rm -rf /tmp/healthy; sleep 600
    livenessProbe:
      exec:
        command:
        - cat
        - /tmp/healthy
      initialDelaySeconds: 5
      periodSeconds: 5
```

In the configuration file, you can see that the Pod has a single Container. The `periodSeconds` field specifies that the kubelet should perform a liveness probe every 5 seconds. The `initialDelaySeconds` field tells the kubelet that it should wait 5 second before performing the first probe. To perform a probe, the kubelet executes the command `cat /tmp/healthy` in the Container. If the command succeeds, it returns 0, and the kubelet considers the Container to be alive and healthy. If the command returns a non-zero value, the kubelet kills the Container and restarts it.

When the Container starts, it executes this command:

```bash
/bin/sh -c "touch /tmp/healthy; sleep 30; rm -rf /tmp/healthy; sleep 600"
```

For the first 30 seconds of the Container’s life, there is a `/tmp/healthy` file. So during the first 30 seconds, the command c`at /tmp/healthy` returns a success code. After 30 seconds, `cat /tmp/healthy` returns a failure code.

***Define a liveness HTTP request***

Another kind of liveness probe uses an HTTP GET request. Here is the configuration file for a Pod that runs a container based on the k8s.gcr.io/liveness image.

```yaml
apiVersion: v1
kind: Pod
metadata:
  labels:
    test: liveness
  name: liveness-http
spec:
  containers:
  - name: liveness
    image: k8s.gcr.io/liveness
    args:
    - /server
    livenessProbe:
      httpGet:
        path: /healthz
        port: 8080
        httpHeaders:
        - name: Custom-Header
          value: Awesome
      initialDelaySeconds: 3
      periodSeconds: 3
```

In the configuration file, you can see that the Pod has a single Container. The `periodSeconds` field specifies that the kubelet should perform a liveness probe every 3 seconds. The `initialDelaySeconds` field tells the kubelet that it should wait 3 seconds before performing the first probe. To perform a probe, the kubelet sends an HTTP GET request to the server that is running in the Container and listening on port 8080. If the handler for the server’s `/healthz` path returns a success code, the kubelet considers the Container to be alive and healthy. If the handler returns a failure code, the kubelet kills the Container and restarts it.

Any code greater than or equal to 200 and less than 400 indicates success. Any other code indicates failure.

***Define a TCP liveness probe***

A third type of liveness probe uses a TCP Socket. With this configuration, the kubelet will attempt to open a socket to your container on the specified port. If it can establish a connection, the container is considered healthy, if it can’t it is considered a failure.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: goproxy
  labels:
    app: goproxy
spec:
  containers:
  - name: goproxy
    image: k8s.gcr.io/goproxy:0.1
    ports:
    - containerPort: 8080
    readinessProbe:
      tcpSocket:
        port: 8080
      initialDelaySeconds: 5
      periodSeconds: 10
    livenessProbe:
      tcpSocket:
        port: 8080
      initialDelaySeconds: 15
      periodSeconds: 20
```

As you can see, configuration for a TCP check is quite similar to an HTTP check. This example uses both readiness and liveness probes. The kubelet will send the first readiness probe 5 seconds after the container starts. This will attempt to connect to the `goproxy` container on port 8080. If the probe succeeds, the pod will be marked as ready. The kubelet will continue to run this check every 10 seconds.

***Define readiness probes***

Sometimes, applications are temporarily unable to serve traffic. For example, an application might need to load large data or configuration files during startup, or depend on external services after startup. In such cases, you don’t want to kill the application, but you don’t want to send it requests either. Kubernetes provides readiness probes to detect and mitigate these situations. A pod with containers reporting that they are not ready does not receive traffic through Kubernetes Services.

Readiness probes are configured similarly to liveness probes. The only difference is that you use the **readinessProbe** field instead of the **livenessProbe** field.

```yaml
readinessProbe:
  exec:
    command:
    - cat
    - /tmp/healthy
  initialDelaySeconds: 5
  periodSeconds: 5
```

Probes have a number of fields that you can use to more precisely control the behavior of liveness and readiness checks:

* **initialDelaySeconds**: Number of seconds after the container has started before liveness or readiness probes are initiated.
* **periodSeconds**: How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1.
* **timeoutSeconds**: Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1.
* **successThreshold**: Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness. Minimum value is 1.
* **failureThreshold**: When a Pod starts and the probe fails, Kubernetes will try failureThreshold times before giving up. Giving up in case of liveness probe means restarting the Pod. In case of readiness probe the Pod will be marked Unready. Defaults to 3. Minimum value is 1.

HTTP probes have additional fields that can be set on httpGet:

* **host**: Host name to connect to, defaults to the pod IP. You probably want to set “Host” in httpHeaders instead.
* **scheme**: Scheme to use for connecting to the host (HTTP or HTTPS). Defaults to HTTP.
* **path**: Path to access on the HTTP server.
* **httpHeaders**: Custom headers to set in the request. HTTP allows repeated headers.
* **port**: Name or number of the port to access on the container. Number must be in the range 1 to 65535.

#### What are the limits of gcloud when it comes to GKE? 

GKE's per-project limits are:

* Maximum of 50 clusters per zone, plus 50 regional clusters per region.
GKE's per-cluster limits are:

* Maximum of 5000 nodes per cluster.
* Maximum of 1000 nodes per node pool.
* Maximum of 1000 nodes per cluster if you use the GKE ingress controller.
* 100 Pods per node.
* 300,000 containers.

The rate limit for the GKE API is 10 requests per second.

You might also encounter Compute Engine resource quotas. Additionally, for projects with default regional Compute Engine CPUs quota, container clusters are limited to three per region.

To examine these quotas, use the `kubectl get resourcequota gke-resource-quotas -o yaml` command. To view the `gke-resource-quotas` object for a given Namespace, specify the Namespace by adding the `--namespace` option.

#### What are the things that kubectl can do?

[kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

[Full kubectl command reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-)

## Managed Instance Groups

### Summary

Managed instance groups (MIGs) allow you to operate applications on multiple identical VMs. You can make your workloads scalable and highly available by taking advantage of automated MIG services, including: autoscaling, autohealing, regional (multi-zone) deployment, and auto-updating.

A managed instance group contains one or more virtual machine instances that are controlled using an instance template. To update instances in a managed instance group, you can make update requests to the group as a whole, using the Managed Instance Group Updater feature.
The Managed Instance Group Updater allows you to easily deploy new versions of software to instances in your managed instance groups, while controlling the speed of deployment, the level of disruption to your service, and the scope of the update. The Updater offers two primary advantages:

* The rollout of an update happens automatically to your specifications, without the need for additional user input after the initial request.
* You can perform partial rollouts which allows for canary testing.

By allowing new software to be deployed inside an existing managed instance group, there is no need for you to reconfigure the instance group or reconnect load balancing, autoscaling, or autohealing each time a new version of software is rolled out. Without the Updater, new software versions must be deployed either by creating a new managed instance group with a new software version, requiring additional set up each time, or through a manual, user-initiated, instance-by-instance recreate. Both of these approaches require significant manual steps throughout the process.

### Questions

#### How do you scale and update deployments?

Here are things to keep in mind when making a rolling update:

* Updates are intent based. When you make the initial update request, the API returns a successful response to confirm that the request was valid but that does not indicate that the update was successful. You must check the status of the managed instance group to determine if your update was deployed successfully.
* The Instance Group Updater API is a declarative API. The API expects a request to specify the desired post update configuration of the managed instance group, rather than an explicit function call.
* The Updater feature supports up to two instance template versions in your managed instance group. This means that you can specify two different instance template versions for your managed instance group, which is useful for performing canary updates.

To start a basic rolling update where the update is applied to 100% of the instances in the group:

Console:

1. Go to the Instance groups page in the GCP Console.
2. Select the instance group you want to update.
3. At the top of the page, click Rolling update.
4. Under Template, pull down the drop down menu and select the new template to update to.
5. For the target size, enter 100% to update all instances.
6. Optionally, you can toggle configuration options like whether the update is proactive (the group actively replaces instances) or opportunistic (the group does not actively replace instances but applies the update when instances are replaced from other means). You can also supply max surge, max unavailable options, and minimum wait time.
7. Click Update to start the update.

GCloud:

```shell
gcloud compute instance-groups managed rolling-action start-update [INSTANCE_GROUP] \
    --version template=[INSTANCE_TEMPLATE] [--zone [ZONE] | --region [REGION]]
```

***Configuring options for your update***

Set the **maxSurge** property to allow the Updater to temporarily create new instances above the targetSize during the update. For example, if you set maxSurge to 5, the managed instance group will create up to 5 new instances above your target size, with the new instance template. Setting a higher maxSurge value speeds up your update, at the cost of additional instances, which are billed according to the Compute Engine price sheet.

Set the **maxUnavailable** configuration so that only a certain number of instances are unavailable at any time during the update. For example, if you set maxUnavailable to 5, then only 5 instances will be taken offline for updating at a time. Use this parameter to control how disruptive the update is to your service and to control the rate at which the update is deployed.

Set the **minReadySeconds** to specify the amount of time to wait before considering a newly created or restarted instance as updated. Use this feature to control the rate at which the update is deployed. The timer starts when both of the following conditions are satisfied:

Set the minimal action property to control the minimum action that Updater must perform to update the instances in the group. For example, if you set **REPLACE** as the minimum action, then all instances that are affected will be deleted and replaced with a new instance, whether or not it is necessary. Applicable actions are `REPLACE` or `RESTART`:

`RESTART`: Restarts the instance (performs a stop and start request). Note that if your update request requires that the instance be replaced to pick up the changes (for example, changing the image would require that the instance is deleted and replaced), it will be forced to perform REPLACE.


`REPLACE`: Deletes the existing instance and creates a new instance from the target template. The Updater creates a brand new instance with all new instance properties, such as new internal and external IP addresses.

***Additional updating deployments***

[Link](https://cloud.google.com/compute/docs/instance-groups/rolling-out-updates-to-managed-instance-groups)

#### How do you scale MIGs based on various parameters?

***Scaling based on CPU or load balancing serving capacity***

Console:

1. Go to the Instance Groups page.
2. If you have an instance group, select it and click Edit group. If you don't have an instance group, click Create instance group.
3. Under Autoscaling, select On.
4. Under Autoscale based on, select CPU usage.
5. Enter the Target CPU usage. This will be treated as a percentage. For example, for 60% CPU usage, enter 60.
6. Provide a number for the maximum number of instances that you want in this instance group. You can also set the minimum number of instances and the cool down period. The cool down period is the number of seconds the autoscaler should wait after a virtual machine has started before the autoscaler starts collecting information from it. This accounts for the amount of time it can take for a virtual machine to initialize, during which the collected usage is not reliable for autoscaling. The default cool down period is 60 seconds.
7. Save your changes.

GCloud:

```shell
gcloud compute instance-groups managed set-autoscaling example-managed-instance-group \
    --max-num-replicas 20 \
    --target-cpu-utilization 0.75 \
    --cool-down-period 90
```

***Scaling based on HTTP(S) load balancing serving capacity***

Console:

1. Go to the Instance Groups pane in the Google Cloud Platform Console.
1. If you have an instance group, select it and click Edit group. If you don't, click Create instance group.
1. Under Autoscaling, select On.
1. Under Autoscale based on, select HTTP load balancing usage.
1. Enter the Target load balancing usage. This will be treated as a percentage. For example, for 60% HTTP load balancing usage, enter 60.
1. Provide a number for the maximum number of instances that you want in this instance group. You can also set the minimum number of instances and the cool down period. The cool down period is the number of seconds the autoscaler should wait after a virtual machine has started before the autoscaler starts collecting information from it. This accounts for the amount of time it might take for the instance to initialize, during which the collected usage is not reliable for autoscaling. The default cool down period is 60 seconds.
1. Save your changes.

GCloud:

```shell
gcloud compute instance-groups managed set-autoscaling example-managed-instance-group \
    --max-num-replicas 20 \
    --target-load-balancing-utilization 0.6 \
    --cool-down-period 90
```

***Scaling Based on Stackdriver Monitoring Metrics***

You can set up autoscaler to scale based on the following metric types:

* Scale using per-instance metrics where the selected metric provides data for each instance in the managed instance group indicating resource utilization.
* Scale using per-group metrics (Beta) where the group scales based on a metric that provides a value related to the whole managed instance group.

[See Scaling Based on Stackdriver Monitoring Metrics](https://cloud.google.com/compute/docs/autoscaler/scaling-stackdriver-monitoring-metrics)

## Deployment Manager

### Summary

Create and manage cloud resources with simple templates. 

Google Cloud Deployment Manager allows you to specify all the resources needed for your application in a declarative format using yaml. You can also use Python or Jinja2 templates to parameterize the configuration and allow reuse of common deployment paradigms such as a load balanced, auto-scaled instance group. Treat your configuration as code and perform repeatable deployments.

By creating configuration files which define the resources, the process of creating those resources can be repeated over and over with consistent results.

Many tools use an imperative approach, requiring the user to define the steps to take to create and configure resources. A declarative approach allows the user to specify what the configuration should be and let the system figure out the steps to take.
The user can focus on the set of resources which comprise the application or service instead of deploying each resource separately.

Templates allow the use of building blocks to create abstractions or sets of resources that are typically deployed together (e.g. an instance template, instance group, and autoscaler). These templates can be parameterized to allow them to be used over and over by changing input values to define what image to deploy, the zone in which to deploy, or how many virtual machines to deploy.


### Features

**Parallel deployment**

Deploy many resources at one time, in parallel.

**Templates**

Python and Jinja2 template to programmatically control what gets deployed.

**Updates**

Add, delete, or change resources in the deployment.

**Input and output parameters**

Pass variables (e.g. zone, machine size, number of machines, state: test, prod, staging) into your templates and get output values back (e.g. IP address assigned, link to the instance).

**Schema files**

JSON schema for defining and constraining parameters.

**References**

One resource definition can reference another resource creating dependencies and controlling the order of resource creation.

**Preview mode**

See what changes Deployment Manager will make on a create or update operation before you commit the changes.

**Console UI**

View your deployments in the Google Cloud Console where you can see one view of your whole deployment in a hierarchical view.

### Questions

#### How do I create templates?

A template is a separate file from your configuration that defines a set of resources. You import a template into your configuration and Deployment Manager expands the template and inlines the contents during deployment, leaving a cleaner, simpler configuration file. After it has been imported, you can use a template in the same way you use a resource type.

A template can use other templates and Deployment Manager recursively expands templates when they are used in a configuration, so that the final result after templates have been expanded would be as if you had written the configuration without templates. For example, a configuration with templates could look like this:

```yaml
imports:
- path: vm-template.jinja

resources:
- name: vm-instance
  type: vm-template.jinja
```

After Deployment Manager expands the templates, the full configuration looks like this, without additional work on your part:

```yaml
resources:
- name: vm-instance
  type: compute.v1.instance
  properties:
    disks:
    - deviceName: boot
      type: PERSISTENT
      boot: true
      autoDelete: true
      initializeParams:
        sourceImage: https://www.googleapis.com/compute/v1/projects/debian-cloud/global/images/family/debian-9
    machineType: https://www.googleapis.com/compute/v1/projects/myproject/zones/us-central1-f/machineTypes/f1-micro
    networkInterfaces:
    - network: $(ref.a-new-network.selfLink)
      accessConfigs:
      - name: External NAT
        type: ONE_TO_ONE_NAT
    zone: us-central1-f
```

You can write templates in your choice of Python 2.7 or Jinja2. Python templates are more powerful for complex deployments, and more flexible when your deployments to get more complex over time. If you are familiar with Python, we recommend using Python for your templates.

You can also use the Jinja2 templating language for your templates. With Jinja2, you can write your templates in YAML, and use features such as control structures and expressions to customize the templates.

***Creating a Template***

You can create a deployment using a configuration at any time, but as you create more complex configurations, you should create and use templates for more flexible and robust configurations.

A template is a separate file from your configuration that defines a set of resources. You import a template into your configuration and Deployment Manager expands the template and inlines the contents during deployment, leaving a cleaner, simpler configuration file. After it has been imported, you can use a template in the same way you use a resource type.

A template can use other templates and Deployment Manager recursively expands templates when they are used in a configuration, so that the final result after templates have been expanded would be as if you had written the configuration without templates. For example, a configuration with templates could look like this:

```yaml
imports:
- path: vm-template.jinja

resources:
- name: vm-instance
  type: vm-template.jinja
After Deployment Manager expands the templates, the full configuration looks like this, without additional work on your part:

resources:
- name: vm-instance
  type: compute.v1.instance
  properties:
    disks:
    - deviceName: boot
      type: PERSISTENT
      boot: true
      autoDelete: true
      initializeParams:
        sourceImage: https://www.googleapis.com/compute/v1/projects/debian-cloud/global/images/family/debian-9
    machineType: https://www.googleapis.com/compute/v1/projects/myproject/zones/us-central1-f/machineTypes/f1-micro
    networkInterfaces:
    - network: $(ref.a-new-network.selfLink)
      accessConfigs:
      - name: External NAT
        type: ONE_TO_ONE_NAT
    zone: us-central1-f
```

Example Python template:

```py
"""Creates the virtual machine."""

COMPUTE_URL_BASE = 'https://www.googleapis.com/compute/v1/'


def GenerateConfig(unused_context):
  """Creates the first virtual machine."""

  resources = [{
      'name': 'the-first-vm',
      'type': 'compute.v1.instance',
      'properties': {
          'zone': 'us-central1-f',
          'machineType': ''.join([COMPUTE_URL_BASE, 'projects/[MY_PROJECT]',
                                  '/zones/us-central1-f/',
                                  'machineTypes/f1-micro']),
          'disks': [{
              'deviceName': 'boot',
              'type': 'PERSISTENT',
              'boot': True,
              'autoDelete': True,
              'initializeParams': {
                  'sourceImage': ''.join([COMPUTE_URL_BASE, 'projects/',
                                          'debian-cloud/global/',
                                          'images/family/debian-9'])
              }
          }],
          'networkInterfaces': [{
              'network': '$(ref.a-new-network.selfLink)',
              'accessConfigs': [{
                  'name': 'External NAT',
                  'type': 'ONE_TO_ONE_NAT'
              }]
          }]
      }
  }]
  return {'resources': resources}
```

Add the templates:

```yaml
imports:
- path: vm-template.py

resources:
- name: vm-1
  type: vm-template.py
- name: a-new-network
  type: compute.v1.network
  properties:
    routingConfig:
      routingMode: REGIONAL
    autoCreateSubnetworks: true
```

***Writing Jinja2 or Python templates***

You can write templates in your choice of Python 2.7 or Jinja2. Python templates are more powerful for complex deployments, and more flexible when your deployments to get more complex over time. If you are familiar with Python, we recommend using Python for your templates.

You can also use the Jinja2 templating language for your templates. With Jinja2, you can write your templates in YAML, and use features such as control structures and expressions to customize the templates.

If you aren't familiar with Python or want to write simple templates without using Python, use Jinja2. The rest of this guide includes examples in both Jinja and Python.

***Python templates***

If you choose to write templates in Python, your templates must meet these requirements:

* The template must be written in Python 2.7
* The template must define a method called GenerateConfig() or generate_config(). If you use both method names in the same template, the generate_config() method will take precedence.
* The method must return a Python dictionary.

***Deploying your template***

```bash
gcloud deployment-manager deployments create deployment-with-templates --config two-vms.yaml
```

#### How do I use references?

As you continue development, the resources in your configuration might start to depend on other resources in the same configuration. For example, you might want to add a virtual machine to a new network, and create both these resources in the same deployment. However, Deployment Manager creates resources in parallel, so there is no guarantee that the network is created before the virtual machine.

To help you define these dependencies correctly in your configuration file, you use references to refer to other resources.

References are useful because:

* **Deployment Manager resolves resources in dependent order**, which means that if resource A references resource B, resource B is created first. For example, if a VM instance references a new network in the configuration, Deployment Manager always creates the network before creating the instance.

* **You can use references to access properties of resources**. For example, when you define a virtual machine in your configuration, you do not yet know its IP address. However, you can still use a reference to the IP address. When you deploy your configuration, the VM is created first, and Deployment Manager gets the external IP address when it is available.

To use references, use this syntax in your configuration:

```$(ref.RESOURCE_NAME.PROPERTY)```

Example - Adding a network definition:

Adding the following resource to the yaml file:

```yaml
- name: a-new-network
  type: compute.v1.network
  properties:
    IPv4Range: 10.0.0.0/24
```

Then using the reference to specify a value:
```yaml
networkInterfaces:
- network: $(ref.a-new-network.selfLink)
```

Redeploying the configuration:
```bash
gcloud deployment-manager deployments create deployment-with-references --config two-vms.yaml
```

#### How do I use environment variables?

Templates also support the use of custom template properties and predefined environment variables so that you can reuse templates across zones, regions, or even projects.

For example, you can use an arbitrary template property in place of hard coding a specific zone value in your template. Anytime you use the template, you include the template and provide a value for the zone in the top-level configuration.

Reference an arbitrary template property using this syntax in your templates:

```python
context.properties["property-name"]
```

For example, the following template uses the following template properties: zone, machineType, and network:

```py
"""Creates the virtual machine."""

def GenerateConfig(context):
  """Creates the virtual machine with environment variables."""

  resources = [{
      'name': 'example',
      'type': 'compute.v1.instance',
      'properties': {
          'zone': context.properties['zone'],
          'machineType': ''.join(['https://www.googleapis.com/compute/v1/',
                                  'projects/my-project/zones/',
                                  context.properties['zone'], '/machineTypes/',
                                  context.properties['machineType']]),
          'disks': [{
              'deviceName': 'boot',
              'type': 'PERSISTENT',
              'boot': True,
              'autoDelete': True,
              'initializeParams': {
                  'sourceImage': ''.join(['https://www.googleapis.com/compute/v1/', 'projects/',
                                          'debian-cloud/global/',
                                          'images/family/debian-8'])
              }
          }],
          'networkInterfaces': [{
              'network': '$(ref.' + context.properties['network']
                         + '.selfLink)',
              'accessConfigs': [{
                  'name': 'External NAT',
                  'type': 'ONE_TO_ONE_NAT'
              }]
          }]
      }
  }]
  return {'resources': resources}
```

Then you would set the value of this template property at the top-level configuration or the parent template:

```yaml
resources:
- name: the-first-vm
  type: vm-template.jinja
  properties:
    machineType: f1-micro # Sets the 'machineType' template property
    zone: us-central1-f # Sets the 'zone' template property
    network: example-network # Sets the 'network' template property
- name: the-second-vm
```

In addition to template properties, you can also reference environment variables that are prepopulated with specific information about your deployment. Valid environment variables include the deployment name, the project ID, the name property of your resource, and the type of your configuration. For more details about each environment variable, read the Environment Variables documentation.

You can reference an environment variable using this syntax:

```py
context.env['variable-name']
```
For example, the following template uses the name and project environment variables

```py

"""Creates the virtual machine."""

COMPUTE_URL_BASE = 'https://www.googleapis.com/compute/v1/'


def GenerateConfig(context):
  """Creates the virtual machine with environment variables."""

  resources = [{
      'name': context.env['name'],
      'type': 'compute.v1.instance',
      'properties': {
          'zone': context.properties['zone'],
          'machineType': ''.join([COMPUTE_URL_BASE, 'projects/',
                                  context.env['project'], '/zones/',
                                  context.properties['zone'], '/machineTypes/',
                                  context.properties['machineType']]),
          'disks': [{
              'deviceName': 'boot',
              'type': 'PERSISTENT',
              'boot': True,
              'autoDelete': True,
              'initializeParams': {
                  'sourceImage': ''.join([COMPUTE_URL_BASE, 'projects/',
                                          'debian-cloud/global/',
                                          'images/family/debian-9'])
              }
          }],
          'networkInterfaces': [{
              'network': '$(ref.' + context.properties['network']
                         + '.selfLink)',
              'accessConfigs': [{
                  'name': 'External NAT',
                  'type': 'ONE_TO_ONE_NAT'
              }]
          }]
      }
  }]
  return {'resources': resources}
```

## General Data Protection Regulation (GDPR)

### Summary

The General Data Protection Regulation (EU) 2016/679 (GDPR) is a regulation in EU law on data protection and privacy for all individual citizens of the European Union (EU) and the European Economic Area (EEA). It also addresses the transfer of personal data outside the EU and EEA areas. The GDPR aims primarily to give control to individuals over their personal data and to simplify the regulatory environment for international business by unifying the regulation within the EU.[1] Superseding the Data Protection Directive 95/46/EC, the regulation contains provisions and requirements pertaining to the processing of personal data of individuals (formally called data subjects in the GDPR) inside the EEA, and applies to any enterprise established in the EEA or—regardless of its location and the data subjects' citizenship—that is processing the personal information of data subjects inside the EEA.

Controllers of personal data must put in place appropriate technical and organisational measures to implement the data protection principles. Business processes that handle personal data must be designed and built with consideration of the principles and provide safeguards to protect data (for example, using pseudonymization or full anonymization where appropriate), and use the highest-possible privacy settings by default, so that the datasets are not publicly available without explicit, informed consent, and cannot be used to identify a subject without additional information (which must stored separately). No personal data may be processed unless this processing is done under a lawful basis specified by the regulation, or unless the data controller or processor has received an unambiguous and individualized affirmation of consent from the data subject. The data subject has the right to revoke this consent at any time.

A processor of personal data must clearly disclose any data collection, declare the lawful basis and purpose for data processing, and state how long data is being retained and if it is being shared with any third parties or outside of the EEA. Data subjects have the right to request a portable copy of the data collected by a processor in a common format, and the right to have their data erased under certain circumstances. Public authorities, and businesses whose core activities centre around regular or systematic processing of personal data, are required to employ a data protection officer (DPO), who is responsible for managing compliance with the GDPR. Businesses must report any data breaches within 72 hours if they have an adverse effect on user privacy. In some cases, violators of the GDPR may be fined up to €20 million or up to 4% of the annual worldwide turnover of the preceding financial year in case of an enterprise, whichever is greater.

The GDPR was adopted on 14 April 2016, and became enforceable beginning 25 May 2018. As the GDPR is a regulation, not a directive, it is directly binding and applicable, but does provide flexibility for certain aspects of the regulation to be adjusted by individual member states.

### HIPAA (Health Insurance Portability and Accountability Act)

HIPAA (Health Insurance Portability and Accountability Act of 1996) is United States legislation that provides data privacy and security provisions for safeguarding medical information. The law has emerged into greater prominence in recent years with the proliferation of health data breaches caused by cyberattacks and ransomware attacks on health insurers and providers.

***HIPAA Privacy Rule***

The Standards for Privacy of Individually Identifiable Health Information, commonly known as the HIPAA Privacy Rule, establishes the first national standards in the United States to protect patients' personal or protected health information (PHI).

HHS issued the rule to limit the use and disclosure of sensitive PHI. It seeks to protect the privacy of patients by requiring doctors to provide patients with an account of each entity to which the doctor discloses PHI for billing and administrative purposes, while still allowing relevant health information to flow through the proper channels. 

The privacy rule also guarantees patients the right to receive their own PHI, upon request, from healthcare providers covered by HIPAA.

The HIPAA Privacy Rule applies to organizations that are considered HIPAA-covered entities, including health plans, healthcare clearinghouses and healthcare providers. In addition, the HIPAA Privacy Rule requires covered entities that work with a HIPAA business associate to produce a contract that imposes specific safeguards on the PHI that the business associate uses or discloses.

The HIPAA Privacy Rule protects all individually identifiable health information that is held or transmitted by a covered entity or a business associate. This information can be held in any form, including digital, paper or oral. This individually identifiable health information is also known as PHI under the Privacy Rule.

What is considered protected health information under HIPAA?
PHI includes:

* a patient's name, address, birth date and Social Security number;
* an individual's physical or mental health condition;
* any care provided to an individual; or
* information concerning the payment for the care provided to the individual that identifies the patient, or information for which there is a reasonable basis to believe could be used to identify the patient.

The HIPAA Privacy Rule does not consider employment records -- including information about education, as well as other records subject to or defined in the Family Educational Rights and Privacy Act -- as PHI.

For de-identified data, however, there are no restrictions to its use or disclosure. De-identified data does not identify or provide information that could identify an individual.

The Privacy Rule lays out certain administrative requirements that covered entities must have in place.

These requirements include the following:

* A privacy official must be appointed who is responsible for developing and implementing policies and procedures at a covered entity.
* Employees, including volunteers and trainees, must be trained on policies and procedures.
* Appropriate administrative, technical and physical safeguards must be maintained to protect the privacy of PHI in a covered entity.
* A process for individuals to make complaints concerning policies and procedures must be in place at a covered entity.
* If PHI is disclosed in violation of its policies and procedures, a covered entity must mitigate, to the furthest extent actionable, any harmful effects.

### COPPA

The Children's Online Privacy Protection Act (COPPA) is a law created to protect the privacy of children under 13. The Act was passed by the U.S. Congress in 1998 and took effect in April 2000. COPPA is managed by the Federal Trade Commission (FTC).

The Act specifies:

* That sites must require parental consent for the collection or use of any personal information of young Web site users.
* What must be included in a privacy policy, including the requirement that the policy itself be posted anywhere data is collected.
* When and how to seek verifiable consent from a parent or guardian.
* What responsibilities the operator of a Web site legally holds with regards to children's privacy and safety online, including restrictions on the types and methods of marketing targeting those under 13.

COPPA was passed to address the rapid growth of online marketing techniques in the 1990s that were targeting children. Various Web sites were collecting personal data from children without parental knowledge or consent. Research published by the Center for Media Education showed that children did not understand the potential negative outcomes of revealing personal information online. In the wake of media reports demonstrating the ease of gathering private data from children, the public pressured Congress to legislate.

Although COPPA does not specifically define how parental consent should be gained, the (FTC) has established guidelines to help Web site operators ensure compliance with the Act. These suggestions include:

* Clear display of downloadable consent forms that may be mailed or faxed to to the operator.
* Requiring that a parent use a credit card to authenticate age and identity.
* Requiring that a parent call a toll-free phone number.
* Accepting an email from a parent that includes a digital signature.

COPPA requires that site operators allow parents to review any information collected from their children. In practice, this means that any relevant site has to provide full access to all user records, profiles and log-in information when a parent requests it. The FTC has stipulated that parents may delete certain information but may not otherwise alter it.

Any Web site that collects information from children under the age of 13 has to abide by COPPA. The Act affects many popular sites like MySpace.com, Facebook.com, Friendster.com, Xanga.com and other social networking sites.

COPPA should not be confused with COPA, the Child Online Protection Act, which was relevant to the exposure of children to online pornography. COPA was ruled to be unconstitutional and was placed under injunction.



## Resource Manager

### Summary

Hierarchically manage resources by project, folder, and organization.

Google Cloud Platform provides resource containers such as organizations, folders, and projects that allow you to group and hierarchically organize other GCP resources. This hierarchical organization lets you easily manage common aspects of your resources such as access control and configuration settings. Resource Manager enables you to programmatically manage these resource containers.

Create an organization that contains all of your projects and resources. Create folders to group projects by department, team, application, or environment. Easily modify your Cloud Identity and Access Management policies for your organization and folders, and the changes will apply across all the projects and resources. You can also edit projects directly.

Resources are organized hierarchically. An organization is the root node in the hierarchy and has projects and folders as children. Folders can contain projects or other folders. All other resources are the children of projects. Each resource has exactly one parent. Set access control policies and configuration settings at a parent resource, and the policies and settings are inherited by the children resources.

Programmatically create, manage, and delete projects and folders that belong to your organization. You can also undelete or recover projects that you didn’t mean to delete.

### Features

**Organization**

The organization resource represents an organization such as your company and is the root node in the Google Cloud Platform resource hierarchy.

**Organization policies**

Centrally control your organization’s resources. Restrict allowed configurations across your entire cloud resource hierarchy programmatically.

**Cloud IAM policies**

Create and manage IAM access control policies for your organization and projects. Control what access members of the project have to manage virtual machines, logs, and much more.

**Asset inventory**

Use asset inventory to get an org-wide snapshot of your inventory for a wide variety of GCP resources and policies with a single API call.

**Create, update, delete projects**

Create, update, and delete projects that belong to your organization. You can also undelete projects in the “pending deletion” state.

**Project details**

Pull a list of all projects in the organization.

**Cloud folders**

Use Cloud folders to organize resources under your organization and configure IAM policies at the folder level so policies apply transitively to the resources contained within the folder.

**Cloud console and API access**

Access Resource Manager in the GCP Console in the Admin section, via Resource Manager API, or through the command line using gcloud.

### Usage

### Questions

#### How do I use Resource Manager programmatically?

You can use one of the following to interact with resource manager:

* REST API
* gcloud CLI
* Language specific client libraries

Example creating a project using the Python library:

```py
crm = discovery.build(
    'cloudresourcemanager', 'v1', http=creds.authorize(httplib2.Http()))

operation = crm.projects().create(
body={
    'project_id': flags.projectId,
    'name': 'my project'
}).execute()
```

## Data Loss Prevention API

### Summary

Automatically discover and redact sensitive data everywhere.

Cloud DLP helps you better understand and manage sensitive data. It provides fast, scalable classification and redaction for sensitive data elements like credit card numbers, names, social security numbers, US and selected international identifier numbers, phone numbers, and GCP credentials. Cloud DLP classifies this data using more than 90 predefined detectors to identify patterns, formats, and checksums, and even understands contextual clues. You can optionally redact data as well, using techniques like masking, secure hashing, tokenization, bucketing, and format-preserving encryption.

One of the first steps to properly managing your sensitive data is knowing where it exists. Cloud DLP gives you the power to scan, discover, classify, and report on data from virtually anywhere. Cloud DLP has native support for scanning and classifying sensitive data in Cloud Storage, BigQuery, and Cloud Datastore and a streaming content API to enable support for additional data sources, custom workloads and applications.

Today your data is your most critical asset. Cloud DLP provides tools to classify, mask, tokenize, and transform sensitive elements to help you better manage the data that you collect, store, or use for business or analytics. For example, features like format-preserving encryption or tokenization allow you to preserve the utility of your data for joining or analytics while obfuscating the raw sensitive identifiers.

Cloud DLP architecture includes several features to make it easy to use in small or large operations. Templates for inspection and de-identification allow you to define configurations once and use them across requests. DLP job triggers and actions allow you to kick off inspection jobs periodically and generate Cloud Pub/Sub notifications when jobs are complete. See this tutorial on using DLP with Cloud Functions to automatically classify data in Cloud Storage.

Quasi-identifiers are partially identifying or elements or combinations of data that may link to a single person or a very small group. Cloud DLP allows you to measure statistical properties such as k-anonymity and l-diversity, expanding your ability to understand and protect data privacy.

### Features

**Flexible classification**

90+ pre-defined detectors with a focus on quality, speed, scale. Detectors are improving and expanding all the time. A full list of detectors is available in the documentation.

**Pay-as-you-go pricing**

Cloud DLP is charged based on the amount of data processed, not based on a subscription service or device. This customer-friendly pricing allows you to pay as you go and not in advance of demand.

**Secure data handling**

Cloud DLP handles your data securely and undergoes several independent third-party audits to test for data safety, privacy, and security. Read more on our compliance page.

**No hardware or deployments to manage**

Cloud DLP is ready to go, no need to manage hardware, VMs, or scale. Just send a little or a lot of data and Cloud DLP scales for you.

**Custom detectors**

Extend the power of Cloud DLP with custom-defined detection, including custom dictionaries that can scale to millions of entries, pattern recognition, exclusion rules, and context rules.

**Detailed findings**

Classification results can be sent directly into BigQuery for detailed analysis or export into other systems. Custom reports can easily be generated in Cloud Data Studio.

**Easy workload integration**

Efficiently deploy DLP with reusable templates, monitor your data with periodic scans, and integrate into serverless architecture with Cloud Pub/Sub notifications.

**Simple and powerful redaction**

De-identify your data: redact, mask, tokenize, and transform text and images to help ensure data privacy.

**Likelihood scores**

Customize the sensitive data detection threshold to fit your needs and reduce noise.

**REST API**

The DLP API is an HTTP REST API that can be used on data inside or outside of GCP and from mobile devices, IoT devices, and browsers.

### Usage

### Questions

#### What are use cases for the Data Loss Prevention API?

* Adhering to information/data regulations
* Analyzing the risk of customer/user information you store
* Securing your data by de-identification/anonymization via masking, hashing etc
* Determine the diversity of your data

## GSuite

### Questions

#### How do you write an app that has permissions on GSuite products?

For GSuite and Google products you will need to enable API access for the specific product.

*Enable the Drive API*

To interact with the Drive API, you need to enable the Drive API service for your app. You can do this in the Google API project for the app.

To enable the Drive API, complete these steps:

* Go to the Google API Console.
* Select a project.
* In the sidebar on the left, expand APIs & auth and select APIs.
* In the displayed list of available APIs, click the Drive API link and click Enable API.

## gsutil

### Questions

#### What are all the different commands that can be used with gsutil?

gsutil is a Python application that lets you access Cloud Storage from the command line. You can use gsutil to do a wide range of bucket and object management tasks, including:

* Creating and deleting buckets.
* Uploading, downloading, and deleting objects.
* Listing buckets and objects.
* Moving, copying, and renaming objects.
* Editing object and bucket ACLs.

Syntax for accessing resources:
gsutil uses the prefix `gs://` to indicate a resource in Cloud Storage:

`gs://[BUCKET_NAME]/[OBJECT_NAME]`

In addition to specifying exact resources, gsutil supports the use of wildcards in your commands.

gsutil contains thorough built-in help about every command as well as a number of topics, which you can get by running:

`gsutil help`

This command outputs a list of all commands and available help topics, and you can then get detailed help for each command or topic. For example, you can get help about the gsutil cp command by running:

`gsutil help cp`

To get information about gsutil top-level command-line options, use:

`gsutil help options`

List of commands available in *gsutil*:

* acl
* bucketpolicyonly
* cat
* compose
* config
* cors
* cp
* defacl
* defstorageclass
* du
* hash
* help
* hmac
* iam
* kms
* label
* lifecycle
* logging
* ls
* mb
* mv
* notification
* perfdiag
* rb
* requesterpays
* retention
* rewrite
* rm
* rsync
* setmeta
* signurl
* stat
* test
* update
* version
* versioning
* web

## Cloud Armor

### Summary

Protect your services against denial of service and web attacks.

Google Cloud Armor delivers defense at scale against infrastructure and application Distributed Denial of Service (DDoS) attacks using Google’s global infrastructure and security systems.

Google Cloud Armor works with Global HTTP(S) Load Balancer to provide built-in defenses against infrastructure DDoS attacks. Google Cloud Armor benefits from more than a decade of experience protecting the world’s largest Internet properties like Google Search, Gmail and YouTube.

Permit or block your incoming traffic based on IP addresses or ranges using allow lists and deny lists.

Google Cloud Armor’s flexible rules language enables you to customize your defenses and mitigate multivector attacks. It also provides predefined rules to defend against cross-site scripting (XSS) and SQL injection (SQLi) application-aware attacks. Alpha features are only available to selected customers for a limited availability test but will be more generally available soon.

Google Cloud Armor works with security offerings from security partners, enabling you to build a comprehensive security model for your GCP services.

### Features

**Google Cloud Armor with Global HTTP(S) Load Balancer**

Google Cloud Armor works with the HTTP(S) Load Balancer, which provides built-in infrastructure DDoS defense.

**Rich Rules Language ALPHA**

Create rules using any combination of L3–L7 parameters and geolocation to protect your deployment with a flexible rules language. Also use predefined rules to defend against cross-site scripting (XSS) and SQL injection defense.

**Policy Framework with Rules**

Configure one or more security policies with a hierarchy of rules. Apply a policy to one or more services.

**Stackdriver Logging**

Get visibility into the policy and rule matched and the action taken by the rule for each incoming request.

**Preview Mode**

Enable Preview mode to understand service access patterns before enabling your policies and to ensure the correct traffic sources are being allowed and blocked.

**IP-based Access Control**

Enforce access control based on IPv4 and IPv6 addresses or CIDRs.

**Geo-based Access Control ALPHA**

Identify and enforce access control based on geographic location of incoming traffic.

### Questions

#### What are the use cases for Cloud Armor and what protection does it provide?

***Use case 1: Limiting access to the GCP HTTP(S) load balancer***

A typical use case for placing user IP addresses on an allow list is when your external load balancer is used only by a specific set of users. In the following example, only users from your organization are allowed access to services behind your load balancer. These users have IP addresses or address blocks assigned by your organization. You can place these IP addresses or CIDR ranges on an allow list so that only these users have access to the load balancer.

***Use case 2: Block unauthorized or malicious traffic at the edge with deny lists***

Use deny lists to create Google Cloud Armor security policies that reject traffic from an IP address or CIDR range. In the following illustration, the Google Cloud Armor security policy has a deny rule that blocks traffic from the IP address 198.51.100.1, where a malicious user has been identified.

***Use case 3: Allow traffic to the HTTPS load balancer only from an allow listed third-party security provider and other authorized users***

If your organization uses a third-party security provider to scrub traffic, you can allow list the security provider's IP address to ensure that only scrubbed traffic can access the load balancer and backends.

***Limits***

* Each project is limited to a maximum of 200 (two hundred) security rules across all Google Cloud Armor security policies.
* Each project is limited to a maximum of 10 (ten) Google Cloud Armor security policies.
* Each rule is limited to a maximum of 5 (five) IP addresses or IP address ranges.
* There is a limit of 20,000 requests per second per project across all backends with a Google Cloud Armor security policy. Google Cloud Armor limits the volume of traffic that can be processed by all security policies on a per-project basis. Once the inbound request traffic volume (RPS) across all backends protected by a Google Cloud Armor security policy exceeds the limit, then inbound traffic covered by security policies will be throttled to be within the limit.

***Protection against DDoS attacks***

Use Google Cloud Armor security policies to protect your load-balanced services. Google Cloud Armor security policies are made up of rules that allow or prohibit traffic from IP addresses or ranges defined in the rule.

Google Cloud Armor security policies and IP deny lists and allow lists are available only for HTTP(S) Load Balancing

## Cloud Security Scanner

Automatically scan your App Engine, Compute Engine, and Google Kubernetes Engine apps for common vulnerabilities.

### Summary

Cloud Security Scanner is a web security scanner for common vulnerabilities in App Engine, Compute Engine, and Google Kubernetes Engine applications. It can automatically scan and detect four common vulnerabilities, including cross-site-scripting (XSS), Flash injection, mixed content (HTTP in HTTPS), and outdated/insecure libraries. It enables early identification and delivers very low false-positive rates. You can easily set up, run, schedule, and manage security scans, and it is available at no additional charge for Google Cloud Platform users.

Detect key vulnerabilities in development prior to production. After you set up a scan, Cloud Security Scanner automatically crawls your application, following all links within the scope of your starting URLs, and attempts to exercise as many user inputs and event handlers as possible.

The findings for XSS, Flash injection, mixed content usage, and outdated/insecure libraries all have very low false-positive rates. Results are highlighted to enable you to explore and verify in detail and focus on fixes.

You can easily set up and run on-demand immediate or scheduled security scans from the Google Cloud Platform console. Scans should be run from a test environment and test accounts, and are enabled for targets only within your App Engine project to prevent unintended effects.

### Features

**Vulnerability detection**

XSS, Flash injection, mixed content, and use of outdated/insecure JavaScript libraries.

**Simple control**

Set up and run either immediate or scheduled scans from your Google Cloud Platform console. Select your start point and specify excluded paths.

**Actionable results**

Simple and clear scan outputs available from your Google Cloud Platform console.

**Selection of agent browsers**

Scans are run using Chrome, Safari, Blackberry, or Nokia browser agents.

**User authentication**

Supports both Google and non-Google accounts and automatically handles common login scenarios.

### Questions

#### What are the use cases for Cloud Security Scanner and what protection does it provide?

Cloud Security Scanner identifies security vulnerabilities in your App Engine and Compute Engine web applications. It crawls your application, following all links within the scope of your starting URLs, and attempts to exercise as many user inputs and event handlers as possible. The scanner currently detects the following:

* XSS
* Flash injection
* Mixed-content
* Clear text passwords
* Usage of insecure JavaScript libraries
* Cloud Security Scanner currently supports the App Engine standard environment and App Engine flexible environments, Compute Engine instances, and Google Kubernetes Engine resources.

The Cloud Security Scanner is designed to complement your existing secure design and development processes. To avoid distracting you with false positives, the Cloud Security Scanner errs on the side of under reporting and will not display low confidence alerts. It does not replace a manual security review, and it does not guarantee that your application is free from security flaws.

Some important things to be aware of when using Cloud Security Scanner:

* Because the Cloud Security Scanner is undergoing continual improvements, a future scan may report issues that are not reported by the current scan.
* Some features or sections of your application might not be tested.
* The Cloud Security Scanner attempts to activate every control and input it finds.
* If you expose state-changing actions for which your test account has permission, the Cloud Security Scanner is likely to activate them. This may lead to undesirable results.

## Cloud Storage

### Summary

Unified object storage for developers and enterprises

Geo-redundant storage with the highest level of availability and performance is ideal for low-latency, high-QPS content serving to users distributed across geographic regions. Google Cloud Storage provides the availability and throughput needed to stream audio or video directly to apps or websites.

**Common use cases**:

* Streaming videos and music
* Serving images and website content
* Mobile app development

### Features

**A single API for all storage classes**

Cloud Storage’s consistent API, latency, and speed across storage classes simplifies development integration and reduces code complexity. Implement Object Lifecycle Management to set a Time to Live (TTL) for objects, archive older version of objects, or downgrade storage classes without compromising on latency or accessibility. Set custom policies to transition data seamlessly from one storage class to the next, depending on your cost and availability needs at the time

**Designed for eleven 9’s of durability**

Cloud Storage is designed for 99.999999999% durability. It stores data redundantly, with automatic checksums to ensure data integrity. With Multi-Regional Storage, your data is maintained in geographically distinct locations.

**Highly scalable and performant**

Cloud Storage offers unlimited object storage and individual objects can be as large as 5TB. Objects can be overwritten no more than once per second and there is no limit to read frequency. Objects larger than 5MB should be uploaded with multipart or resumable uploading. For more details, review Cloud Storage Quotas & Limits.

**Strongly consistent**

When a write succeeds, the latest copy of the object is guaranteed to be returned to any GET, globally. This applies to PUTs of new or overwritten objects and DELETEs.

**Zero carbon emissions**

By moving storage from a self-managed data center or colocation facility to GCP, the emissions directly associated with your company’s data storage will be zero.

### Usage

### Questions

#### What is standard storage and what are the use cases?

Standard Storage is best for data that is frequently accessed ("hot" data) and/or stored for only brief periods of time.

When used in a region, Standard Storage is appropriate for storing data in the same location as Google Kubernetes Engine clusters or Compute Engine instances that use the data. Co-locating your resources maximizes the performance for data-intensive computations and can reduce network charges.

When used in a dual-region, you still get optimized performance when accessing Google Cloud Platform products that are located in one of the associated regions, but you also get the improved availability that comes from storing data in geographically separate locations.

When used in a multi-region, Standard Storage is appropriate for storing data that is accessed around the world, such as serving website content, streaming videos, executing interactive workloads, or serving data supporting mobile and gaming applications.

#### What is nearline storage and what are the use cases?

Nearline Storage is a low-cost, highly durable storage service for storing infrequently accessed data. Nearline Storage is a better choice than Standard Storage in scenarios where slightly lower availability, a 30-day minimum storage duration, and costs for data access are acceptable trade-offs for lowered at-rest storage costs.

Nearline Storage is ideal for data you plan to read or modify on average once per month or less. For example, if you want to continuously add files to Cloud Storage and plan to access those files once a month for analysis, Nearline Storage is a great choice.

Nearline Storage is also appropriate for data backup, long-tail multimedia content, and data archiving. Note, however, that for data accessed less frequently than once a year, Coldline Storage is the most cost-effective choice, as it offers the lowest storage costs.

#### What is coldline storage and what are the use cases?

Coldline Storage is a very-low-cost, highly durable storage service for data archiving, online backup, and disaster recovery. Unlike other "cold" storage services, your data is available within milliseconds, not hours or days.

Coldline Storage is the best choice for data that you plan to access at most once a year, due to its slightly lower availability, 90-day minimum storage duration, costs for data access, and higher per-operation costs. For example:

Cold Data Storage - Infrequently accessed data, such as data stored for legal or regulatory reasons, can be stored at low cost as Coldline Storage and be available when you need it.

Disaster recovery - In the event of a disaster recovery event, recovery time is key. Cloud Storage provides low latency access to data stored as Coldline Storage.

#### What are signed urls and what are the use cases?

A signed URL is a URL that provides limited permission and time to make a request. Signed URLs contain authentication information in their query string, allowing users without credentials to perform specific actions on a resource. When you generate a signed URL, you specify a user or service account which must have sufficient permission to make the request that the signed URL will make. After you generate a signed URL, anyone who possesses it can use the signed URL to perform specified actions, such as reading an object, within a specified period of time.

In some scenarios, you might not want to require your users to have a Google account in order to access Cloud Storage, but you still want to control access using your application-specific logic. The typical way to address this use case is to provide a signed URL to a user, which gives the user read, write, or delete access to that resource for a limited time. Anyone who knows the URL can access the resource until the URL expires. You specify the expiration time when you create the signed URL.

When using signed URLs with resumable uploads to upload objects to your bucket, you only need to use the signed URL in the initial POST request. No data is uploaded in the POST request; instead, the request returns a session URI which is used in subsequent PUT requests to upload data. Since the session URI is, in effect, an authentication token, the PUT requests do not need to use the original signed URL. This behavior allows the POST request to be made by the server, avoiding the need for clients to have to deal with signed URLs themselves.

#### How do I set policies?

You can add a retention policy to a bucket to specify a retention period.

* If a bucket has a retention policy, objects in the bucket can only be deleted or overwritten once their age is greater than the retention period.

* A retention policy retroactively applies to existing objects in the bucket as well as new objects added to the bucket.

* You can lock a retention policy to permanently set it on the bucket.
  * Once you lock a retention policy, you cannot remove it or reduce the retention period it has.
  * You cannot delete a bucket with a locked retention policy unless every object in the bucket has met the retention period.
  * You can increase the retention period of a locked retention policy.
  * Locking a retention policy can help your data comply with record retention regulations.

* You can place holds on individual objects which prevent them from being deleted or overwritten.

When working with retention policies, keep in mind the following:

* Unless the retention policy is locked, you can increase, decrease, or remove the retention policy from a bucket.

* Changing a retention policy is considered a single Class A operation, regardless of the number of objects affected.

* An object's editable metadata is not subject to the retention policy and can be modified even when the object itself cannot be.

* A retention policy contains an effective time, the time after which all objects in the bucket are guaranteed to be in compliance with the retention period.

* To see the earliest date when a given object is eligible for deletion in a bucket with a retention policy, view the retention expiration date portion of the object's metadata.

* Retention policies and Object Versioning are mutually exclusive features in Cloud Storage: for a given bucket, only one of these can be enabled at a time. Any versioned objects remaining in a bucket when you apply a retention policy are also protected by the retention policy.

* You can use Object Lifecycle Management to automatically delete objects in a bucket, including in a bucket with a locked policy. A lifecycle rule won't delete an object until after the object fulfills the retention policy.

* You use constraints in organization policies to require that retention policies with specific retention periods be included as part of creating a new bucket or as part of adding/updating the a retention policy on an existing bucket. For more information, including instructions for setting this organization policy, see Setting Organization Policies.

#### What are the bucket limitations and quotas?

*Buckets*

* There is a per-project rate limit to bucket creation and deletion of approximately 1 operation every 2 seconds, so plan on fewer buckets and more objects in most cases. For example, a common design choice is to use one bucket per user of your project. However, if you're designing a system that adds many users per second or that creates objects using robot credentials, then design for many users in one bucket (with appropriate permissions) so that the bucket creation rate limit doesn't become a bottleneck.

* Highly available applications should not depend on bucket creation or deletion in the critical path of their application. Bucket names are part of a centralized and global namespace: any dependency on this namespace creates a single point of failure for your application. Due to this and the 1 operation per 2-second limit mentioned above, the recommended practice for highly available services on Cloud Storage is to pre-create all the buckets necessary.

* There is an update limit on each bucket of once per second, so rapid updates to a single bucket (for example, changing the CORS configuration) won’t scale.

* There is a limit of 100 members holding legacy IAM roles per bucket.

*Objects*

* There is a maximum size limit of 5 TB for individual objects stored in Cloud Storage.

* There is an update limit on each object of once per second, so rapid writes to a single object won’t scale. For more information, see Object immutability in Key Terms.

* There is no limit to writes across multiple objects, which include uploading, updating, and deleting objects. Buckets initially support roughly 1000 writes per second and then scale as needed.

* There is no limit to reads of an object. Buckets initially support roughly 5000 object reads per second and then scale as needed.

* Performance is much better for publicly cacheable objects. If you have an object being used to control many clients and thus want to disable caching to provide the latest data:
  * Consider instead setting the object's Cache-Control metadata to public with max-age of 15-60 seconds. Most applications can tolerate a minute of spread, and the cache hit rate will improve performance drastically.
  * Proxy data transfers through a Google App Engine application located in the same location as your bucket.
  * Use Cache-Control: no-cache for an object to indicate that the object must not be cached for subsequent requests in edge-caches.

  For more information about Cache-Control directives, see RFC 7234: Cache-Control.

* There is a limit of 100 access control list entries (ACLs) per object.

* For object composition:
  * Up to 32 objects can be composed in a single composition request.
  * While there is no limit to the number of components that make up a composite object, the componentCount metadata associated with a composite object saturates at 2,147,483,647.
  * Composite objects are subject to the overall 5 TB size limit for objects stored in Cloud Storage.

*XML API requests*

* When sending requests through the XML API, there is a limit on the combined size of the request URL and HTTP headers of 16 KB.

*HMAC keys for service accounts*

* There is a limit of 5 HMAC keys per service account. Deleted keys do not count towards this limit.

#### How can you optimize for heavy load?

In addition, please see [Best Practices for Cloud Storage](https://cloud.google.com/storage/docs/best-practices)

Perform a back-of-the-envelope estimation of the amount of traffic that will be sent to Cloud Storage. Specifically, think about:

Operations per second. How many operations per second do you expect, for both buckets and objects, and for create, update, and delete operations.

Bandwidth. How much data will be sent, over what time frame?

Cache control. Specifying the Cache-Control metadata on objects will benefit read latency on hot or frequently accessed objects. See Viewing and Editing Metadata for instructions for setting object metadata, such as Cache-Control.

Design your application to minimize spikes in traffic. If there are clients of your application doing updates, spread them out throughout the day.

While Cloud Storage has no upper bound on the request rate, for the best performance when scaling to high request rates, follow the Request Rate and Access Distribution Guidelines.

Be aware that there are rate limits for certain operations and design your application accordingly.

If you get an error, use exponential backoff to avoid problems due to large traffic bursts.

Understand the performance level customers will expect from your application. This information will help you choose a storage option and region when creating new buckets.

Cloud Storage is a multi-tenant service, meaning that users share the same set of underlying resources. In order to make the best use of these shared resources, buckets have an initial IO capacity of around 1000 object write requests per second (including uploading, updating, and deleting objects) and 5000 object read requests per second. These initial read and write rates average to 2.5PB written and 13PB read in a month for 1MB objects. As the request rate for a given bucket grows, Cloud Storage automatically increases the IO capacity for that bucket by distributing the request load across multiple servers.

As a bucket approaches its IO capacity limit, Cloud Storage typically takes on the order of minutes to detect and accordingly redistribute the load across more servers. Consequently, if the request rate on your bucket increases faster than Cloud Storage can perform this redistribution, you may run into temporary limits, specifically higher latency and error rates. Ramping up the request rate gradually for your buckets, as described below, avoids such latency and errors.

Cloud Storage supports consistent object listing, which enables users to run data processing workflows easily against Cloud Storage. In order to provide consistent object listing, Cloud Storage maintains an index of object keys for each bucket. This index is stored in lexicographical order and is updated whenever objects are written to or deleted from a bucket. Adding and deleting objects whose keys all exist in a small range of the index naturally increases the chances of contention.

Cloud Storage detects such contention and automatically redistributes the load on the affected index range across multiple servers. Similar to scaling a bucket's IO capacity, when accessing a new range of the index, such as when writing objects under a new prefix, you should ramp up the request rate gradually, as described below. Not doing so may result in temporarily higher latency and error rates.

*Best practices*

Ramp up request rate gradually:

To ensure that Cloud Storage auto-scaling always provides the best performance, you should ramp up your request rate gradually for any bucket that hasn’t had a high request rate in several weeks or that has a new range of object keys. If your request rate is less than 1000 write requests per second or 5000 read requests per second, then no ramp-up is needed. If your request rate is expected to go over these thresholds, you should start with a request rate below or near the thresholds and then double the request rate no faster than every 20 minutes.

Note: We recommend that you run performance and scalability tests to ensure that this guideline works for your specific use case, prior to ramping up your traffic in production.
If you run into any issues such as increased latency or error rates, pause your ramp-up or reduce the request rate temporarily in order to give Cloud Storage more time to scale your bucket. You should use exponential backoff to retry your requests when receiving errors with 5xx or 429 response codes from Cloud Storage.

Use a naming convention that distributes load evenly across key ranges:

Auto-scaling of an index range can be slowed when using sequential names, such as object keys based on a sequence of numbers or timestamp. This occurs because requests are constantly shifting to a new index range, making redistributing the load harder and less effective.

In order to maintain a high request rate, avoid using sequential names. Using completely random object names will give you the best load distribution. If you want to use sequential numbers or timestamps as part of your object names, introduce randomness to the object names by adding a hash value before the sequence number or timestamp.

For example, if the original object names you want to use are:

```
my-bucket/2016-05-10-12-00-00/file1
my-bucket/2016-05-10-12-00-00/file2
my-bucket/2016-05-10-12-00-01/file3
```
...
You can compute the MD5 hash of the original object name and add the first 6 characters of the hash as a prefix to the object name. The new object names become:

```
my-bucket/2fa764-2016-05-10-12-00-00/file1
my-bucket/5ca42c-2016-05-10-12-00-00/file2
my-bucket/6e9b84-2016-05-10-12-00-01/file3
```

*Randomness after a common prefix is effective under the prefix*
Note that the random string doesn’t necessarily need to be at the beginning of the object name. Adding a random string after a common prefix still allows auto-scaling to work, but the effect is limited to that prefix, with no consideration of the rest of the bucket.

For example:

my-bucket/images/animals/4ce4c6af-6d27-4fa3-8a91-5701a8552705/1.jpg
my-bucket/images/animals/9a495e72-1d85-4637-a243-cbf3e4a90ae7/2.jpg
...
my-bucket/images/landscape/585356ac-ce89-47a8-bdd2-78a86b58fee6/1.jpg
my-bucket/images/landscape/2550ae5b-395e-4243-a29b-bbf5aece60ef/2.jpg
...
my-bucket/images/clouds/1.jpg
my-bucket/images/clouds/2.jpg
...
The above naming allows for efficient auto-scaling of objects in images/animals and images/landscape, but not images/clouds.

*Randomness after sequential prefixes is not as effective*

As mentioned above, using a random string after a common prefix only helps with auto-scaling under that prefix. Once the requests shift to a new prefix, you may no longer benefit from the previous auto-scaling effects. This is especially a problem when the prefixes follow a sequential pattern.

For example, if you write files under a new timestamp-based prefix every hour:
```
my-bucket/2016-05-10-00/cf9a7b95-0d2e-4466-9596-840ff388ddbd
my-bucket/2016-05-10-00/f1e16a88-16b8-4c66-ba66-a225c87be80c
my-bucket/2016-05-10-00/646d8272-4a88-4dc2-b2d4-d537c778df41
my-bucket/2016-05-10-01/bdcba6de-ac25-4c27-8550-0d08f249e69d
my-bucket/2016-05-10-01/a32c867c-09a9-4d65-9668-ddd4ebe4138b
my-bucket/2016-05-10-01/d619485c-5243-4a4e-8ef3-0f7e1d26ce1d
```

Although auto-scaling helps to increase the write rate under a prefix over time, the write rate resets at the beginning of each hour. This results in a sub-optimal write rate and periodic increases in latency and error rate. If you need to write to different prefixes over time, to avoid this problem, make sure the new prefixes are evenly distributed across the entire key range.

Reorder bulk operations to distribute load evenly across key ranges:
Sometimes you'll want to perform a bulk upload or deletion of data in Cloud Storage. In both cases, you may not have control over the object names. Nevertheless, you can control the order in which the objects are uploaded or deleted to achieve the highest write or deletion rate possible.

To do so, you should distribute the uploads or deletes across multiple prefixes. For example, if you have many folders and many files under each folder to upload, a good strategy is to upload from multiple folders in parallel and randomly choose which folders and files are uploaded. Doing so allows the system to distribute the load more evenly across the entire key range, which allows you to achieve a high request rate after the initial ramp-up.


## Cloud Composer

### Summary

A fully managed workflow orchestration service built on Apache Airflow

Cloud Composer is a fully managed workflow orchestration service that empowers you to author, schedule, and monitor pipelines that span across clouds and on-premises data centers. Built on the popular Apache Airflow open source project and operated using the Python programming language, Cloud Composer is free from lock-in and easy to use.

Cloud Composer pipelines are configured as directed acyclic graphs (DAGs) using Python, making it easy for users of any experience level to author and schedule a workflow. One-click deployment yields instant access to a rich library of connectors and multiple graphical representations of your workflow in action, increasing pipeline reliability by making troubleshooting easy. Automatic synchronization of your directed acyclic graphs ensures your jobs stay on schedule.

Cloud Composer is deeply integrated within the Google Cloud Platform, giving users the ability to orchestrate their full pipeline. Cloud Composer has robust, built-in integration with many products, including Google BigQuery, Cloud Dataflow, Cloud Dataproc, Cloud Datastore, Cloud Storage, Cloud Pub/Sub, and Cloud ML Engine.

Cloud Composer gives you the ability to connect your pipeline through a single orchestration tool whether your workflow lives on-premises, in multiple clouds, or fully within GCP. The ability to author, schedule, and monitor your workflows in a unified manner means you can break down the silos in your environment and focus less on infrastructure.

Cloud Composer is built on Apache Airflow, the popular open source orchestration tool. This open source project, which Google is contributing back into, provides freedom from lock in for customers as well as integration with a broad number of platforms, which will only expand as the Airflow community grows.

### Features

**Multi-cloud**

Create workflows that connect data, processing, and services across clouds, giving you a unified data environment.

**Hybrid**

Ease your transition to the cloud or maintain a hybrid data environment by orchestrating workflows that cross between on-premises and the public cloud.

**Python Programming Language**

Leverage existing Python skills to dynamically author and schedule workflows within Cloud Composer.

**Fully Managed**

Cloud Composer's managed nature allows you to focus on authoring, scheduling, and monitoring your workflows as opposed to provisioning resources.

**Open Source**

Cloud Composer is built upon Apache Airflow, giving users freedom from lock-in and portability.

**Integrated**

Built-in integration with BigQuery, Dataflow, Dataproc, Datastore, Cloud Storage, Pub/Sub, Cloud ML Engine, and more, giving you the ability to orchestrate end-to-end GCP workloads.

**Reliability**

Increase reliability of your workflows through easy-to-use charts for monitoring and troubleshooting the root cause of an issue.

### Questions

#### How does it work?

Cloud Composer deploys Cloud Storage, Google Kubernetes Engine, and Stackdriver in your customer project.

*Cloud Storage*

Cloud Storage provides the storage bucket for staging DAGs, plugins, data dependencies, and logs. To deploy workflows (DAGs), you copy your files to the bucket for your environment. Cloud Composer takes care of synchronizing the DAGs among workers, schedulers, and the web server. With Cloud Storage you can store your workflow artifacts in the data/ and logs/ folders without worrying about size limitations and retain full access control of your data.

*Google Kubernetes Engine*

By default, Cloud Composer deploys core components—such as Airflow scheduler, worker nodes, and CeleryExecutor—in a GKE. For additional scale and security, Cloud Composer also supports VPC-native clusters using alias IPs.

Redis, the message broker for the CeleryExecutor, runs as a StatefulSet application so that messages persist across container restarts.

Running the scheduler and workers on GKE enables you to use the KubernetesPodOperator to run any container workload. By default, Cloud Composer enables auto-upgrade and auto-repair to protect the GKE clusters from security vulnerabilities. If you need to upgrade your Cloud Composer GKE cluster before the auto-upgrade cycle, you can perform a manual upgrade.

Note that the Airflow worker and scheduler nodes and the Airflow web server run on different service accounts.

Scheduler and workers: If you do not specify a service account during environment creation, the environment runs under the default Compute Engine service account.
web server: The service account is auto-generated during environment creation and derived from the web server domain. For example, if the domain is foo-tp.appspot.com, the service account is foo-tp@appspot.gserviceaccount.com.

*Stackdriver*

Cloud Composer integrates with Stackdriver Logging and Stackdriver Monitoring, so you have a central place to view all Airflow service and workflow logs.

Because of the streaming nature of Stackdriver Logging, you can view the logs that the Airflow scheduler and workers emit immediately instead of waiting for Airflow logging module synchronization. And because the Stackdriver logs for Cloud Composer are based on google-fluentd, you have access to all logs the scheduler and worker containers produce. These logs greatly improve debugging and contain useful system-level and Airflow dependency information.

Stackdriver Monitoring collects and ingests metrics, events, and metadata from Cloud Composer to generate insights via dashboards and charts.


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




