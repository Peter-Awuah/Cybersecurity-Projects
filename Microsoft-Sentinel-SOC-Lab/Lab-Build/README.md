## Lab Build
Objective

Built a Microsoft Sentinel environment capable of collecting Windows Security Events and generating actionable alerts.

---



## 1. Resource Group

Created a dedicated Azure Resource Group to host all SOC lab resources.


![Resource Group](screenshots/01-resource-group.png)

---



## 2. Log Analytics Workspace

Configured a Log Analytics Workspace to centralise security telemetry from monitored systems.


![Log Analytics Workspace](screenshots/02-Log-Analytics-workspace.png)

----




## 3. Microsoft Sentinel

Enabled Microsoft Sentinel and connected it to the Log Analytics Workspace.

![Microsoft Sentinel](screenshots/03-Sentinel-Workspace.png)

---



## 4. Domain Controller

Deployed a Windows Server 2022 virtual machine and configured it as a domain controller.

![Domain Controller](screenshots/04-soc-win01-vm.png)

---



## 5. Active Directory

Installed Active Directory Domain Services and created the CORP.LOCAL domain.

![Active Directory](screenshots/05-ad-ds-installation.png)

---


## 6. Users and Groups

Created users and security groups to simulate a production environment and RBAC implementation

Examples:

john.smith, sarah.jones, peter.admin

Groups:

SG_Finance
SG_IT
SG_Server_Admins

![Users and Groups](screenshots/06-active-directory-users.png)

![Users and Groups](screenshots/07-security-groups.png)

---



## 7. Domain Workstation

Deployed and joined SOC-CLIENT01 to the domain.

![Domain Workstation](screenshots/08-soc-client01.png)

---



## 8. Data Collection Rule

Created a Data Collection Rule to ingest Windows Security Events for both VMS

![Data Collection Rule](screenshots/09-data-collection-rule.png)


![Data Collection Rule](screenshots/09.1-collection-forVMS.png)

---





## 9. Validation

Verified successful log ingestion through Heartbeat events and Security Event logs.

![Validation](screenshots/10-heartbeat validation.png)


-----




## Lessons Learned
  How Microsoft Sentinel ingests telemetry.
  The importance of Data Collection Rules.
  Active Directory event monitoring.
  Building role-based access controls.
  Validating telemetry before building detections.



















