###Findings

##The investigation confirmed a system compromise characterized by the following:

    #Persistence Mechanism: An unauthorized entry was identified in the root crontab, configured to execute a hidden shell script every five minutes.

    #Evidence: The screenshot below shows the discovery of the malicious cron job via the cat command:
    [Evidence](terminal1.png)

Evidence Summary
Artifact Type	Path / Location	Description
Persistence	/var/spool/cron/crontabs/root	Confirmed malicious cron job execution.
Process Tree	live_response/process/pstree.txt	Captured system process hierarchy.
System State	live_response/process/ps.txt	Full snapshot of active processes.
Conclusion

The system was found to be compromised with a persistent backdoor. The identified malicious script (/tmp/.hidden_malware/malware.sh) was scheduled to run every five minutes, confirming unauthorized persistence.
