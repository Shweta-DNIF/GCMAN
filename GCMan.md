# **GCMan**

## **Description of GCMan**

> GCMAN is a threat group that focuses on targeting banks for the purpose of transferring money to e-currency services. 
> It is a group that uses APT techniques and legitimate penetration testing tools to infect computer networks and attempt to steal funds by transferring money from financial institutions to e-currency services.

### **Technique Detection Strategies**

- TDS #1- Malicious connection through Putty
- TDS #2- Malicious connection through TeamViewer
- TDS #3- Malicious connection through AnyDesk
- TDS #4- Cron job execution every minute
- TDS #5- [URL IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)
- TDS #6- [Domain IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)
- TDS #7- [Hash IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)

### TDS #1- Malicious connection through Putty
Detecting this through Sysmon by monitoring event ID 3 for network connections using Putty and looking for malicious destinations IPs through Intel.

### TDS #2- Malicious connection through TeamViewer
Detecting this through Sysmon by monitoring event ID 3 for network connections using TeamViewer and looking for malicious destinations IPs through Intel.

### TDS #3- Malicious connection through AnyDesk
Detecting this through Sysmon by monitoring event ID 3 for network connections using AnyDesk and looking for malicious destinations IPs through Intel.

### TDS #4- Cron job execution every minute
Looking for cron jobs that are executed more than 10 times within 15 minutes.

### TDS #5- [URL IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)
Comparing URLs from live data to the URL IOC list uploaded and alerting if a match is found.

### TDS #6- [Domain IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)
Comparing domains from live data to the Domain IOC list uploaded and alerting if a match is found.

### TDS #7- [Hash IOC](https://media.kasperskycontenthub.com/wp-content/uploads/sites/43/2018/03/07195101/Gcman-AttackAgainstFinancialInstitutions.ioc)
Comparing hashes from live data to the Hash IOC list uploaded and alerting if a match is found.
