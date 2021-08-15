---
description: Представляет категории и подкатегории событий аудита политики.
ms.assetid: e3b12139-947d-4922-91fd-f9833c069011
title: Константы аудита (Нтсекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316dcd969ebba3cf571c7851a6d628617e4a261aea83c26b2524e3edcc0e4b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784312"
---
# <a name="auditing-constants"></a>Константы аудита

Следующие константы представляют категории и подкатегории событий аудита политики.

Следующие константы представляют категории событий аудита политики. Эти константы определяются как структуры **GUID** в нтсекапи. h.

<dl> <dt>

<span id="Audit_System"></span><span id="audit_system"></span><span id="AUDIT_SYSTEM"></span>**\_Система аудита**
</dt> <dd> <dl> <dt>

69979848-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит попытается завершить работу или перезагрузить компьютер. Кроме того, события аудита, влияющие на безопасность системы или журнал безопасности.


</dt> </dl> </dd> <dt>

<span id="Audit_Logon"></span><span id="audit_logon"></span><span id="AUDIT_LOGON"></span>**Аудит \_ входа**
</dt> <dd> <dl> <dt>

69979849-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит пытается войти в систему или выйти из нее. Кроме того, аудит пытается установить сетевое подключение.


</dt> </dl> </dd> <dt>

<span id="Audit_ObjectAccess"></span><span id="audit_objectaccess"></span><span id="AUDIT_OBJECTACCESS"></span>**\_Обжектакцесс аудита**
</dt> <dd> <dl> <dt>

6997984a-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит пытается получить доступ к защищаемым объектам.


</dt> </dl> </dd> <dt>

<span id="Audit_PrivilegeUse"></span><span id="audit_privilegeuse"></span><span id="AUDIT_PRIVILEGEUSE"></span>**\_Привилежеусе аудита**
</dt> <dd> <dl> <dt>

6997984b-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит пытается использовать [*привилегии*](/windows/desktop/SecGloss/p-gly).


</dt> </dl> </dd> <dt>

<span id="Audit_DetailedTracking"></span><span id="audit_detailedtracking"></span><span id="AUDIT_DETAILEDTRACKING"></span>**\_Детаиледтраккинг аудита**
</dt> <dd> <dl> <dt>

6997984c-797a-11d9-bed3-505054503030
</dt> <dt>



События, относящиеся к аудиту, такие как активация программы, некоторые формы дублирования, косвенный доступ к объекту и завершение процесса.


</dt> </dl> </dd> <dt>

<span id="Audit_PolicyChange"></span><span id="audit_policychange"></span><span id="AUDIT_POLICYCHANGE"></span>**\_Полицичанже аудита**
</dt> <dd> <dl> <dt>

6997984d-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит попытается изменить правила объекта [**политики**](/windows/desktop/SecMgmt/the-policy-object-type) .


</dt> </dl> </dd> <dt>

<span id="Audit_AccountManagement"></span><span id="audit_accountmanagement"></span><span id="AUDIT_ACCOUNTMANAGEMENT"></span>**Аудит \_ AccountManagement**
</dt> <dd> <dl> <dt>

6997984e-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит попытается создать, удалить или изменить учетные записи пользователей или групп. Кроме того, аудит изменений паролей.


</dt> </dl> </dd> <dt>

<span id="Audit_DirectoryServiceAccess"></span><span id="audit_directoryserviceaccess"></span><span id="AUDIT_DIRECTORYSERVICEACCESS"></span>**\_Директорисервицеакцесс аудита**
</dt> <dd> <dl> <dt>

6997984f-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит попытается получить доступ к службе каталогов.


</dt> </dl> </dd> <dt>

<span id="Audit_AccountLogon"></span><span id="audit_accountlogon"></span><span id="AUDIT_ACCOUNTLOGON"></span>**\_Аккаунтлогон аудита**
</dt> <dd> <dl> <dt>

69979850-797a-11d9-bed3-505054503030
</dt> <dt>



Аудит попыток входа привилегированными учетными записями, которые подключаются к контроллеру домена. Эти события аудита создаются, когда [*центр распространения ключей*](/windows/desktop/SecGloss/k-gly) Kerberos (KDC) входит в систему на контроллере домена.


</dt> </dl> </dd> </dl>

Следующие константы представляют подкатегории событий аудита политики. Эти константы определяются как структуры **GUID** в нтсекапи. h.

<dl> <span id="Audit_System_SecurityStateChange"></span><span id="audit_system_securitystatechange"></span><span id="AUDIT_SYSTEM_SECURITYSTATECHANGE"></span>**Аудит \_ System \_ секуритистатечанже** (0cce9210-69ae-11d9-bed3-505054503030) <span id="Audit_System_SecuritySubsystemExtension"></span> <span id="audit_system_securitysubsystemextension"></span> <span id="AUDIT_SYSTEM_SECURITYSUBSYSTEMEXTENSION"></span> **Аудит \_ системы \_ аудита System секуритисубсистемекстенсион** (0cce9211-69ae-11d9-bed3-505054503030) <span id="Audit_System_Integrity"></span> <span id="audit_system_integrity"></span> <span id="AUDIT_SYSTEM_INTEGRITY"></span> **Аудит системы \_ \_ целостность** систем <span id="Audit_System_IPSecDriverEvents"></span> <span id="audit_system_ipsecdriverevents"></span> <span id="AUDIT_SYSTEM_IPSECDRIVEREVENTS"></span> **\_ \_ 0cce9212-69ae-11d9-bed3-505054503030** (ипсекдриверевентс) аудит системы другие (0cce9213-69ae-11d9-bed3-505054503030) аудит входа в систему (0cce9214-69ae-11d9-bed3-505054503030) аудит входа в систему (0cce9215-69ae-11d9-bed3-505054503030 <span id="Audit_System_Others"></span> <span id="audit_system_others"></span> <span id="AUDIT_SYSTEM_OTHERS"></span> **\_ \_** <span id="Audit_Logon_Logon"></span> <span id="audit_logon_logon"></span> <span id="AUDIT_LOGON_LOGON"></span> **\_ \_** <span id="Audit_Logon_Logoff"></span> <span id="audit_logon_logoff"></span> <span id="AUDIT_LOGON_LOGOFF"></span> ) аудит **\_ \_** входа <span id="Audit_Logon_AccountLockout"></span> <span id="audit_logon_accountlockout"></span> <span id="AUDIT_LOGON_ACCOUNTLOCKOUT"></span> **\_ \_ 0cce9216-69ae-11d9-bed3-505054503030** (аккаунтлоккаут) <span id="Audit_Logon_IPSecMainMode"></span> <span id="audit_logon_ipsecmainmode"></span> <span id="AUDIT_LOGON_IPSECMAINMODE"></span> **Аудит входа в систему \_ \_ 0cce9217-69ae-11d9-bed3-505054503030** (IPSecMainMode <span id="Audit_Logon_IPSecQuickMode"></span> <span id="audit_logon_ipsecquickmode"></span> <span id="AUDIT_LOGON_IPSECQUICKMODE"></span> ) **Аудит \_ Вход в систему \_ ипсеккуиккмоде** (0cce9219-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_IPSecUserMode"></span> <span id="audit_logon_ipsecusermode"></span> <span id="AUDIT_LOGON_IPSECUSERMODE"></span> **Аудит \_ входа \_ ипсекусермоде** (0cce921a-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_SpecialLogon"></span> <span id="audit_logon_speciallogon"></span> <span id="AUDIT_LOGON_SPECIALLOGON"></span> **Аудит \_ входа \_ спеЦиаллогон** (0cce921b-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_Others"></span> <span id="audit_logon_others"></span> <span id="AUDIT_LOGON_OTHERS"></span> **Аудит \_ входа в \_ другие пользователи** (0cce921c-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FileSystem"></span> <span id="audit_objectaccess_filesystem"></span> <span id="AUDIT_OBJECTACCESS_FILESYSTEM"></span> **Audit \_ обжектакцесс \_ FileSystem** (0cce921d-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Registry"></span> <span id="audit_objectaccess_registry"></span> <span id="AUDIT_OBJECTACCESS_REGISTRY"></span> **Audit \_ обжектакцесс \_ Реестр** (0cce921e-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Kernel"></span> <span id="audit_objectaccess_kernel"></span> <span id="AUDIT_OBJECTACCESS_KERNEL"></span> **Audit \_ обжектакцесс \_ ядре** (0cce921f-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Sam"></span> <span id="audit_objectaccess_sam"></span> <span id="AUDIT_OBJECTACCESS_SAM"></span> **Audit \_ ObjectAccess \_ SAM** (0cce9220-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_CertificationServices"></span> <span id="audit_objectaccess_certificationservices"></span> <span id="AUDIT_OBJECTACCESS_CERTIFICATIONSERVICES"></span> **Audit \_ ObjectAccess \_ CertificationServices** ( 0cce9221-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_ApplicationGenerated"></span> <span id="audit_objectaccess_applicationgenerated"></span> <span id="AUDIT_OBJECTACCESS_APPLICATIONGENERATED"></span> **Audit \_ обжектакцесс \_ аппликатионженератед** (0cce9222-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Handle"></span> <span id="audit_objectaccess_handle"></span> <span id="AUDIT_OBJECTACCESS_HANDLE"></span> **Audit \_ обжектакцесс \_ Handle** (0cce9223-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Share"></span> <span id="audit_objectaccess_share"></span> <span id="AUDIT_OBJECTACCESS_SHARE"></span> **Audit \_ обжектакцесс \_ поделиться** (0cce9224-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FirewallPacketDrops"></span> <span id="audit_objectaccess_firewallpacketdrops"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLPACKETDROPS"></span> **Audit \_ обжектакцесс \_ фиреваллпаккетдропс** (0cce9225-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_FirewallConnection"></span> <span id="audit_objectaccess_firewallconnection"></span> <span id="AUDIT_OBJECTACCESS_FIREWALLCONNECTION"></span> **Audit \_ ObjectAccess \_ FirewallConnection** (0cce9226-69ae-11d9-bed3-505054503030) <span id="Audit_ObjectAccess_Other"></span> <span id="audit_objectaccess_other"></span> <span id="AUDIT_OBJECTACCESS_OTHER"></span> **Audit \_ ObjectAccess \_ другой** (0cce9227-69ae-11d9-bed3-505054503030) <span id="Audit_PrivilegeUse_Sensitive"></span> <span id="audit_privilegeuse_sensitive"></span> <span id="AUDIT_PRIVILEGEUSE_SENSITIVE"></span> **Audit \_ PrivilegeUse \_ конфиденциальный** (0cce9228-69ae-11d9-bed3-505054503030) <span id="Audit_PrivilegeUse_NonSensitive"></span> <span id="audit_privilegeuse_nonsensitive"></span> <span id="AUDIT_PRIVILEGEUSE_NONSENSITIVE"></span> **Audit \_ PrivilegeUse \_ Нечувствительный** (0cce9229-69ae-11d9-bed3-505054503030) <span id="Audit_PrivilegeUse_Others"></span> <span id="audit_privilegeuse_others"></span> <span id="AUDIT_PRIVILEGEUSE_OTHERS"></span> **Аудит \_ привилежеусе \_ другие** (0cce922a-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessCreation"></span> <span id="audit_detailedtracking_processcreation"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSCREATION"></span> **Audit \_ детаиледтраккинг \_ процесскреатион** (0cce922b-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_ProcessTermination"></span> <span id="audit_detailedtracking_processtermination"></span> <span id="AUDIT_DETAILEDTRACKING_PROCESSTERMINATION"></span> **Audit \_ детаиледтраккинг \_ процесстерминатион** (0cce922c-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_DpapiActivity"></span> <span id="audit_detailedtracking_dpapiactivity"></span> <span id="AUDIT_DETAILEDTRACKING_DPAPIACTIVITY"></span> **Audit \_ DetailedTracking \_ DpapiActivity** (0cce922d-69ae-11d9-bed3-505054503030) <span id="Audit_DetailedTracking_RpcCall"></span> <span id="audit_detailedtracking_rpccall"></span> <span id="AUDIT_DETAILEDTRACKING_RPCCALL"></span> **Audit \_ DetailedTracking \_ RpcCall** (0cce922e-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuditPolicy"></span> <span id="audit_policychange_auditpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUDITPOLICY"></span> **Audit \_ PolicyChange \_ AuditPolicy** (0cce922f-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuthenticationPolicy"></span> <span id="audit_policychange_authenticationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHENTICATIONPOLICY"></span> **Audit \_ PolicyChange \_ AuthenticationPolicy** (0cce9230-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_AuthorizationPolicy"></span> <span id="audit_policychange_authorizationpolicy"></span> <span id="AUDIT_POLICYCHANGE_AUTHORIZATIONPOLICY"></span> **Audit \_ полицичанже \_ AuthorizationPolicy** (0cce9231-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_MpsscvRulePolicy"></span> <span id="audit_policychange_mpsscvrulepolicy"></span> <span id="AUDIT_POLICYCHANGE_MPSSCVRULEPOLICY"></span> **Аудит \_ полицичанже \_ мпсскврулеполици** (0cce9232-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_WfpIPSecPolicy"></span> <span id="audit_policychange_wfpipsecpolicy"></span> <span id="AUDIT_POLICYCHANGE_WFPIPSECPOLICY"></span> **Audit \_ полицичанже \_ вфпипсекполици** (0cce9233-69ae-11d9-bed3-505054503030) <span id="Audit_PolicyChange_Others"></span> <span id="audit_policychange_others"></span> <span id="AUDIT_POLICYCHANGE_OTHERS"></span> **Audit \_ полицичанже \_** Other (0cce9234-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_UserAccount"></span> <span id="audit_accountmanagement_useraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_USERACCOUNT"></span> **Audit \_ AccountManagement \_ UserAccount** (0cce9235-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ComputerAccount"></span> <span id="audit_accountmanagement_computeraccount"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_COMPUTERACCOUNT"></span> **Audit \_ AccountManagement \_ ComputerAccount** (0cce9236-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_SecurityGroup"></span> <span id="audit_accountmanagement_securitygroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_SECURITYGROUP"></span> **Аудит \_ AccountManagement \_ SecurityGroup** (0cce9237-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_DistributionGroup"></span> <span id="audit_accountmanagement_distributiongroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_DISTRIBUTIONGROUP"></span> **Audit \_ AccountManagement \_ DistributionGroup**(0cce9238-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_ApplicationGroup"></span> <span id="audit_accountmanagement_applicationgroup"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_APPLICATIONGROUP"></span> **Аудит \_ AccountManagement \_ ApplicationGroup** (0cce9239-69ae-11d9-bed3-505054503030) <span id="Audit_AccountManagement_Others"></span> <span id="audit_accountmanagement_others"></span> <span id="AUDIT_ACCOUNTMANAGEMENT_OTHERS"></span> **Audit \_ AccountManagement \_** Other (0cce923a-69ae-11d9-bed3-505054503030) <span id="Audit_DSAccess_DSAccess"></span> <span id="audit_dsaccess_dsaccess"></span> <span id="AUDIT_DSACCESS_DSACCESS"></span> **Audit \_ DSAccess \_ DSAccess** (0cce923b-69ae-11d9-bed3-505054503030) <span id="Audit_DsAccess_AdAuditChanges"></span> <span id="audit_dsaccess_adauditchanges"></span> <span id="AUDIT_DSACCESS_ADAUDITCHANGES"></span> **Audit \_ DSAccess \_ адаудитчанжес** (0cce923c-69ae-11d9-bed3-505054503030) <span id="Audit_Ds_Replication"></span> <span id="audit_ds_replication"></span> <span id="AUDIT_DS_REPLICATION"></span> **Аудит \_ DS \_ Replication** (0cce923d-69ae-11d9-bed3-505054503030) <span id="Audit_Ds_DetailedReplication"></span> <span id="audit_ds_detailedreplication"></span> <span id="AUDIT_DS_DETAILEDREPLICATION"></span> **Audit \_ DS \_ детаиледрепликатион** (0cce923e-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_CredentialValidation"></span> <span id="audit_accountlogon_credentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_CREDENTIALVALIDATION"></span> **Audit \_ аккаунтлогон \_ кредентиалвалидатион** (0cce923f-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Kerberos"></span> <span id="audit_accountlogon_kerberos"></span> <span id="AUDIT_ACCOUNTLOGON_KERBEROS"></span> **Audit \_ аккаунтлогон \_ Kerberos** (0cce9240-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_Others"></span> <span id="audit_accountlogon_others"></span> <span id="AUDIT_ACCOUNTLOGON_OTHERS"></span> **Audit \_ аккаунтлогон \_** Other (0cce9241-69ae-11d9-bed3-505054503030) <span id="Audit_AccountLogon_KerbCredentialValidation"></span> <span id="audit_accountlogon_kerbcredentialvalidation"></span> <span id="AUDIT_ACCOUNTLOGON_KERBCREDENTIALVALIDATION"></span> **Audit \_ аккаунтлогон \_ кербкредентиалвалидатион** (0cce9242-69ae-11d9-bed3-505054503030) <span id="Audit_Logon_NPS"></span> <span id="audit_logon_nps"></span> <span id="AUDIT_LOGON_NPS"></span> **Аудит \_ входа в систему \_ NPS** (0cce9243-69ae-11d9-bed3-505054503030)
</dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Нтсекапи. h</dt> </dl> |



 

