# Role Name:
- ansible-role-compliance-windows-security-options-policy-2019


# Description:
This Security Options Policy Role was based off the CIS specs for 2019 servers.   This role covers the "Security Options Policy" section only. The checks and remediation commands are for local settings only. Group Policy settings may override these settings. When the "remediate" variable is set to "YES", the role will try to remediate the server's setting(s) according to the CIS standards.  The defaults/main.yml file can be used to disable specific CIS items (i.e. "execute_<cis task #>") from executing. The default value in the defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means that the CIS item will execute at run time. Set the value to "NO" if you want to skip this CIS item in question from executing.


# Requirements:
Windows Ansible related pre-requisites 
Powershell 3.0 or higher


# Defaults file for ansible-role-compliance-windows-security-options-policy-2019.
# Variables:
Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| variable used to determine whether or not to remedaite
__LimitBlankPasswordUse_cis__ |"1"| CIS value.
__NoConnectedUser_cis__ |"1"| CIS value.
__SCENoApplyLegacyAuditPolicy_cis__ |"1"| CIS value.
__CrashOnAuditFail_cis__ |"1"| CIS value.
__AllocateDASD_cis__ |"0"| CIS value.
__AddPrinterDrivers_cis__ |"1"| CIS value.
__RequireSignOrSeal_cis__ |"1"| CIS value.
__SealSecureChannel_cis__ |"1"| CIS value.
__SignSecureChannel_cis__ |"1"| CIS value.
__DisablePasswordChange_cis__ |"0"| CIS value.
__RequireStrongKey_cis__ |"1"| CIS value.
__DontDisplayLastUserName_cis__ |"1"| CIS value.
__DisableCAD_cis__ |"0"| CIS value.
__InactivityTimeoutSecs_cis__ |"900"| CIS value.
__LegalNoticeText_cis__ |"IBM, Inc. and its subsidiaries computer systems are for the job related use of IBM personnel only. All information herein is the property of IBM and authorized employees have the right to monitor these systems at any time."| CIS value.
__LegalNoticeCaption_cis: "Logon notice:"| CIS value.
__PasswordExpiryWarning_cis__ |["5","6","7","8","9","10","11","12","13","14"]| CIS value.
__ForceUnlockLogon_cis__ |"1"| CIS value.
__ScRemoveOption_cis__ |"1"| CIS value.
__RequireSecuritySignature_cis__ |"1"| CIS value.
__EnableSecuritySignature_cis__ |"1"| CIS value.
__EnablePlainTextPassword_cis__ |"0"| CIS value.
__AutoDisconnect_cis__ |["1","2","3","4","5","6","7","8","9","10","11","12","13","14","15"]| CIS value.
__RequireSecuritySignature2_cis__ |"1"| CIS value.
__EnableSecuritySignature2_cis__ |"1"| CIS value.
__enableforcedlogoff_cis__ |"1"| CIS value.
__SMBServerNameHardeningLevel_cis__ |"1"| CIS value.
__RestrictAnonymousSAM_cis__ |"1"| CIS value.
__RestrictAnonymous_cis__ |"1"| CIS value.
__EveryoneIncludesAnonymous_cis__ |"0"| CIS value.
__RestrictNullSessAccess_cis__ |"0"| CIS value.
__ForceGuest_cis__ |"0"| CIS value.
__UseMachineId_cis__ |"1"| CIS value.
__RestrictAnonymous2_cis__ |"1"| CIS value.
__AllowOnlineID_cis__ |"1"| CIS value.
__SupportedEncryptionTypes_cis__ |"2147483640"| CIS value.
__NoLMHash_cis__ |"1"| CIS value.
__LmCompatibilityLevel_cis__ |"5"| CIS value.
__LDAPClientIntegrity_cis__ |"1"| CIS value.
__NTLMMinClientSec_cis__ |"537395200"| CIS value.
__NTLMMinServerSec_cis__ |"537395200"| CIS value.
__ShutdownWithoutLogon_cis__ |"1"| CIS value.
__ObCaseInsensitive_cis__ |"1"| CIS value.
__FilterAdministratorToken_cis__ |"1"| CIS value.
__EnableUIADesktopToggle_cis__ |"0"| CIS value.
__ConsentPromptBehaviorAdmin_cis__ |"2"| CIS value.
__ConsentPromptBehaviorUser_cis__ |"0"| CIS value.
__EnableInstallerDetection_cis__ |"1"| CIS value.
__EnableSecureUIAPaths_cis__ |"1"| CIS value.
__EnableLUA_cis__ |"1"| CIS value.
__PromptOnSecureDesktop_cis__ |"1"| CIS value.
__EnableVirtualization_cis__ |"1"| CIS value.
__MaximumPasswordAge_cis__ |30| CIS value.
__CachedLogonsCount_cis__ |4| CIS value.
__ProtectionMode_cis__ |1"| CIS value.
__EnableForcedLogoff_cis__ |"1"| CIS value.
__NullSessionShares_cis__ |""| CIS value.
__RestrictRemoteSAM_cis__ |"O:BAG:BAD:(A;;RC;;;BA)"| CIS value.
__Machine_cis__ |"too many to list"| CIS value.
__DisableDomainCreds_cis__ |"1"| CIS value.
__SubmitControl_cis__ |"0"| CIS value.
__LDAPServerIntegrity_cis__ |"2"| CIS value.
__RefusePasswordChange_cis__ |"0"| CIS value.
__Machine_cis1__ |"System\\CurrentControlSet\\Control\\Print\\Printers"| CIS value.
__Machine_cis2__ |"System\\CurrentControlSet\\Services\\Eventlog"| CIS value.
__Machine_cis3__ |"Software\\Microsoft\\OLAP Server"| CIS value.
__Machine_cis4__ |"Software\\Microsoft\\Windows NT\\CurrentVersion\\Print"| CIS value.
__Machine_cis5__ |"Software\\Microsoft\\Windows NT\\CurrentVersion\\Windows"| CIS value.
__Machine_cis6__ |"System\\CurrentControlSet\\Control\\ContentIndex"| CIS value.
__Machine_cis7__ |"System\\CurrentControlSet\\Control\\Terminal Server"| CIS value.
__Machine_cis8__ |"System\\CurrentControlSet\\Control\\Terminal Server\\UserConfig"| CIS value.
__Machine_cis9__ |"System\\CurrentControlSet\\Control\\Terminal Server\\DefaultUserConfiguration"| CIS value.
__Machine_cis10__ |"Software\\Microsoft\\Windows NT\\CurrentVersion\\Perflib"| CIS value.
__Machine_cis11__ |"System\\CurrentControlSet\\Services\\SysmonLog"| CIS value.
__Machine2_cis1__ |"System\\CurrentControlSet\\Control\\ProductOptions"| CIS value.
__Machine2_cis2__ |"System\\CurrentControlSet\\Control\\Server Applications"| CIS value.
__Machine2_cis3__ |"Software\\Microsoft\\Windows NT\\CurrentVersion"| CIS value.
__NullSessionPipes_cis__ |""| CIS value.
__NullSessionPipes2_cis__ |"netlogon, samr, lsarpc"| CIS value.


# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-security-options-policy-2019


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
