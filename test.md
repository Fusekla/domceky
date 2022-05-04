---
title: Postgre SQL
---

??? abstract "Document Control and Status"

    !!! info "Page Owner: @Alberto-Crego-Matas"

    !!! info "Status"
        - [X] Structure
        - [X] Draft
        - [ ] Reviewed
        - [ ] Ready

!!! warning
    Work in progrees. Pending data Production DDBB

## Database

PostgreSQL Version 11 - SaaS DDBB Administrate with IBM Cloud

=== "DEV - DirectStatDev"

    * Name: ibc01-mpc-001-pgsql01
    * Version PostgreSQL 11
    * Resource group: DirectStatDev
    * Resources:
      * 4GB RAM x 2 members = 8GB RAM
      * 1.5TB disk x 2 members = 3TB disk - 15360 IOPS/member
      * 4 cores x 2 members = 8 cores

    * Database Info:
      * Private Endpoint: `9026bbac-75f6-44bf-a50f-810d2911f436.659dc287bad647f9b4fe17c4e4c38dcc.private.databases.appdomain.cloud:31573`
      * Private PostgreSQL Endpoint: `postgres://$USERNAME:$PASSWORD@9026bbac-75f6-44bf-a50f-810d2911f436.659dc287bad647f9b4fe17c4e4c38dcc.private.databases.appdomain.cloud:31573/ibmclouddb?sslmode=verify-full`
      * Database Internal Name: `ibmclouddb`
      * TLS Enabled - Certificate inside the resource in IBM Cloud

    * Backup (SaaS Service):
      * Automatic backups are performed daily and retained for 30 days.
      * Point-in-time recovery maintains continuous incremental backups for the last 7 days.

    * Logging:
      * LogDNA: Lite Version - Only live logs (Not retained) - _The customer don't require more persistence_

    * Monitoring:
      * Link: Review the link in the chapter "Monitoring"

=== "DEV - Deols"

    * Name: ibc01-mpc-001-pgsql02
    * Version PostgreSQL 12
    * Resource group: DeolsDev
    * Resources:
      * 4GB RAM x 2 members = 8GB RAM
      * 100GB disk x 2 members = 200GB disk - 100 IOPS/member
      * 4 cores x 2 members = 8 cores

    * Database Info:
      * Private Endpoint: `7068397d-4e80-4a9b-a18b-476688be6c44.c13p25pf03djhc8of4jg.private.databases.appdomain.cloud:31573`
      * Private PostgreSQL Endpoint: `postgres://$USERNAME:$PASSWORD@7068397d-4e80-4a9b-a18b-476688be6c44.c13p25pf03djhc8of4jg.private.databases.appdomain.cloud:30579/ibmclouddb?sslmode=verify-full`
      * Database Internal Name: `ibmclouddb`
      * TLS Enabled - Certificate inside the resource in IBM Cloud

    * Backup (SaaS Service):
      * Automatic backups are performed daily and retained for 30 days.
      * Point-in-time recovery maintains continuous incremental backups for the last 7 days.

    * Logging:
      * LogDNA: Lite Version - Only live logs (Not retained) - _The customer don't require more persistence_

    * Monitoring:
      * Link: Review the link in the chapter "Monitoring"

=== "PRO - DirectStatProd"

    * Name: ibc01-mpc-002-pgsql01
    * Version PostgreSQL 11
    * Resource group: DirectStatProd
    * Resources:
      * 4GB RAM x 2 members = 8GB RAM
      * 1.5TB disk x 2 members = 3TB disk - 15360 IOPS/member
      * 4 cores x 2 members = 8 cores

    * Database Info:
      * Private Endpoint: `3a03f6ab-ecd2-4ba5-a8d4-bb9fa9d69aa2.bpb68u2f0gvaqgd0n64g.databases.appdomain.cloud`
      * Private PostgreSQL Endpoint: `postgres://$USERNAME:$PASSWORD@3a03f6ab-ecd2-4ba5-a8d4-bb9fa9d69aa2.bpb68u2f0gvaqgd0n64g.private.databases.appdomain.cloud:32185/ibmclouddb?sslmode=verify-full`
      * Database Internal Name: `ibmclouddb`
      * TLS Enabled - Certificate inside the resource in IBM Cloud

    * Backup (SaaS Service):
      * Automatic backups are performed daily and retained for 30 days.
      * Point-in-time recovery maintains continuous incremental backups for the last 7 days.

    * Logging:
      * LogDNA: Lite Version - Only live logs (Not retained) - _The customer don't require more persistence_

    * Monitoring:
      * Link: Review the link in the chapter "Monitoring"

    ---
    ### Replica
    * Name: ibc01-mpc-002-pgsql01-replica-5801c3
    * Version PostgreSQL 11
    * Resource group: DirectStatProd
    * Resources:
      * 8GB RAM x 1 members = 8GB RAM
      * 1.5TB disk = 15360 IOPS/member
      * 0 cores x 1 members = 0 cores

    * Database Info:
      * Private Endpoint: `9eeeeec6-6329-4e3f-8648-b1291da70d56.br38q28f0334iom5lv4g.databases.appdomain.cloud:30579`
      * Private PostgreSQL Endpoint: `postgres://$USERNAME:$PASSWORD@9eeeeec6-6329-4e3f-8648-b1291da70d56.br38q28f0334iom5lv4g.databases.appdomain.cloud:31091/ibmclouddb?sslmode=verify-full`
      * Database Internal Name: `ibmclouddb`
      * TLS Enabled - Certificate inside the resource in IBM Cloud

    * Backup (SaaS Service):
      * Automatic backups are performed daily and retained for 30 days.
      * Point-in-time recovery maintains continuous incremental backups for the last 7 days.

    * Logging:
      * LogDNA: Lite Version - Only live logs (Not retained) - _The customer don't require more persistence_

    * Monitoring:
      * The alerts were configured to Sysdig
