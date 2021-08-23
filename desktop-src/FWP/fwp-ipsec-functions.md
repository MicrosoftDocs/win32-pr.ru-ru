---
title: Функции IPsec
description: Функции IPsec
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- Windows Функции IPsec для API платформы фильтрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccd557011547a06ce0ad232fa84341f56a1b7f7ebdf4281e04bcf715f19922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069224"
---
# <a name="ipsec-functions"></a>Функции IPsec

функции платформы фильтрации Windows (WFP), взаимодействующие с безопасностью протокола ip (IPsec), приведены ниже.

-   Фвпмипсектуннеладд:
    -   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)
    -   [**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)
    -   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)
-   [**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [**\_ \_ \_ \_ CHECK0 диктофона ключей диспетчера ключей \_ IPSec**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**\_Диспетчер ключей \_ IPSec \_ определяет \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_ \_ \_ Уведомление \_ Key0 диспетчера ключей IPsec**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_ \_ CALLBACK0 контекста SA \_ IPSec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecDospGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [**IPsecDospGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [**IPsecDospSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [**IPsecDospStateCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [**IPsecDospStateDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [**IPsecDospStateEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   Ипсекжетстатистикс:
    -   [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)
    -   [**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 и более поздних версий)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   Ипсексаконтекстаддинбаунд:
    -   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)
    -   [**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 и более поздних версий)
-   Ипсексаконтекстаддаутбаунд:
    -   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)
    -   [**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 и более поздних версий)
-   Ипсексаконтексткреате:
    -   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)
    -   [**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 и более поздних версий)
-   [**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [**IPsecSaContextDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   Ипсексаконтекстенум:
    -   [**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)
    -   [**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 и более поздних версий)
-   [**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   Ипсексаконтекстжетбид:
    -   [**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)
    -   [**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 и более поздних версий)
-   Ипсексаконтекстжетспи:
    -   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)
    -   [**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 и более поздних версий)
-   [**IPsecSaContextSetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaContextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [**IPsecSaDbGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [**IPsecSaDbSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [**IPsecSaDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   Ипсексаенум:
    -   [**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)
    -   [**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 и более поздних версий)

 

 