# Awesome-Security-Information-n-Event-Management

## Top Security Information & Event Management (SIEM) Platforms



**A comprehensive ecosystem of SIEM, security analytics, log management, threat detection and open-source security monitoring platforms**



*Open-source-first reference covering security information and event management, centralized log collection, detection engineering, correlation, threat hunting, UEBA, threat intelligence, incident investigation, compliance and security analytics.*



**Last updated: September 2026**



Security Information & Event Management (**SIEM**) platforms collect, normalize, correlate, search and analyze security telemetry from across an organization's infrastructure.



A modern SIEM typically processes:



```text

Endpoints

   ↓

Servers

   ↓

Network Devices

   ↓

Cloud

   ↓

Identity

   ↓

Applications

   ↓

Security Tools

   ↓

SIEM

   ↓

Detection

   ↓

Investigation

   ↓

Response

```



Examples include **Splunk Enterprise Security, Microsoft Sentinel, Google Security Operations, Elastic Security, Exabeam, Sumo Logic Cloud SIEM, LogRhythm, Devo, IBM QRadar and Chronicle SIEM**.



The modern SIEM ecosystem increasingly combines:



* centralized log management

* security analytics

* detection engineering

* correlation

* threat intelligence

* behavioral analytics

* UEBA

* threat hunting

* incident management

* SOAR integration

* compliance reporting

* cloud security telemetry

* endpoint telemetry

* network telemetry

* machine learning

* AI-assisted investigation



This README focuses particularly on **open-source alternatives and composable building blocks**, including Wazuh, OpenSearch, Security Onion, Elastic Stack, OSSEC, Graylog, AlienVault OSSIM, SIEMonster and many complementary security projects.



## Open-source emphasis



Open-source projects are divided into:



1. **Direct SIEM platforms** — systems that can independently provide security monitoring, event analysis and detection.

2. **Open-source log analytics platforms** — powerful search and observability systems that can form the data layer of a SIEM.

3. **Network-security platforms** — systems such as Suricata and Zeek that provide high-value security telemetry.

4. **Endpoint-security platforms** — systems such as Wazuh, OSSEC and Velociraptor.

5. **Detection-engineering projects** — Sigma, YARA and related rule frameworks.

6. **Threat-intelligence platforms** — MISP, OpenCTI and related projects.

7. **SOC-in-a-box distributions** — Security Onion and similar integrated platforms.

8. **Open-source SIEM building blocks** — Kafka, Fluent Bit, OpenTelemetry, Grafana, OpenSearch and other infrastructure.



> **Important:** A log-management platform is not automatically a complete SIEM. A serious SIEM requires not only ingestion and search, but also detection rules, correlation, alerting, investigation, threat intelligence, retention, access control and operational workflows.



Wazuh, for example, describes itself as a free and open-source platform unifying XDR and SIEM capabilities, while Security Onion combines network visibility, host visibility, intrusion detection, log management and case management.



Contributions and corrections are welcome.



---



## Table of Contents



