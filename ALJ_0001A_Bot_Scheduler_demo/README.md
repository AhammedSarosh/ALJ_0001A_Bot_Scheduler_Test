
### ALJ_0001A_Bot_Scheduler ###
**Bot Schedule process**
 
 LE Framework Process to control the process tiriggers of ALJ Bank Statment download dipatcher process based as per business requirments schedule



### How It Works ###

1. **INITIALIZE PROCESS**
 + ./Framework/*InitiAllSettings* - Load configuration data from Config.xlsx file and from assets
 + ./Framework/*GetAppCredential* - Retrieve credentials from Orchestrator assets or local Windows Credential Manager
 + ./Framework/*InitiAllApplications* - Open and login to applications used throughout the process

2. **PROCESS TRANSACTION**
 + *Process* - Process trasaction and invoke other workflows related to the process being automated 
 + ./Framework/*SetTransactionStatus* - Updates the status of the processed transaction (Orchestrator transactions by default): Success, Business Rule Exception or System Exception

3. **END PROCESS**
 + ./Framework/*CloseAllApplications* - Logs out and closes applications used throughout the process
