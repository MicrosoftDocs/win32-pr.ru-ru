---
title: Свойства пользователя EAP-TLS
description: Сведения о свойствах пользователя EAP-TLS. См. пример, который является экземпляром устаревшей схемы eaptlsuserpropertiesv1.
ms.assetid: d5a265a9-4c09-4a60-a188-dff471ee72c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb62acc8cbe5a56eb56152f8625bf3c9cfeb79fdf31558aa5de4bf131e82f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275186"
---
# <a name="eap-tls-user-properties"></a>Свойства пользователя EAP-TLS

Этот образец является экземпляром устаревшей схемы [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) .

``` syntax
 <?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials"> 
   <EapMethod>
     <eapCommon:Type>13</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsUserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>13</baseEap:Type> 
       <eapTls:EapType>
         <eapTls:Username>ias-domain\test</eapTls:Username> 
         <eapTls:UserCert /> 
       </eapTls:EapType>
     </baseEap:Eap>
   </Credentials>
 </EapHostUserCredentials>
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства пользователя](user-profiles.md)
</dt> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> </dl>

 

 




