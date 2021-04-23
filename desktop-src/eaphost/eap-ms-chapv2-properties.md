---
title: Свойства пользователя MS-CHAPv2 EAP
description: Сведения о свойствах пользователя MS-CHAPv2 EAP. См. пример, который является экземпляром устаревшей схемы mschapv2userpropertiesv1.
ms.assetid: f360913d-be5d-4ef0-96c9-652e4d08d9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d1672d32b87fe98816fb5baeac791df343d0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104414005"
---
# <a name="eap-ms-chapv2-user-properties"></a><span data-ttu-id="edea2-104">Свойства пользователя MS-CHAPv2 EAP</span><span class="sxs-lookup"><span data-stu-id="edea2-104">EAP MS-CHAPv2 User Properties</span></span>

<span data-ttu-id="edea2-105">Этот образец является экземпляром устаревшей схемы [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="edea2-105">This sample is an instance of the [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) legacy schema.</span></span>

``` syntax
<?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
   <EapMethod>
     <eapCommon:Type>26</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1" 
     xmlns:MsChapV2="https://www.microsoft.com/provisioning/MsChapV2UserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>26</baseEap:Type> 
       <MsChapV2:EapType>
         <MsChapV2:Username>test</MsChapV2:Username> 
         <MsChapV2:Password>test</MsChapV2:Password> 
         <MsChapV2:LogonDomain>ias-domain</MsChapV2:LogonDomain> 
       </MsChapV2:EapType>
     </baseEap:Eap>
   </Credentials>
 </EapHostUserCredentials>
```

## <a name="related-topics"></a><span data-ttu-id="edea2-106">См. также</span><span class="sxs-lookup"><span data-stu-id="edea2-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edea2-107">Свойства пользователя</span><span class="sxs-lookup"><span data-stu-id="edea2-107">User Properties</span></span>](user-profiles.md)
</dt> <dt>

[<span data-ttu-id="edea2-108">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="edea2-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