* [SaaS/Hosted Platforms](#saashosted-platforms)

* [Open-Source SIEM Platforms](#open-source-siem-platforms)

* [Open-Source Log Analytics & Security Analytics](#open-source-log-analytics--security-analytics)

* [Open-Source SOC-in-a-Box Platforms](#open-source-soc-in-a-box-platforms)

* [Open-Source Endpoint Security & HIDS](#open-source-endpoint-security--hids)

* [Open-Source Network Security Telemetry](#open-source-network-security-telemetry)

* [Open-Source Threat Intelligence](#open-source-threat-intelligence)

* [Open-Source Detection Engineering](#open-source-detection-engineering)

* [Open-Source Security Data Pipelines](#open-source-security-data-pipelines)

* [Additional Strong Open-Source Options](#additional-strong-open-source-options)

* [Commercial Platform → Open-Source Equivalents](#commercial-platform--open-source-equivalents)

* [Frameworks for Building Custom SIEM Platforms](#frameworks-for-building-custom-siem-platforms)

* [Reference Architecture](#reference-architecture)

* [Typical SIEM Workflow](#typical-siem-workflow)

* [Log Collection Workflow](#log-collection-workflow)

* [Detection Engineering Workflow](#detection-engineering-workflow)

* [Threat Hunting Workflow](#threat-hunting-workflow)

* [Incident Investigation Workflow](#incident-investigation-workflow)

* [Cloud SIEM Workflow](#cloud-siem-workflow)

* [Capability Matrix](#capability-matrix)

* [Recommended Open-Source Stacks](#recommended-open-source-stacks)

* [What Is Still Difficult to Reproduce in Open Source?](#what-is-still-difficult-to-reproduce-in-open-source)

* [Why Open Source Is Interesting](#why-open-source-is-interesting)

* [How to Contribute](#how-to-contribute)

* [Disclaimer](#disclaimer)



---



# SaaS/Hosted Platforms



These are commercial, hosted or enterprise-oriented SIEM and security analytics platforms.



| Platform                                                                                     | Primary Model          | Main Strength                                      |

| -------------------------------------------------------------------------------------------- | ---------------------- | -------------------------------------------------- |

| [Splunk Enterprise Security](https://www.splunk.com/en_us/products/enterprise-security.html) | Enterprise SIEM        | Broad security analytics ecosystem                 |

| [Microsoft Sentinel](https://azure.microsoft.com/products/microsoft-sentinel)                | Cloud SIEM             | Azure/Microsoft ecosystem + cloud-native analytics |

| [Google Security Operations](https://cloud.google.com/security/products/security-operations) | Cloud SIEM             | Chronicle-scale telemetry + threat intelligence    |

| [Elastic Security](https://www.elastic.co/security)                                          | Search/SIEM            | Elastic analytics + security detection             |

| [Exabeam](https://www.exabeam.com/)                                                          | SIEM/UEBA              | Behavioral analytics and investigation             |

| [Sumo Logic Cloud SIEM](https://www.sumologic.com/solutions/cloud-siem)                      | Cloud SIEM             | Cloud-native security analytics                    |

| [LogRhythm](https://logrhythm.com/)                                                          | Enterprise SIEM        | Security monitoring and analytics                  |

| [Devo](https://www.devo.com/)                                                                | Cloud SIEM             | Real-time security analytics                       |

| [IBM QRadar](https://www.ibm.com/products/qradar-siem)                                       | Enterprise SIEM        | Mature correlation and enterprise security         |

| [Chronicle SIEM](https://cloud.google.com/security/products/security-operations)             | Cloud SIEM             | High-scale security telemetry                      |

| [Rapid7 InsightIDR](https://www.rapid7.com/products/insightidr/)                             | Cloud SIEM/XDR         | Detection + investigation                          |

| [CrowdStrike Falcon Next-Gen SIEM](https://www.crowdstrike.com/platform/next-gen-siem/)      | SIEM/XDR               | Endpoint-centric security analytics                |

| [Securonix](https://www.securonix.com/)                                                      | SIEM/UEBA              | Behavioral analytics                               |

| [Exabeam Fusion](https://www.exabeam.com/)                                                   | SIEM/UEBA              | Threat detection and investigation                 |

| [Trellix Helix](https://www.trellix.com/en-us/products/helix.html)                           | SIEM/SOC               | Security operations analytics                      |

| [FortiSIEM](https://www.fortinet.com/products/siem/fortisiem)                                | SIEM                   | Fortinet ecosystem                                 |

| [AlienVault USM Anywhere](https://cybersecurity.opentext.com/products/usm-anywhere)          | Cloud SIEM             | Unified security monitoring                        |

| [OpenText ArcSight](https://www.opentext.com/products/arcsight)                              | Enterprise SIEM        | Enterprise security analytics                      |

| [RSA NetWitness](https://www.netwitness.com/)                                                | SIEM/Network Analytics | Network-centric detection                          |

| [Graylog Security](https://graylog.org/products/security/)                                   | SIEM                   | Log analytics + security detection                 |



---



# Open-Source SIEM Platforms



These are the most important projects to investigate when building a SIEM without depending entirely on proprietary software.



---



# 1. Wazuh



[GitHub](https://github.com/wazuh/wazuh)



Wazuh is one of the strongest open-source SIEM/XDR platforms.



Its architecture consists of:



```text

Wazuh Agent

     ↓

Wazuh Server

     ↓

Wazuh Indexer

     ↓

Wazuh Dashboard

```



Wazuh describes the platform as free and open source, with components covering endpoint and cloud security, SIEM/XDR, file-integrity monitoring, vulnerability detection and compliance.



Capabilities include:



* log analysis

* endpoint monitoring

* file-integrity monitoring

* vulnerability detection

* security configuration assessment

* malware detection

* compliance monitoring

* cloud security

* container security

* threat detection

* incident response

* security dashboards



It is one of the closest open-source alternatives to a traditional integrated SIEM/XDR platform.



---



# 2. OpenSearch + Security Analytics



[GitHub](https://github.com/opensearch-project/OpenSearch)



OpenSearch provides a powerful open-source search and analytics foundation.



Its security ecosystem can provide:



* log analytics

* security analytics

* alerting

* detection rules

* dashboards

* anomaly detection

* audit logging

* access control



OpenSearch is Apache 2.0 licensed and is a community-driven fork of Elasticsearch.



OpenSearch Security also provides encryption, authentication, access control and audit logging.



A possible SIEM stack:



```text

Fluent Bit

    ↓

OpenSearch

    ↓

Security Analytics

    ↓

Detection

    ↓

Alerting

    ↓

OpenSearch Dashboards

```



---



# 3. Security Onion



[Website](https://securityonionsolutions.com/)



[GitHub](https://github.com/Security-Onion-Solutions/securityonion)



Security Onion is an integrated open security platform designed for defenders.



It combines:



* network visibility

* host visibility

* intrusion detection

* packet capture

* log management

* threat hunting

* alert management

* case management



Its current documentation describes a platform incorporating Suricata, Zeek/Suricata metadata, packet capture, Elastic Agent, osquery and Elasticsearch-based security interfaces.



Typical architecture:



```text

Network Traffic

      ↓

Suricata / Zeek

      ↓

Security Onion

      ↓

Elasticsearch

      ↓

Detection

      ↓

Hunt / Alert / Case

```



Security Onion is particularly strong for network-centric SOC operations.



---



# 4. Elastic Stack / Elastic Security



[GitHub](https://github.com/elastic/elastic-stack)



[Elastic Security](https://www.elastic.co/security)



Elastic provides:



```text

Elasticsearch

+

Kibana

+

Elastic Agent

+

Security

```



It is one of the most powerful open/self-managed foundations for security analytics.



Capabilities include:



* log ingestion

* search

* detection rules

* threat hunting

* endpoint telemetry

* network telemetry

* SIEM dashboards

* security analytics

* machine learning

* observability



> **Licensing note:** Elastic's licensing is more nuanced than the simple phrase "open source." Elasticsearch/Kibana have multiple licensing options, including AGPLv3 for portions/editions, while some capabilities remain under Elastic's commercial licensing. Verify the specific version and component before redistribution.



---



# 5. OSSEC



[GitHub](https://github.com/ossec/ossec-hids)



OSSEC is one of the foundational open-source host-based intrusion detection systems.



Capabilities include:



* log analysis

* file-integrity monitoring

* rootkit detection

* compliance monitoring

* active response

* host intrusion detection



OSSEC is especially useful as a lightweight HIDS layer.



```text

Endpoint

   ↓

OSSEC Agent

   ↓

OSSEC Manager

   ↓

Alerts

```



Wazuh originated from the OSSEC ecosystem and expanded it significantly.



---



# 6. AlienVault OSSIM



[GitHub](https://github.com/AlienVault-ossim/ossim)



OSSIM is one of the best-known historical open-source SIEM platforms.



It combines security technologies such as:



* event collection

* correlation

* vulnerability assessment

* IDS

* asset discovery

* risk assessment



It remains historically important to the open-source SIEM ecosystem.



---



# Open-Source Log Analytics & Security Analytics



Not every project in this section is a complete SIEM.



However, these platforms can provide the **data, search and analytics layer** needed to construct one.



---



## OpenSearch



[GitHub](https://github.com/opensearch-project/OpenSearch)



Strong for:



* log storage

* full-text search

* analytics

* alerting

* dashboards

* security analytics

* distributed data



---



## OpenSearch Dashboards



[GitHub](https://github.com/opensearch-project/OpenSearch-Dashboards)



Provides visualization and operational interfaces for OpenSearch.



---



## Elasticsearch



[GitHub](https://github.com/elastic/elasticsearch)



A major search and analytics engine widely used in SIEM architectures.



---



## Kibana



[GitHub](https://github.com/elastic/kibana)



Provides visualization, dashboards, investigation interfaces and security analytics interfaces for Elastic environments.



---



## Graylog



[GitHub](https://github.com/Graylog2/graylog2-server)



Graylog is a powerful centralized log-management platform.



It provides:



* ingestion

* parsing

* pipelines

* search

* dashboards

* streams

* alerting in applicable editions

* security analytics in commercial offerings



> **Important:** Graylog's licensing and feature split have changed over time. Verify the current edition and license before treating Graylog Open as a complete open-source SIEM.



---



## Grafana Loki



[GitHub](https://github.com/grafana/loki)



Loki is a log aggregation system optimized for efficient storage and querying.



It can serve as a logging layer but requires additional detection/security components to become a full SIEM.



---



## Grafana



[GitHub](https://github.com/grafana/grafana)



Useful for:



* security dashboards

* alert visualization

* operational dashboards

* threat-hunting views



---



# Open-Source SOC-in-a-Box Platforms



## Security Onion



Security Onion is arguably the strongest open-source choice when the objective is:



> **"Deploy a complete defensive monitoring environment rather than assemble every component manually."**



It integrates network and host visibility, intrusion detection, packet capture, log management and case-management functionality.



---



## Wazuh



Wazuh similarly provides an integrated architecture with:



```text

Agent

+

Server

+

Indexer

+

Dashboard

```



and is explicitly positioned as an open-source unified XDR/SIEM platform.



---



## OSSIEM



[GitHub](https://github.com/dLoProdz/OSSIEM)



OSSIEM is an example of a community-built integrated stack combining components such as:



```text

Wazuh

+

Graylog

+

Grafana

+

OpenSearch

```



It is useful as a laboratory/reference deployment rather than as a drop-in production SIEM.



---



# Open-Source Endpoint Security & HIDS



Endpoint telemetry is essential to a modern SIEM.



## Wazuh



```text

Endpoint

 ↓

Agent

 ↓

Manager

 ↓

Indexer

 ↓

SIEM

```



---



## OSSEC



[GitHub](https://github.com/ossec/ossec-hids)



Lightweight HIDS with:



* log analysis

* FIM

* rootkit detection

* active response



---



## Velociraptor



[GitHub](https://github.com/Velocidex/velociraptor)



Excellent for:



* endpoint visibility

* digital forensics

* live response

* artifact collection

* hunting



---



## osquery



[GitHub](https://github.com/osquery/osquery)



Turns endpoint state into SQL-queryable data.



Example:



```sql

SELECT name, path, pid

FROM processes

WHERE name = 'powershell.exe';

```



A SIEM can use osquery results as high-value endpoint telemetry.



---



## GRR Rapid Response



[GitHub](https://github.com/google/grr)



Useful for:



* remote forensic collection

* endpoint investigation

* incident response



---



# Open-Source Network Security Telemetry



## Suricata



[GitHub](https://github.com/OISF/suricata)



Provides:



* IDS

* IPS

* network security monitoring

* EVE JSON

* protocol analysis



---



## Zeek



[GitHub](https://github.com/zeek/zeek)



Provides rich network metadata.



Example:



```text

Connection

DNS

HTTP

TLS

SSH

Files

Certificates

```



Zeek is especially valuable for threat hunting.



---



## Arkime



[GitHub](https://github.com/arkime/arkime)



Arkime provides large-scale packet capture indexing and network-session analysis.



---



## Suricata + Zeek + SIEM



A powerful open architecture is:



```text

Network

   ↓

Suricata

   +

Zeek

   ↓

Kafka / Fluent Bit

   ↓

OpenSearch

   ↓

SIEM

```



---



# Open-Source Threat Intelligence



## MISP



[GitHub](https://github.com/MISP/MISP)



MISP is a major open-source threat-intelligence platform.



It provides:



* indicators

* threat feeds

* events

* sharing

* enrichment

* correlation



---



## OpenCTI



[GitHub](https://github.com/OpenCTI-Platform/opencti)



OpenCTI provides graph-oriented threat intelligence.



Useful entities include:



```text

Threat Actor

Campaign

Malware

Infrastructure

Indicator

Vulnerability

Attack Pattern

Victim

```



---



## Yeti



[GitHub](https://github.com/yeti-platform/yeti)



Open-source platform for organizing and enriching threat intelligence.



---



## IntelOwl



[GitHub](https://github.com/intelowlproject/IntelOwl)



Provides automated intelligence analysis through multiple analyzers.



---



# Open-Source Detection Engineering



Detection engineering is one of the most important parts of a SIEM.



## Sigma



[GitHub](https://github.com/SigmaHQ/sigma)



Sigma provides a generic, shareable format for detection rules.



Example:



```yaml

title: Suspicious PowerShell

logsource:

  product: windows

  category: process_creation



detection:

  selection:

    Image|endswith: '\powershell.exe'

    CommandLine|contains:

      - '-enc'

      - 'EncodedCommand'



  condition: selection

```



Sigma allows detection logic to be translated into platform-specific queries.



---



## YARA



[GitHub](https://github.com/VirusTotal/yara)



YARA is primarily a malware and pattern-matching framework but can provide high-value detection signals to a SIEM.



---



## Suricata Rules



Suricata signatures can provide network detection.



---



## Zeek Scripts



Zeek's scripting language can create custom network detections.



---



## Falco



[GitHub](https://github.com/falcosecurity/falco)



Falco provides runtime security detection for:



* Linux

* containers

* Kubernetes

* cloud-native workloads



---



## Tetragon



[GitHub](https://github.com/cilium/tetragon)



Provides eBPF-based security observability and runtime enforcement.



---



# Open-Source Security Data Pipelines



Large SIEM deployments require reliable data transport.



## Fluent Bit



[GitHub](https://github.com/fluent/fluent-bit)



Lightweight log collector.



---



## Fluentd



[GitHub](https://github.com/fluent/fluentd)



Flexible log collection and routing.



---



## Vector



[GitHub](https://github.com/vectordotdev/vector)



High-performance observability data pipeline.



---



## OpenTelemetry Collector



[GitHub](https://github.com/open-telemetry/opentelemetry-collector)



Provides vendor-neutral telemetry collection and routing.



---



## Apache Kafka



[GitHub](https://github.com/apache/kafka)



Useful for:



* event buffering

* streaming

* decoupling collectors

* large-scale ingestion



---



## Apache NiFi



[GitHub](https://github.com/apache/nifi)



Visual dataflow platform suitable for security telemetry ingestion and transformation.



---



## Logstash



[GitHub](https://github.com/elastic/logstash)



A mature log-processing pipeline.



---



# Additional Strong Open-Source Options



## SIEM / Security Analytics



* [Wazuh](https://github.com/wazuh/wazuh)

* [Security Onion](https://github.com/Security-Onion-Solutions/securityonion)

* [OpenSearch](https://github.com/opensearch-project/OpenSearch)

* [Elastic Stack](https://github.com/elastic/elastic-stack)

* [OSSEC](https://github.com/ossec/ossec-hids)

* [AlienVault OSSIM](https://github.com/AlienVault-ossim/ossim)

* [Graylog](https://github.com/Graylog2/graylog2-server)

* [SIEMonster](https://github.com/SIEMonster)

* [MozDef](https://github.com/mozilla/MozDef)



## Network Detection



* [Suricata](https://github.com/OISF/suricata)

* [Zeek](https://github.com/zeek/zeek)

* [Arkime](https://github.com/arkime/arkime)

* [Snort](https://github.com/snort3/snort3)

* [Corelight Community Zeek](https://github.com/zeek)



## Endpoint



* [Wazuh](https://github.com/wazuh/wazuh)

* [OSSEC](https://github.com/ossec/ossec-hids)

* [Velociraptor](https://github.com/Velocidex/velociraptor)

* [osquery](https://github.com/osquery/osquery)

* [GRR](https://github.com/google/grr)



## Threat Intelligence



* [MISP](https://github.com/MISP/MISP)

* [OpenCTI](https://github.com/OpenCTI-Platform/opencti)

* [Yeti](https://github.com/yeti-platform/yeti)

* [IntelOwl](https://github.com/intelowlproject/IntelOwl)

* [SpiderFoot](https://github.com/smicallef/spiderfoot)



## Detection



* [Sigma](https://github.com/SigmaHQ/sigma)

* [YARA](https://github.com/VirusTotal/yara)

* [Falco](https://github.com/falcosecurity/falco)

* [Tetragon](https://github.com/cilium/tetragon)

* [Suricata](https://github.com/OISF/suricata)



## Visualization



* [Grafana](https://github.com/grafana/grafana)

* [OpenSearch Dashboards](https://github.com/opensearch-project/OpenSearch-Dashboards)

* [Kibana](https://github.com/elastic/kibana)

* [Metabase](https://github.com/metabase/metabase)

* [Apache Superset](https://github.com/apache/superset)



---



# Commercial Platform → Open-Source Equivalents



| Commercial / Hosted Platform               | Closest Open-Source Options          | Notes                                                |

| ------------------------------------------ | ------------------------------------ | ---------------------------------------------------- |

| **Splunk Enterprise Security**             | OpenSearch + Wazuh + Sigma + Kafka   | Strong general-purpose DIY SIEM                      |

| **Microsoft Sentinel**                     | Wazuh + OpenSearch + Kafka + MISP    | Cloud integrations require additional work           |

| **Google Security Operations / Chronicle** | OpenSearch + Wazuh + Kafka + OpenCTI | Large-scale architecture required                    |

| **Elastic Security**                       | Elastic Stack + Sigma                | Closest technology-family alternative                |

| **Exabeam**                                | Wazuh + OpenSearch + custom UEBA     | Behavioral analytics requires additional engineering |

| **Sumo Logic Cloud SIEM**                  | OpenSearch + Wazuh + Fluent Bit      | Cloud-native architecture can be assembled           |

| **LogRhythm**                              | Wazuh + OpenSearch + Security Onion  | Strong open-source combination                       |

| **Devo**                                   | OpenSearch + Kafka + Vector          | High-scale analytics architecture                    |

| **IBM QRadar**                             | Wazuh + OpenSearch + Sigma + TheHive | SIEM + case management                               |

| **Chronicle SIEM**                         | OpenSearch + Kafka + OpenCTI         | Requires distributed architecture                    |

| **FortiSIEM**                              | Wazuh + OpenSearch + Suricata + Zeek | Broad security telemetry                             |

| **Rapid7 InsightIDR**                      | Wazuh + Velociraptor + OpenSearch    | Endpoint + SIEM combination                          |

| **Securonix**                              | OpenSearch + Wazuh + custom UEBA     | UEBA is the major gap                                |

| **Trellix Helix**                          | Wazuh + OpenSearch + MISP            | Integrated detection/response alternative            |

| **AlienVault USM**                         | OSSIM + Wazuh + Security Onion       | Strong OSS lineage                                   |

| **ArcSight**                               | OpenSearch + Kafka + Sigma + Wazuh   | Event correlation stack                              |

| **RSA NetWitness**                         | Security Onion + Arkime + OpenSearch | Network-centric alternative                          |

| **Graylog Security**                       | Graylog + Wazuh / OpenSearch         | Verify current licensing/features                    |

| **Generic SIEM**                           | Wazuh + OpenSearch + Sigma           | Strong starting point                                |



---



# Frameworks for Building Custom SIEM Platforms



A complete open-source SIEM can be assembled from multiple layers.



## 1. Data Collection



```text

Endpoint

Server

Firewall

Router

Switch

Application

Cloud

Identity

Database

Container

Kubernetes

```



Collectors:



```text

Wazuh Agent

Fluent Bit

Fluentd

Vector

OpenTelemetry

Filebeat

Syslog

Kafka

```



---



# 2. Event Transport



Use:



* Apache Kafka

* Redpanda

* NATS

* RabbitMQ

* Apache Pulsar



For large-scale SIEM:



```text

Collectors

    ↓

Kafka

    ↓

Consumers

```



This decouples ingestion from indexing and detection.



---



# 3. Normalization



A SIEM needs a common schema.



Useful standards/frameworks include:



```text

ECS

OCSF

CEF

LEEF

Syslog

OpenTelemetry

```



A normalized event might look like:



```json

{

  "timestamp": "2026-09-09T12:00:00Z",

  "source": "endpoint",

  "event_type": "process_creation",

  "user": "alice",

  "host": "WORKSTATION-01",

  "process": "powershell.exe",

  "command_line": "powershell -enc ...",

  "severity": "high"

}

```



---



# 4. Storage



Potential open-source choices:



```text

OpenSearch

Elasticsearch

ClickHouse

PostgreSQL

VictoriaMetrics

Loki

```



For high-volume security analytics, ClickHouse is particularly interesting.



[GitHub](https://github.com/ClickHouse/ClickHouse)



---



# 5. Detection Engine



Possible detection engines:



```text

Sigma

Wazuh Rules

OpenSearch Security Analytics

Elastic Detection Rules

Suricata

Zeek

Falco

YARA

Custom SQL

Custom DSL

```



---



# 6. Correlation Engine



Example:



```text

Event 1:

Multiple failed logins



+



Event 2:

Successful login



+



Event 3:

New privileged session



+



Event 4:

Large data transfer



=



Potential Account Compromise

```



A custom correlation engine can use:



```text

Temporal windows

Sequence matching

Entity correlation

Risk scoring

Graph relationships

```



---



# 7. Threat Intelligence



```text

MISP

OpenCTI

Yeti

IntelOwl

Commercial APIs

```



---



# 8. UEBA



User and Entity Behavior Analytics can model:



```text

Normal login location

Normal login time

Normal device

Normal command usage

Normal data volume

Normal resource access

```



Possible open-source components:



* Python

* scikit-learn

* PyOD

* River

* XGBoost

* LightGBM

* ClickHouse

* OpenSearch



---



# 9. Case Management



Use:



* TheHive

* DFIR-IRIS

* OpenSearch dashboards

* custom applications



---



# 10. SOAR Integration



Connect the SIEM to:



* Shuffle

* StackStorm

* n8n

* Temporal

* Ansible



Architecture:



```text

SIEM

 ↓

Alert

 ↓

SOAR

 ↓

Response

```



---



# Reference Architecture



```mermaid

flowchart TD



    ENDPOINT[Endpoints]



    SERVERS[Servers]



    NETWORK[Network Devices]



    CLOUD[Cloud]



    IAM[Identity]



    APPS[Applications]



    EDR[Security Tools]



    COLLECT[Collectors]



    BUS[Event Bus]



    NORMALIZE[Normalization]



    STORE[(Security Data Lake)]



    DETECT[Detection Engine]



    TI[Threat Intelligence]



    UEBA[UEBA]



    CORRELATE[Correlation]



    ALERT[Alerts]



    CASE[Case Management]



    SOAR[SOAR]



    DASH[Dashboards]



    HUNT[Threat Hunting]



    ENDPOINT --> COLLECT

    SERVERS --> COLLECT

    NETWORK --> COLLECT

    CLOUD --> COLLECT

    IAM --> COLLECT

    APPS --> COLLECT

    EDR --> COLLECT



    COLLECT --> BUS

    BUS --> NORMALIZE

    NORMALIZE --> STORE



    STORE --> DETECT

    STORE --> UEBA

    STORE --> CORRELATE



    TI --> DETECT

    TI --> CORRELATE



    DETECT --> ALERT

    UEBA --> ALERT

    CORRELATE --> ALERT



    ALERT --> CASE

    CASE --> SOAR



    STORE --> HUNT

    STORE --> DASH

    ALERT --> DASH

```



---



# Typical SIEM Workflow



```mermaid

flowchart LR



    A[Security Event]



    B[Collect]



    C[Normalize]



    D[Store]



    E[Correlate]



    F[Detect]



    G[Enrich]



    H[Score]



    I[Alert]



    J[Investigate]



    K[Respond]



    A --> B

    B --> C

    C --> D

    D --> E

    E --> F

    F --> G

    G --> H

    H --> I

    I --> J

    J --> K

```



---



# Log Collection Workflow



```mermaid

flowchart TD



    WINDOWS[Windows]



    LINUX[Linux]



    FIREWALL[Firewall]



    CLOUD[Cloud]



    APPS[Applications]



    AGENTS[Agents / Collectors]



    BUS[Kafka / NATS]



    NORMALIZE[Normalization]



    SIEM[SIEM Storage]



    WINDOWS --> AGENTS

    LINUX --> AGENTS

    FIREWALL --> AGENTS

    CLOUD --> AGENTS

    APPS --> AGENTS



    AGENTS --> BUS

    BUS --> NORMALIZE

    NORMALIZE --> SIEM

```



---



# Detection Engineering Workflow



```mermaid

flowchart LR



    DATA[Security Telemetry]



    HYPOTHESIS[Detection Hypothesis]



    RULE[Sigma / Detection Rule]



    TEST[Test]



    TUNE[Tune]



    DEPLOY[Deploy]



    ALERT[Alert]



    FEEDBACK[Analyst Feedback]



    DATA --> HYPOTHESIS

    HYPOTHESIS --> RULE

    RULE --> TEST

    TEST --> TUNE

    TUNE --> DEPLOY

    DEPLOY --> ALERT

    ALERT --> FEEDBACK

    FEEDBACK --> TUNE

```



---



# Threat Hunting Workflow



```mermaid

flowchart TD



    HUNTER[Threat Hunter]



    QUERY[Query SIEM]



    FILTER[Filter Telemetry]



    CORRELATE[Correlate]



    TI[Threat Intelligence]



    HYPOTHESIS[Hypothesis]



    FINDING[Finding]



    DETECTION[New Detection]



    CASE[Investigation]



    HUNTER --> QUERY

    QUERY --> FILTER

    FILTER --> CORRELATE

    CORRELATE --> TI

    TI --> HYPOTHESIS



    HYPOTHESIS --> FINDING

    FINDING --> DETECTION

    FINDING --> CASE

```



---



# Incident Investigation Workflow



```mermaid

flowchart TD



    ALERT[SIEM Alert]



    TRIAGE[Triage]



    ENRICH[Threat Intelligence]



    ENDPOINT[Endpoint Evidence]



    NETWORK[Network Evidence]



    IDENTITY[Identity Evidence]



    CORRELATE[Correlate Evidence]



    CASE[Create Case]



    SOAR[Automated Response]



    CLOSE[Close]



    ALERT --> TRIAGE



    TRIAGE --> ENRICH

    TRIAGE --> ENDPOINT

    TRIAGE --> NETWORK

    TRIAGE --> IDENTITY



    ENRICH --> CORRELATE

    ENDPOINT --> CORRELATE

    NETWORK --> CORRELATE

    IDENTITY --> CORRELATE



    CORRELATE --> CASE

    CASE --> SOAR

    SOAR --> CLOSE

```



---



# Cloud SIEM Workflow



```mermaid

flowchart LR



    AWS[AWS]



    AZURE[Azure]



    GCP[GCP]



    SAAS[SaaS]



    IAM[Cloud Identity]



    COLLECT[Cloud Collectors]



    BUS[Event Bus]



    SIEM[SIEM]



    DETECT[Detection]



    ALERT[Alert]



    SOAR[SOAR]



    AWS --> COLLECT

    AZURE --> COLLECT

    GCP --> COLLECT

    SAAS --> COLLECT

    IAM --> COLLECT



    COLLECT --> BUS

    BUS --> SIEM

    SIEM --> DETECT

    DETECT --> ALERT

    ALERT --> SOAR

```



---



# SIEM Data Model



A normalized security event can contain:



```text

timestamp

event_id

event_type

source

destination

user

host

process

command_line

ip

port

protocol

application

cloud_account

resource

severity

action

outcome

threat_indicator

geo

authentication

```



A useful SIEM data model should support:



```text

Entity

   ↓

Event

   ↓

Relationship

   ↓

Detection

   ↓

Alert

   ↓

Incident

```



---



# Entity Model



Modern SIEMs increasingly correlate entities rather than simply individual log messages.



```text

User

  │

  ├── Device

  │

  ├── IP

  │

  ├── Session

  │

  ├── Application

  │

  └── Cloud Resource

```



Example:



```text

alice

  ↓

WORKSTATION-01

  ↓

10.10.10.25

  ↓

powershell.exe

  ↓

External IP

  ↓

Known malicious infrastructure

```



This is much more valuable than examining each event independently.



---



# SIEM Correlation Example



Suppose:



```text

Event 1:

10 failed logins



Event 2:

Successful login



Event 3:

MFA disabled



Event 4:

Privileged group membership changed



Event 5:

Large outbound transfer

```



The SIEM can correlate these events:



```text

10 Failed Logins

      +

Successful Login

      +

MFA Disabled

      +

Privilege Change

      +

Data Exfiltration

      ↓

ACCOUNT COMPROMISE

      ↓

HIGH / CRITICAL

```



---



# SIEM Risk Scoring



A custom SIEM can calculate:



```text

Risk =

Event Severity

+

Entity Risk

+

Threat Intelligence

+

Behavioral Anomaly

+

Privilege

+

Asset Criticality

```



Example:



```text

Critical Server

+

Privileged User

+

Known Malicious IP

+

Unusual Login

+

Large Data Transfer



        ↓



CRITICAL

```



---



# UEBA Architecture



```mermaid

flowchart TD



    EVENTS[User / Entity Events]



    FEATURES[Feature Extraction]



    BASELINE[Behavior Baseline]



    MODEL[ML / Statistical Model]



    ANOMALY[Anomaly Score]



    CONTEXT[Threat Intelligence]



    RISK[Risk Score]



    ALERT[Alert]



    EVENTS --> FEATURES

    FEATURES --> BASELINE

    FEATURES --> MODEL



    BASELINE --> ANOMALY

    MODEL --> ANOMALY



    ANOMALY --> RISK

    CONTEXT --> RISK



    RISK --> ALERT

```



Potential open-source ML components:



* [scikit-learn](https://github.com/scikit-learn/scikit-learn)

* [PyOD](https://github.com/yzhao062/pyod)

* [River](https://github.com/online-ml/river)

* [XGBoost](https://github.com/dmlc/xgboost)

* [LightGBM](https://github.com/microsoft/LightGBM)



---



# Detection Content



A mature SIEM needs a continuously maintained detection library.



Typical categories:



```text

Initial Access

Execution

Persistence

Privilege Escalation

Defense Evasion

Credential Access

Discovery

Lateral Movement

Collection

Command & Control

Exfiltration

Impact

```



MITRE ATT&CK can provide the conceptual framework.



---



# Sigma-Based SIEM Architecture



```text

Sigma Rule

    ↓

Validation

    ↓

Backend Conversion

    ↓

Platform Query

    ↓

Test Dataset

    ↓

Detection Engine

    ↓

Alert

```



This makes Sigma an important interoperability layer across SIEM platforms.



---



# Open-Source SIEM Stack: Minimal



```text

Wazuh

   +

Wazuh Dashboard

   +

Wazuh Indexer

```



Best for:



* small organizations

* labs

* universities

* endpoint-focused monitoring

* compliance

* initial SOC deployments



Wazuh's official documentation describes these three central components plus the Wazuh agent and confirms its free/open-source positioning.



---



# Open-Source SIEM Stack: Search-Centric



```text

Fluent Bit

    ↓

OpenSearch

    ↓

Security Analytics

    ↓

Sigma

    ↓

OpenSearch Dashboards

```



Best for:



* security analytics

* high-volume logs

* custom detection engineering

* teams comfortable with search infrastructure



---



# Open-Source SIEM Stack: Network-Centric



```text

Suricata

   +

Zeek

   +

Arkime

   +

Security Onion

```



Best for:



* network monitoring

* threat hunting

* packet analysis

* NDR-style operations



Security Onion explicitly combines network and host visibility, IDS, packet capture, log management and case management.



---



# Open-Source SIEM Stack: Full SOC



```text

Wazuh

   +

OpenSearch

   +

Security Onion

   +

MISP

   +

OpenCTI

   +

TheHive

   +

Cortex

   +

Velociraptor

   +

Shuffle

```



This creates:



```text

SIEM

+

NDR

+

HIDS/XDR

+

CTI

+

Case Management

+

SOAR

+

DFIR

```



---



# Capability Matrix



| Capability             |        Splunk ES |         Sentinel |    Google SecOps | Elastic Security |          Exabeam |            Wazuh |       OpenSearch |   Security Onion |            OSSIM |

| ---------------------- | ---------------: | ---------------: | ---------------: | ---------------: | ---------------: | ---------------: | ---------------: | ---------------: | ---------------: |

| Log ingestion          |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |

| Search                 |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |

| Correlation            |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |

| Detection rules        |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |

| Threat hunting         |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |

| UEBA                   |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |          Limited |          Limited |          Limited |          Limited |

| Endpoint telemetry     | Via integrations | Native ecosystem | Via integrations |                ✅ | Via integrations |                ✅ | Via integrations |                ✅ | Via integrations |

| Network telemetry      | Via integrations | Via integrations | Via integrations | Via integrations | Via integrations | Via integrations | Via integrations |                ✅ |                ✅ |

| Threat intelligence    |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ | Via integrations | Via integrations | Via integrations |                ✅ |

| Case management        |                ✅ |  Via integration |                ✅ |                ✅ |                ✅ |          Limited |          Limited |                ✅ |          Limited |

| SOAR integration       | Native ecosystem |           Native |           Native | Native ecosystem |           Native |  Via integration |  Via integration |  Via integration |  Via integration |

| ML / anomaly detection |                ✅ |                ✅ |                ✅ |                ✅ |           Strong |          Limited |                ✅ |          Limited |          Limited |

| Cloud-native           |          Partial |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |          Partial |          Partial |

| Self-hosted            |                ✅ |                ❌ |                ❌ |                ✅ |          Limited |                ✅ |                ✅ |                ✅ |                ✅ |

| Open source            |                ❌ |                ❌ |                ❌ |  Mixed licensing |                ❌ |                ✅ |                ✅ |    Open platform |   Historical OSS |

| Large-scale deployment |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |                ✅ |          Limited |



---



# Recommended Open-Source Stacks



## 1. Best Overall Open-Source SIEM



```text

Wazuh

   +

OpenSearch

   +

Sigma

   +

MISP

   +

TheHive

```



Why:



```text

Wazuh

 ↓

Endpoint + SIEM



OpenSearch

 ↓

Search + Analytics



Sigma

 ↓

Detection Engineering



MISP

 ↓

Threat Intelligence



TheHive

 ↓

Incident Management

```



---



# 2. Best Network-Centric Open-Source SIEM



```text

Security Onion

   +

Suricata

   +

Zeek

   +

Arkime

```



Best for:



* NDR

* network threat hunting

* packet capture

* network forensics



---



# 3. Best Search-Centric Stack



```text

OpenSearch

   +

Security Analytics

   +

Fluent Bit

   +

Sigma

   +

Kafka

```



Best for:



* high-volume logs

* centralized analytics

* custom SIEM development



---



# 4. Best Endpoint-Centric SIEM



```text

Wazuh

   +

Velociraptor

   +

OpenSearch

```



Best for:



* endpoint monitoring

* FIM

* vulnerability detection

* incident response

* threat hunting



---



# 5. Best Threat-Intelligence-Centric SIEM



```text

OpenSearch

   +

Wazuh

   +

MISP

   +

OpenCTI

   +

Cortex

```



---



# 6. Best Full Open-Source SOC



```text

                 Wazuh

                   │

                   ↓

              OpenSearch

                   │

        ┌──────────┼──────────┐

        ↓          ↓          ↓

      MISP      OpenCTI     Sigma

        │          │          │

        └──────────┼──────────┘

                   ↓

                TheHive

                   │

                   ↓

                Shuffle

                   │

        ┌──────────┼──────────┐

        ↓          ↓          ↓

  Velociraptor  Suricata     Zeek

```



---



# 7. Cloud-Native Open-Source Stack



```text

OpenTelemetry

      +

Kafka

      +

OpenSearch

      +

Wazuh

      +

Sigma

      +

MISP

      +

Shuffle

```



---



# 8. Kubernetes Security Stack



```text

Falco

   +

Tetragon

   +

OpenTelemetry

   +

Kafka

   +

OpenSearch

   +

Wazuh

   +

Grafana

```



Useful for:



* container runtime security

* Kubernetes events

* workload behavior

* cloud-native detection



---



# Example SIEM Repository



```text

open-siem/

│

├── collectors/

│   ├── windows/

│   ├── linux/

│   ├── firewall/

│   ├── cloud/

│   └── application/

│

├── pipelines/

│   ├── normalization/

│   ├── enrichment/

│   └── routing/

│

├── detections/

│   ├── sigma/

│   ├── wazuh/

│   ├── suricata/

│   └── custom/

│

├── correlation/

│   ├── authentication/

│   ├── endpoint/

│   ├── network/

│   └── cloud/

│

├── threat-intelligence/

│   ├── misp/

│   └── opencti/

│

├── dashboards/

│

├── hunting/

│

├── playbooks/

│

├── tests/

│

└── README.md

```



---



# SIEM Data Pipeline



```mermaid

flowchart LR



    SOURCES[Security Sources]



    COLLECT[Collectors]



    KAFKA[Kafka / Event Bus]



    NORMALIZE[Normalize]



    ENRICH[Enrich]



    STORE[Security Data Lake]



    DETECT[Detection]



    CORRELATE[Correlation]



    ALERT[Alert]



    HUNT[Threat Hunting]



    CASE[Case Management]



    SOURCES --> COLLECT

    COLLECT --> KAFKA

    KAFKA --> NORMALIZE

    NORMALIZE --> ENRICH

    ENRICH --> STORE



    STORE --> DETECT

    STORE --> HUNT

    DETECT --> CORRELATE

    CORRELATE --> ALERT

    ALERT --> CASE

```



---



# What Is Still Difficult to Reproduce in Open Source?



Even with Wazuh, OpenSearch, Security Onion, Elastic, OSSEC and the surrounding ecosystem, several capabilities remain difficult to reproduce as one unified platform.



## 1. Massive-Scale Ingestion



Enterprise SIEMs may ingest:



```text

Millions

to

Billions

of events per day

```



while maintaining:



```text

Low latency

+

High availability

+

Search performance

+

Retention

+

Cost control

```



This requires serious distributed infrastructure.



---



# 2. Mature Detection Content



A SIEM without detection content is essentially a log-search system.



Commercial platforms invest heavily in:



```text

Detection rules

Threat research

ATT&CK mappings

False-positive tuning

New threat coverage

Industry-specific content

```



Open-source users often need to build and maintain these themselves.



---



# 3. UEBA



Advanced behavioral analytics requires:



```text

Historical data

+

Feature engineering

+

Entity resolution

+

Statistical models

+

ML

+

Risk scoring

+

Continuous tuning

```



This is significantly harder than implementing a simple anomaly detector.



---



# 4. Cloud Telemetry



Cloud platforms produce huge numbers of heterogeneous events.



Examples:



```text

AWS CloudTrail

Azure Activity Logs

Microsoft Entra

GCP Audit Logs

Kubernetes

SaaS APIs

Cloud IAM

Cloud Network Flow Logs

```



Normalizing all of them into one coherent security model is challenging.



---



# 5. Detection Engineering at Scale



A production SOC may maintain:



```text

Hundreds

or

Thousands

of detections

```



Each needs:



```text

Testing

Mapping

Tuning

Versioning

Documentation

False-positive analysis

Performance monitoring

```



---



# 6. Search Performance



SIEM workloads are unusual because users simultaneously require:



```text

Recent searches

Historical searches

Aggregations

Joins

Correlations

Full-text search

Time-series analysis

Rare-event detection

```



This creates significant storage and compute requirements.



---



# 7. Data Retention Costs



The SIEM may store:



```text

Raw logs

Normalized logs

Alerts

Events

Network metadata

Packet captures

Endpoint telemetry

Threat intelligence

Audit logs

```



Long-term retention can become the dominant infrastructure cost.



---



# 8. AI-Assisted Investigation



Modern commercial SIEMs increasingly provide:



```text

Natural-language search

Alert summarization

Incident summaries

Detection generation

Threat-hunting assistance

Automated investigation

Entity analysis

```



An open-source implementation can use:



* local LLMs

* Ollama

* vLLM

* Open WebUI

* LangChain

* LlamaIndex



but production-grade security agents require careful:



```text

Authorization

+

Data isolation

+

Tool controls

+

Prompt security

+

Audit

+

Human approval

```



---



# Why Open Source Is Interesting



The most important open-source opportunity is not simply another log collector.



It is a complete:



> **Open-Source Security Analytics Platform**



combining:



```text

Telemetry

+

Data Lake

+

Detection

+

Correlation

+

Threat Intelligence

+

UEBA

+

Threat Hunting

+

Case Management

+

SOAR

```



A modular architecture can look like:



```text

                    Security Telemetry

                           │

       ┌───────────────────┼───────────────────┐

       ↓                   ↓                   ↓

    Wazuh              Suricata              Zeek

       │                   │                   │

       └───────────────────┼───────────────────┘

                           ↓

                        Kafka

                           ↓

                      OpenSearch

                           ↓

              ┌────────────┼────────────┐

              ↓            ↓            ↓

           Sigma          UEBA         MISP

              │            │            │

              └────────────┼────────────┘

                           ↓

                        Alerts

                           ↓

                        TheHive

                           ↓

                        Shuffle

                           ↓

                       Response

```



---



# Best Open-Source Projects by Use Case



| Use Case                  | Recommended Projects                   |

| ------------------------- | -------------------------------------- |

| Complete open-source SIEM | Wazuh                                  |

| Search-centric SIEM       | OpenSearch                             |

| Network-centric SOC       | Security Onion                         |

| Traditional HIDS          | OSSEC                                  |

| Historical OSS SIEM       | AlienVault OSSIM                       |

| Log management            | Graylog, OpenSearch, Loki              |

| Endpoint telemetry        | Wazuh, Velociraptor, osquery           |

| Network IDS               | Suricata                               |

| Network analysis          | Zeek, Arkime                           |

| Threat intelligence       | MISP, OpenCTI                          |

| Detection rules           | Sigma                                  |

| Malware detection         | YARA                                   |

| Container runtime         | Falco                                  |

| Kubernetes runtime        | Tetragon                               |

| Event streaming           | Kafka, NATS                            |

| Log collection            | Fluent Bit, Fluentd, Vector            |

| Telemetry                 | OpenTelemetry                          |

| Search                    | OpenSearch, Elasticsearch              |

| High-volume analytics     | ClickHouse                             |

| Dashboards                | Grafana, OpenSearch Dashboards, Kibana |

| Incident response         | TheHive, DFIR-IRIS                     |

| SOAR                      | Shuffle, StackStorm                    |

| Endpoint forensics        | Velociraptor, GRR                      |

| ML / UEBA                 | scikit-learn, PyOD, River              |

| Policy                    | OPA, Kyverno                           |



---



# Recommended Open-Source Shortlist



If the objective is to build a serious open-source alternative to the commercial SIEMs listed at the beginning of this README, the first projects to investigate are:



## Tier 1 — Complete SIEM / Security Platforms



1. [Wazuh](https://github.com/wazuh/wazuh)

2. [Security Onion](https://github.com/Security-Onion-Solutions/securityonion)

3. [OpenSearch](https://github.com/opensearch-project/OpenSearch)

4. [Elastic Stack](https://github.com/elastic/elastic-stack)

5. [OSSEC](https://github.com/ossec/ossec-hids)

6. [AlienVault OSSIM](https://github.com/AlienVault-ossim/ossim)



## Tier 2 — Security Data / Analytics



7. [OpenSearch Dashboards](https://github.com/opensearch-project/OpenSearch-Dashboards)

8. [Elasticsearch](https://github.com/elastic/elasticsearch)

9. [Kibana](https://github.com/elastic/kibana)

10. [Graylog](https://github.com/Graylog2/graylog2-server)

11. [ClickHouse](https://github.com/ClickHouse/ClickHouse)

12. [Grafana](https://github.com/grafana/grafana)



## Tier 3 — Detection



13. [Sigma](https://github.com/SigmaHQ/sigma)

14. [YARA](https://github.com/VirusTotal/yara)

15. [Suricata](https://github.com/OISF/suricata)

16. [Zeek](https://github.com/zeek/zeek)

17. [Falco](https://github.com/falcosecurity/falco)

18. [Tetragon](https://github.com/cilium/tetragon)



## Tier 4 — Intelligence / Response



19. [MISP](https://github.com/MISP/MISP)

20. [OpenCTI](https://github.com/OpenCTI-Platform/opencti)

21. [TheHive](https://github.com/TheHive-Project/TheHive)

22. [DFIR-IRIS](https://github.com/dfir-iris/iris-web)

23. [Cortex](https://github.com/TheHive-Project/Cortex)

24. [Shuffle](https://github.com/Shuffle/Shuffle)



---



# Practical Fully Open-Source SIEM/SOC Stack



A serious open-source implementation can use:



```text

                         Security Sources

                               │

            ┌──────────────────┼──────────────────┐

            ↓                  ↓                  ↓

          Wazuh             Suricata             Zeek

            │                  │                  │

            └──────────────────┼──────────────────┘

                               ↓

                            Kafka

                               ↓

                         OpenSearch

                               │

              ┌────────────────┼────────────────┐

              ↓                ↓                ↓

            Sigma             UEBA             MISP

              │                │                │

              └────────────────┼────────────────┘

                               ↓

                           Detection

                               ↓

                            TheHive

                               ↓

                            Shuffle

                               ↓

                   ┌───────────┼───────────┐

                   ↓           ↓           ↓

              Velociraptor  Identity     Firewall

                   │           │           │

                   └───────────┼───────────┘

                               ↓

                            Grafana

```



This provides an open-source architecture spanning:



* SIEM

* endpoint detection

* network detection

* threat intelligence

* detection engineering

* UEBA

* incident management

* SOAR

* endpoint response

* dashboards



---



# SIEM Maturity Model



```text

Level 1

---------

Centralized Logging



        ↓



Level 2

---------

Search + Dashboards



        ↓



Level 3

---------

Detection Rules



        ↓



Level 4

---------

Correlation + Alerting



        ↓



Level 5

---------

Threat Intelligence



        ↓



Level 6

---------

Threat Hunting + UEBA



        ↓



Level 7

---------

SOAR Integration



        ↓



Level 8

---------

AI-Assisted / Autonomous SOC

```



The key transition is from:



```text

Collecting Logs

```



to:



```text

Understanding Security Events

```



---



# SIEM + SOAR Architecture



A modern SOC should generally separate detection from response.



```text

SIEM

 │

 ├── Collect

 ├── Normalize

 ├── Detect

 ├── Correlate

 ├── Hunt

 └── Alert

        │

        ↓

      SOAR

        │

        ├── Enrich

        ├── Investigate

        ├── Approve

        ├── Respond

        └── Audit

```



Open-source combination:



```text

Wazuh / OpenSearch

        +

Shuffle

        +

TheHive

        +

Cortex

        +

MISP

```



---



# SIEM + Threat Intelligence



```mermaid

flowchart LR



    SIEM[SIEM]



    ALERT[Alert]



    IOC[Extract IOC]



    MISP[MISP]



    OPENCTI[OpenCTI]



    CORTEX[Cortex]



    SCORE[Risk Score]



    CASE[Incident]



    SIEM --> ALERT

    ALERT --> IOC



    IOC --> MISP

    IOC --> OPENCTI

    IOC --> CORTEX



    MISP --> SCORE

    OPENCTI --> SCORE

    CORTEX --> SCORE



    SCORE --> CASE

```



---



# SIEM + Endpoint Response



```mermaid

flowchart TD



    SIEM[SIEM Alert]



    WAZUH[Wazuh]



    VELO[Velociraptor]



    INVESTIGATE[Endpoint Investigation]



    DECISION{Confirmed?}



    ISOLATE[Isolate Endpoint]



    COLLECT[Collect Evidence]



    REMEDIATE[Remediate]



    SIEM --> WAZUH

    WAZUH --> VELO

    VELO --> INVESTIGATE

    INVESTIGATE --> DECISION



    DECISION -->|No| COLLECT

    DECISION -->|Yes| ISOLATE



    ISOLATE --> COLLECT

    COLLECT --> REMEDIATE

```



---



# SIEM + Network Detection



```text

Network Traffic

      ↓

Suricata

      +

Zeek

      +

Arkime

      ↓

Kafka / Vector

      ↓

OpenSearch

      ↓

Sigma / Correlation

      ↓

SIEM Alert

```



This is especially valuable for:



* command-and-control

* lateral movement

* DNS tunneling

* data exfiltration

* reconnaissance

* malicious TLS

* suspicious network behavior



---



# Open-Source SIEM Decision Tree



```text

Need a complete free SIEM?

        ↓

     Wazuh



Need network visibility?

        ↓

   Security Onion



Need search/analytics foundation?

        ↓

   OpenSearch



Need Elastic ecosystem?

        ↓

 Elastic Stack



Need lightweight HIDS?

        ↓

     OSSEC



Need threat intelligence?

        ↓

 MISP / OpenCTI



Need case management?

        ↓

 TheHive / DFIR-IRIS



Need SOAR?

        ↓

 Shuffle / StackStorm



Need network IDS?

        ↓

 Suricata / Zeek

```



---



# Conclusion



The SIEM ecosystem has evolved from centralized log collection into a broader security analytics architecture.



The modern SIEM can be represented as:



```text

                         SIEM

                          │

          ┌───────────────┼────────────────┐

          ↓               ↓                ↓

      Collection       Detection        Analytics

          │               │                │

      Wazuh          Sigma/Rules       OpenSearch

      Fluent Bit     Suricata           ClickHouse

      Vector         Zeek               Elasticsearch

          │               │                │

          └───────────────┼────────────────┘

                          ↓

                    Threat Intelligence

                          │

                    MISP / OpenCTI

                          ↓

                       Alerting

                          ↓

                     Investigation

                          ↓

                  TheHive / DFIR-IRIS

                          ↓

                        SOAR

                          ↓

                 Shuffle / StackStorm

                          ↓

                       Response

```



For organizations seeking an open-source alternative, there is no need to reproduce Splunk, Sentinel, Chronicle or QRadar as one monolithic product.



A better strategy is to combine specialized components:



```text

Wazuh

+

OpenSearch

+

Security Onion

+

Sigma

+

Suricata

+

Zeek

+

MISP

+

OpenCTI

+

TheHive

+

Shuffle

```



The most important open-source projects to evaluate first are therefore:



> **Wazuh + OpenSearch + Security Onion + Sigma + Suricata + Zeek + MISP + OpenCTI + TheHive + Shuffle.**



The most interesting opportunity is to build an integrated open-source security analytics platform around these projects that provides:



```text

Collect

 ↓

Normalize

 ↓

Store

 ↓

Detect

 ↓

Correlate

 ↓

Enrich

 ↓

Hunt

 ↓

Investigate

 ↓

Respond

 ↓

Learn

```



This architecture can reproduce a substantial portion of the functional surface traditionally associated with commercial SIEM platforms while retaining control over the underlying data, detection content and infrastructure.



---



# How to Contribute



Useful contributions include:



* adding new SIEM platforms

* adding open-source projects

* adding log collectors

* creating Sigma rules

* adding detection content

* documenting ATT&CK mappings

* adding threat-intelligence integrations

* improving parsers

* adding normalization schemas

* documenting cloud integrations

* creating dashboards

* adding threat-hunting queries

* benchmarking ingestion performance

* documenting storage architectures

* adding UEBA examples

* improving SOAR integrations

* creating incident-response workflows

* documenting high-availability deployments



Pull requests are welcome.



---



# Disclaimer



This README is an ecosystem overview rather than a security certification, product endorsement or guarantee of production readiness.



Open-source availability, licensing, detection coverage, supported integrations and project activity can change.



Before deploying an open-source SIEM, evaluate:



* ingestion capacity

* storage requirements

* retention policy

* detection quality

* false-positive rate

* search performance

* high availability

* disaster recovery

* authentication

* RBAC

* encryption

* audit logging

* threat-intelligence integration

* endpoint coverage

* network visibility

* cloud coverage

* detection engineering capability

* compliance requirements

* operational support



**A SIEM is not simply a log database.**



A production-grade security monitoring environment requires:



```text

Telemetry

+

Detection

+

Correlation

+

Threat Intelligence

+

Investigation

+

Response

+

Continuous Tuning

```



Open-source software can provide the technology for all of these layers, but the effectiveness of the resulting SOC ultimately depends on:



```text

Detection Content

+

Data Quality

+

Architecture

+

Engineering

+

Analyst Expertise

+

Continuous Tuning

```



> **The strongest open-source SIEM strategy is therefore not to find one "free Splunk." It is to assemble an open, modular security platform in which Wazuh/OpenSearch provide the analytics foundation, Sigma/Suricata/Zeek provide detection, MISP/OpenCTI provide intelligence, TheHive/DFIR-IRIS provide investigation and Shuffle/StackStorm provide response automation.**
