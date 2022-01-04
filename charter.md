<!-----
* Docs to Markdown version 1.0β31
* Tue Jan 04 2022 05:45:22 GMT-0800 (PST)
* Source doc: observe-k8s.dev working doc
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!
----->

<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 2.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



# observe-k8s working document

## Mission Statement

For cloud native workloads, observability is a key requirement, yet it’s a broad term and there are many tools and approaches available to achieve it.

While the [whitepaper](https://github.com/cncf/tag-observability/blob/main/whitepaper.md) by the [CNCF TAG Observability](https://github.com/cncf/tag-observability) covers the theoretical foundations of modern observability, practitioners need more guidance on how to achieve it in real life scenarios.

This working group aims to provide:

* a set suite of realistic sample applications, which employ observability tools to demonstrate how practitioners can gain insight and understanding.
* actionable, best-practice guidance on how to apply observability to real-life workloads. Observed workloads will be CNCF Projects.

*A distinct section requiring intentional navigation by the User shall be provided for open source projects which are not CNCF Projects if this opportunity arises.*

---

**Table of Contents**

[TOC]

## Interested Parties

* Matt Young ([halcyondude@gmail.com](mailto:halcyondude@gmail.com))
* Ivan Santos ([pragmaticivan@gmail.com](mailto:pragmaticivan@gmail.com), EverQuote)
* Ken Finnigan ([ken@kenfinnigan.me](mailto:ken@kenfinnigan.me), Workday)
* Michael Hausenblas ([mh9@o11y.engineering](mailto:mh9@o11y.engineering), AWS)  
* Ryan Perry ([rperry2174@gmail.com](mailto:rperry2174@gmail.com), Pyroscope)
* Daniel Khan ([daniel@khan.io](mailto:daniel@khan.io), Elastic)
* Severin Neumann ([severin.neumann@altmuehlnet.de](mailto:severin.neumann@altmuehlnet.de), Cisco)


## Discussion(s) thus far:

* CNCF:  Chris A, Bill M
* Scott Rigby (GitOps WG)
* Bartek
* Alolita
* Friends / fellow Observability geeks :) 
* TAG Observability!
* Crossplane, ACK, Pixie, Linkerd, ...


## Prior discussion takeaways (as of 2021-11-22) 


### CNCF



* Will purchase the domains if we make this real.  has acquired the following domains, the CNCF would assume ownership and make us admin/root.
    * **observe-k8s.io**
    * **observe-k8s.dev**
    * observe-k8s.com
    * observe-k8s.info
    * github.com/observe-k8s.  
