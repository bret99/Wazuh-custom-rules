# Jira tasks
1. mv get_jira_tasks.py /usr/local/bin && chown root:root /usr/local/bin/get_jira_tasks.py
2. mv get_jira_tasks.sh /usr/local/bin && chown root:root /usr/local/bin/get_jira_tasks.sh && chmod +x /usr/local/bin/get_jira_tasks.sh
3. make Wazuh agents group called as one like and add the next lines to agent.conf:
<agent_config>
	<!-- Shared agent configuration here -->
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/suricata/eve.json</location>
	</localfile>
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/jira/tasks.json</location>
	</localfile>
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/confluence/tasks.json</location>
	</localfile>
</agent_config>
4. add host with preinstalled wazuh agent to the group from 3rd point.
   
# Confluence tasks
1. mv get_confluence_tasks.py /usr/local/bin && chown root:root /usr/local/bin/get_confluence_tasks.py
2. mv get_confluence_tasks.sh /usr/local/bin && chown root:root /usr/local/bin/get_confluence_tasks.sh && chmod +x /usr/local/bin/get_confluence_tasks.sh
3. make Wazuh agents group called as one like and add the next lines to agent.conf:
<agent_config>
	<!-- Shared agent configuration here -->
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/suricata/eve.json</location>
	</localfile>
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/jira/tasks.json</location>
	</localfile>
	<localfile>
		<log_format>json</log_format>
		<location>/var/log/confluence/tasks.json</location>
	</localfile>
</agent_config>
4. add host with preinstalled wazuh agent to the group from 3rd point.
   
# Malware IPs
One should get malware IPs list from source one prefer and move this list to /var/ossec/etc/lists/malware_ips. Do not forget add ":" to the end of each line and restart wazuh-manager.
