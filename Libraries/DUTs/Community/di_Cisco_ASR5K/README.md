### Project Information:
Project: Cisco ASR 5000  
Description: Collection of response maps and QuickCalls applicable to Cisco ASR device testing  
Category: library  
Class: Community
 ----
2 quickcall libraries in project
## Quickcall Library: Cisco_ASR5K_telnet_quickcall_library.fftc
### Get clock value and convert to timestamp
Get timestamp from ASR5K and convert to format usable for "show logs".
### clearSubscriberInfo
```
Clear the subcriber info for the specified IMSI
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMSI</td><td>The IMSI of the UE to clear</tr></td></table>

### disableLogging
```
Disable logging on the ASR
```

### enableLogging
```
Enable the ASR logging
```

### getSystemTime
```
Get the system time from the ASR5K in the format: YYYY:MM:DD:hh:mm:ss

Return: JSON Block
sysTime: either the system time or "invalid"
```

### getTimestamp
```
Show the clock and return timestamp in YYYY:MM:DD:hh:mm:ss format
```

### Monitor_Protocol
```
Start a monitor protocol session 

NOTE: Monitor Protocol Never returns so this should be started in a thread and signalled by the main test case or a Fake Prompt should be passed to this procedure.

Return Value: JSON Block
status: 1 - success; 0 - failure
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>protocol_layers</td><tr></tr>
<tr><td>fakePrompt</td><td>If passed, iTest will look to terminate the Mon Sub when this text is found</tr></td>
<tr><td>waitForSignal</td><td>The name of the signal to wait for - if specified</tr></td></table>

### Monitor_Subscriber
```
Start a monitor subscriber session 

NOTE: Monitor Subscriber Never returns so this should be started in a thread and signalled by the main test case or a Fake Prompt should be passed to this procedure.

Return Value: JSON Block
status: 1 - success; 0 - failure
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMEI</td><td>If pased, this procedure will filter on this IMEI</tr></td>
<tr><td>IMSI</td><td>If pased, this procedure will filter on this IMSI</tr></td>
<tr><td>verbosity_level</td><td>The verbosity level to select: iTest will hit theh "+" the specified number of times</tr></td>
<tr><td>protocol_layers</td><tr></tr>
<tr><td>fakePrompt</td><td>If passed, iTest will look to terminate the Mon Sub when this text is found</tr></td>
<tr><td>waitForSignal</td><td>The name of the signal to wait for - if specified</tr></td></table>

### signalWaitCleanupLogging
```
Cleanup logging for a session when the "Cleanup" signal is activated.

This procedure is designed to run in a thread.

Return Value: Block
success: 0 - failure; 1 - success

```

### showLogs
```
Returns the logs since the timestamp value passed.

Return Value:
List of logs
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>timestamp</td><td>Get logs since <timestamp>

timestamp format:
YYYY:MM:DD:hh:mm:ss</tr></td></table>

### showSubscriber
```
Get subscriber information for the specified IMSI
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMSI</td><td>The IMSI values</tr></td>
<tr><td>full</td><td>1 - show subscriber full imsi; 0 - show subscriber imsi</tr></td></table>

### showSubscriberAll
## Quickcall Library: Cisco_ASR5K_ssh_quickcall_library.fftc
### clearSubscriberInfo
```
Clear the subcriber info for the specified IMSI
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMSI</td><td>The IMSI of the UE to clear</tr></td></table>

### disableLogging
```
Disable logging on the ASR
```

### enableLogging
```
Enable the ASR logging
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>captureTime</td><td>The amount of time to capture the logs</tr></td></table>

### getSystemTime
```
Get the system time from the ASR5K in the format: YYYY:MM:DD:hh:mm:ss

Return: JSON Block
sysTime: either the system time or "invalid"
```

### getTimestamp
```
Show the clock and return timestamp in YYYY:MM:DD:hh:mm:ss format
```

### isSubscriberActive
```
Based on the IMSI, see if the subscriber is in the active list

Return Values: JSON Block

active: nonzero - active; 0 - not active
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMSI</td><td>The IMSI of the desired subscriber</tr></td></table>

### configure_Monitor_Protocol
```
Start a monitor protocol session 

NOTE: Monitor Protocol Never returns so this should be started in a thread and signalled by the main test case or a Fake Prompt should be passed to this procedure.

Return Value: JSON Block
status: 1 - success; 0 - failure
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>protocol_layers</td><tr></tr>
<tr><td>fakePrompt</td><td>If passed, iTest will look to terminate the Mon Sub when this text is found</tr></td>
<tr><td>captureTime</td><td>The time to capture monSub in seconds</tr></td>
<tr><td>verbosity_level</td><td>The verbosity level to select: iTest will hit theh "+" the specified number of times</tr></td></table>

### configure_Monitor_Subscriber
```
Start a monitor subscriber session 

NOTE: Monitor Subscriber Never returns so this should be started in a thread and signalled by the main test case or a Fake Prompt should be passed to this procedure.

