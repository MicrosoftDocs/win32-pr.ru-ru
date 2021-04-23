---
title: Свойства подключения PEAP-TLS
description: Сведения о свойствах подключения PEAP-TLS. См. пример, который является экземпляром устаревшей схемы eaptlsconnectionpropertiesv1.
ms.assetid: 1128b3f7-eba7-484e-a3d8-070d37e9c57f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa368ca49b93cff8fa3cd60620ec075bfb8d3a5
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104533557"
---
# <a name="peap-tls-connection-properties"></a><span data-ttu-id="3cb66-104">Свойства подключения PEAP-TLS</span><span class="sxs-lookup"><span data-stu-id="3cb66-104">PEAP-TLS Connection Properties</span></span>

<span data-ttu-id="3cb66-105">Этот образец является экземпляром устаревшей схемы [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb66-105">This sample is an instance of the [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) legacy schema..</span></span>

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon"
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1"
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1"
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <msPeap:EapType>
          <msPeap:ServerValidation>
            <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
            <msPeap:ServerNames /> 
            <msPeap:TrustedRootCA /> 
          </msPeap:ServerValidation>
          <msPeap:FastReconnect>true</msPeap:FastReconnect> 
          <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
          <baseEap:Eap>
            <baseEap:Type>13</baseEap:Type> 
            <eapTls:EapType>
              <eapTls:CredentialsSource>
                <eapTls:CertificateStore /> 
              </eapTls:CredentialsSource>
              <eapTls:ServerValidation>
                <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                <eapTls:ServerNames /> 
                <eapTls:TrustedRootCA /> 
              </eapTls:ServerValidation>
              <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
            </eapTls:EapType>
          </baseEap:Eap>
          <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
          <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
        </msPeap:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a><span data-ttu-id="3cb66-106">См. также</span><span class="sxs-lookup"><span data-stu-id="3cb66-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb66-107">Свойства соединения</span><span class="sxs-lookup"><span data-stu-id="3cb66-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="3cb66-108">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3cb66-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