* CNCF has an [Infrastructure Lab](https://github.com/cncf/cluster), or we could host on public cloud (perhaps easier than futzing with metal)
* Guidance from Chris Aniszczyk (CNCF CTO): Use the working model that the GitOps WG is taking with “OpenGitOps” - in terms of governance. Spend time here to make it sustainable by a community of maintainers / TAG so it can have legs.  Similar feedback from Scott Rigby.


### GitOps WG



* Demonstrate GitOps good practices.
* PR: GitOps WG Charter to include TAG Observability as a related / interested group
* Open Standard for reporting on execution of GitOps workflows.


## 


## Brainstorm: Vision / Ideas


### Working Group Requirements for Launch


```
    TAGs may choose to spawn focused and time-limited working groups to achieve some of their responsibilities (for example, to produce a specific educational white paper, or portfolio gap analysis report). Working groups should have a clearly documented charter, timeline (typically a few quarters at most), and set of deliverables. Once the timeline has elapsed, or the deliverables delivered, the working group dissolves, or is explicitly re-chartered.
```



    (source: https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#responsibilities--empowerment-of-tags)



1. Charter / Description of WG
    1. {This document once it's done}
2. Time Box 
    2. 2 quarters (winter 21-22)
3. Deliverables
    3. github.com/observe-k8s:  An umbrella organization for repos that realize the goals of this org
    4. Repositories containing demo code and examples on how to run and utilize observability tools
        * Examples of use cases we mentioned from whitepaper
        * Also delivered as an interactive environment for exploration
    5. Catalog of resources for learning about observability


### 


### Interactive Demo environment & playground



* Rather than a scripted tutorial or guide, allow free experimentation.
* Demonstrate _value_ of various solutions by (clonable, reproducible) examples.  In other words “see it first, then easily replicate in your own env”
* Enable multiple views of the same underlying infra/workloads.  As the TAG isn’t meant to be a “kingmaker” - 
* a site leveraging Angular (as a framework in particular) might make this somewhat simpler to achieve.  Caveat: I’m not a front end dev :)
* Prometheus provides a demo service [here](https://prometheus.demo.do.prometheus.io/) - anecdotally it is really helpful in explaining key concepts quickly in slack / other support requests.
    * Thanos is discussing adding one too [here](https://github.com/thanos-io/thanos/issues/4606).


### Design: observe.io



* visualization / details showing the actual request, and the infra that's generating the response. Useful as a doorway to engage with persons that find their way to one of the 2 main front doors (observe-k8s.dev, observe-k8s.io). 

        "Welcome! This is you and here is the web server that rendered the site you're currently observing :)  \
 \
Enter! See what else is running!" \


* For 2d (flat browser) and 3d (AR, MR, VR, 3d rendering in-browser) the site would show other CNCF Projects running, hosted by the CNCF Lab ([https://github.com/cncf/cluster](https://github.com/cncf/cluster))
* Suggest [https://angular.io](angular.io) 
    * extensibility via drop-in Angular Controls
    * modelling connections to back end API’s ([Services](https://angular.io/guide/architecture-services))
    * shared data model enabling n views of same underlying data simply.


### Design: observe.dev



* Targeting developer persona


### 


### CNCF interested parties and collaboration opportunities:


#### SIG Instrumentation



* Source of upstream k8s signals


#### CNCF TAG App Deploy: GitOps WG



* Open Standard for data format for reporting 

 \
TAG Observability.



* How to visualize execution of Operators, Controllers en masse / aggregate. 
* Engage with SIG Instrumentation re: gaps and opportunities for signals from k8s
* Collect and Curate templates, recipes, examples, demos highlighting the observation of cloud native systems and workloads (CNCF Projects).


## 


## Personas

Gibbs Cullen from Chronosphere has been working on Personas, TODO ping to see if we can use these here.


### Practitioner


### Developer


### Data Scientist / Analyst


### Business Function Owner


## Technology Stack (brainstorm)

_Proposed: Brainstorming - this is not authoritative!_


### Architecture

TODO: 10k' Diagram


### GitOps for $allTheThings



* Flux v2 - base / common cluster services, workloads as desired
* ArgoCD - workloads
* …?


### Platform Composition & Abstraction

Use [crossplane.io](https://crossplane.io/) for the base kubernetes platform to abstract:



* public cloud { AWS, Azure, GCP, … } where observe-k8s is running
* Enable local development (kind, k3d, …) and iteration 
* CI, running github actions (kind)


### Ingress: NGINX 



* It's portable, runs equally well locally (on a laptop in a kind cluster) or in public cloud


### Prometheus operator



* Provide cluster-local prometheus, alertmanager, …


### Service Mesh: Linkerd



* CNCF Graduated Project


## 


## workloads: Objects of Observation (wOoO)

[https://landscape.cncf.io/card-mode](https://landscape.cncf.io/card-mode), as of 2021-11-22.


### CNCF Projects: Graduated (16) and Incubating (25)



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")



### 


### CNCF Projects: Sandbox (66)



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")





### Potential example workloads


### "Sock Shop"



* [https://github.com/logzio/microservices-demo](https://github.com/logzio/microservices-demo) 
    * This is packaged up nicely, and uses OTel.  Original GCP variant doesn't have OTel
* [https://github.com/GoogleCloudPlatform/microservices-demo](https://github.com/GoogleCloudPlatform/microservices-demo)


### .net core example (from Microsoft)



* https://github.com/dotnet-architecture/eShopOnContainers


### Linkerd Emojivote



* [https://github.com/BuoyantIO/emojivoto](https://github.com/BuoyantIO/emojivoto)


### podtato-head



* [https://github.com/podtato-head/podtato-head](https://github.com/podtato-head/podtato-head)
* This has a fairly active community


### APM Game



* [https://github.com/Appdynamics/apm-game](https://github.com/Appdynamics/apm-game) 
    * A “sample app generator”: instead of having a fixed application like a Shop or Chat App or Blog, you write down a yaml file of services with endpoints and behaviour (language to use, other services to call, probability of errors, slow downs, etc.etc.) you want to have, and then the tool spins up a bunch of docker containers emulating those services, e.g. a simple "upload service":
    * Not yet documented you can use OTel auto instrumentation instead of the vendor specific agents. I am happy to turn this into a “o11y-game” with OTel out of the box.

## Appendices & Resources

### Mandate (from TAG Charter)

_Note: items in bold are considered particularly relevant for this workstream_

#### Mission

Consistent with the CNCF [TAG](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md) definition, the mission of TAG Observability is to:

* **Foster and grow the ecosystem of observability related projects, users, and maintainers.**
* **Identify and report gaps in the CNCF's project portfolio on topics of observability to the TOC and the wider CNCF community.**
* **Collect, curate, champion, and disseminate patterns and current best practices related to the observation of cloud-native systems that are effective and actionable.**
* **Educate and inform users with unbiased, accurate, and pertinent information.**
* **Educate and help other CNCF projects regarding observability techniques and practices available within the CNCF.**
* Provide and maintain a vendor-neutral venue for relevant thought validation, discussion, and project feedback.
* Provide a ladder for community members to become involved with the technical oversight of projects within the TAG's scope in an open, transparent, and inclusive way.

#### Areas considered in Scope

Observability focuses on patterns, projects, tools, and techniques related to topics such as:

* **Methodologies for instrumenting, collecting, processing, storing, querying, curating, and correlating observational data such as metrics, logging/events, trace spans, and profiling of cloud native workloads.**
* Using distributed trace tooling to observe a series of calls between microservices to understand where time is being spent.
* **Managing the complexity, operational cost, and resource consumption of observability tools and systems at the enterprise scale.**
* Best practices for meaningful alerting, queries, and operational dashboards including how to manage things including rules, definitions, thresholds and policies.
* **How developers, operators, Site Reliability Engineers (SRE), IT Engineers, and other actors comprehend, process, and reason on distributed cloud-native systems.**
* Projects that incorporate novel & insightful approaches to utilizing observability data such as:
    * ML, model training, Bayesian networks, and other data science techniques that enable anomaly & intrusion detection.
    * Correlating resource consumption with costing data to reduce the total cost of cloud native infrastructure
    * Using observability data exposed by service meshes, orchestrators, and other metric sources to inform continuous deployment tooling (e.g. Canary Predicates/Judges).
* **Objective curation and generation of case studies pertaining to delivering observability tools/systems to end users.**
* Best practices around observability and its continuous improvement, e.g. post mortems, runbooks
* Provide guidance around and foster interoperability between observability solutions without trying to enforce one specific standard.
* Foster understanding of the prerequisites and corner-stones of observability like SLI/KPI, service objectives, and internal/external commitments.

The following is a non-exhaustive sample list of activities and deliverables that are in-scope for this TAG

* **Summary and overview of projects available in the community.**
* **Catalog of reference architectures that draw from CNCF projects, combining them in useful and novel ways.**
* Definitions of implementations and patterns for best practices for delivering observability tooling at enterprise scale.
* Tooling composition and toolchain creation based on existing projects.
* Best practices for operations and monitoring workflows using CNCF Projects.
* Organizing and helping to provide visibility to Meetups, Blogs, and Podcasts related to the scope of the TAG.
* **Guidance for application development and architecture that is observable.**
* **Replicable reference architectures.**
* **Patterns for observing application delivery pipelines.**
* Education regarding instrumentation cloud native workloads.
* Processing and Accessing relevant observability data at scale.
* Policy and security controls for observability data.
* Creating artifacts as part of CI/CD pipelines that facilitate observation of services. Concrete examples might be:
    * Service profiles for Linkerd.
    * Debug binaries or other diagnostic metadata.
    * representative trace spans from failing CI tests.


## Meeting Notes

### 2021-12-16

* Attendees (Michael H., Ken F., Matt Y., Daniel K.)

#### Actions

* Action (Daniel) work on mission statement

### 2021-12-09

* Attendees (Michael H., Ken F., Matt Y.)

#### Actions


* Action (Matt) send out doodle for recurring times, 
* Action (Matt) communication re: co-chairs
    * 2 volunteers thus far: Michael Hausenblas and Ken Finnigan
* Action (Matt) create GitHub bits (project board)
    * github.com