Return Value: JSON Block
status: 1 - success; 0 - failure
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMEI</td><td>If pased, this procedure will filter on this IMEI</tr></td>
<tr><td>IMSI</td><td>If pased, this procedure will filter on this IMSI</tr></td>
<tr><td>verbosity_level</td><td>The verbosity level to select: iTest will hit theh "+" the specified number of times</tr></td>
<tr><td>protocol_layers</td><tr></tr>
<tr><td>fakePrompt</td><td>If passed, iTest will look to terminate the Mon Sub when this text is found</tr></td>
<tr><td>captureTime</td><td>The time to capture monSub in seconds</tr></td></table>

### signalWaitCleanupLogging
```
Cleanup logging for a session when the "Cleanup" signal is activated.

This procedure is designed to run in a thread.

Return Value: Block
success: 0 - failure; 1 - success

```

### showLogs
```
Returns the logs since the timestamp value passed.

Return Value:
List of logs
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>timestamp</td><td>Get logs since <timestamp>

timestamp format:
YYYY:MM:DD:hh:mm:ss</tr></td></table>

### showSubscriber
```
Get subscriber information for the specified IMSI
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>IMSI</td><td>The IMSI values</tr></td>
<tr><td>full</td><td>1 - show subscriber full imsi; 0 - show subscriber imsi</tr></td></table>

### showSubscriberAll
### startCapture
```
Send a return and capture for the amount of time specified. This procedure will log autonomous messages such as debug logs, monitor subscriber and monitor protocol
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>captureTime</td><td>Send a return and capture for the amount of time specified. </tr></td>
<tr><td>fakePrompt</td><td>If passed, iTest will look to terminate the capture when this text is found</tr></td></table>

### showCallControlProfileName
```
Check if call control profile is set for PTMSI reallocation frequency every RAU in configuration, if not, attempt to set it.

return: frequency: >0(valid), =0(invalid)
```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>cc_profile</td><td>The call control profile to be set</tr></td></table>

### setPTMISIReallocateFrequency
```
Config PTMSI reallocation frequency.


```

<table><tr><th>Argument</th><th>Description</th></tr>
<tr><td>freq</td><tr></tr></table>

40 response maps in project
## Response Map File: T5_1_2_6-CDRSSentToCGFResponseMessage.ffrm
## Response Map File: T2_10MO_Cell_Reselection.ffrm
## Response Map File: T1_3-Detach_Timer.ffrm
## Response Map File: Attach_Request.ffrm
## Response Map File: T4.2SGSN_RoutingAreaUpdateAccept.ffrm
## Response Map File: REQ_RES_ACK_DEL_MessageType.ffrm
## Response Map File: T2_10_2MT_Cell_Reselection_ExtendedServiceRequestionMTCSFB.ffrm
## Response Map File: monitor_protocol.ffrm
## Response Map File: show_call_control_profile_full_name.ffrm
## Response Map File: TestCase6_1_6_2_PGW_sends_CCR-I_to_PCRF.ffrm
## Response Map File: Attach_Accept.ffrm
## Response Map File: T1_9_SPGW-S1AP_ContextReleaseRequest.ffrm
## Response Map File: IPv6Attach_Request.ffrm
## Response Map File: TAU_Accept.ffrm
## Response Map File: MonSubVerbosity.ffrm
## Response Map File: T4_2-SGSNAttachRequest.ffrm
## Response Map File: Detach_Request.ffrm
## Response Map File: TestCase6_1_6_2_PGW_sends_CCR-I_to_PCRF_rick.ffrm
## Response Map File: T1_9_SPGW-S1AP_ContextReleaseResponse.ffrm
## Response Map File: S1APPDUs.ffrm
## Response Map File: PathSwitchRequest.ffrm
## Response Map File: UE_Context_Modification.ffrm
## Response Map File: MessageInfo.ffrm
## Response Map File: id_paging.ffrm
## Response Map File: monSubMenu.ffrm
## Response Map File: T2_10_2MT_Cell_Reselection_MMESendPagingMessageCSCNDomain.ffrm
## Response Map File: show_subscribers_all.ffrm
## Response Map File: show_subscriber_imsi.ffrm
## Response Map File: T2_10_2MT_Cell_Reselection_MMESendSGxServiceRequestMessage.ffrm
## Response Map File: T5_1_2_6-IPv4v6_LTE_CDR_Generated_Request_Msg.ffrm
## Response Map File: T2_10_2MT_Cell_Reselection_PagingRequest.ffrm
## Response Map File: NAS_Msg_Security_Header.ffrm
## Response Map File: JsonBlockToQueries.ffrm
## Response Map File: PDN_Connectivity_Request.ffrm
## Response Map File: TestCase6_1_PGW_sends_CCR-I_to_PCRF-IPv4.ffrm
## Response Map File: TAU_Request.ffrm
## Response Map File: show_subscriber_full_imsi.ffrm
## Response Map File: TAU_Reject.ffrm
## Response Map File: EMM_Information.ffrm
## Response Map File: TestCase1_12-MO_SMS_connected_mode.ffrm