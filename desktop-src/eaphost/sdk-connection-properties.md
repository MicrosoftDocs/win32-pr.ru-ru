---
title: Свойства подключения к пакету SDK
description: Сведения о свойствах подключения пакета SDK. См. пример, который является экземпляром собственной схемы еафостконфиг.
ms.assetid: 34c9b423-4f4c-484e-86d7-4594566cd396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbd404246055a3c94daff4c029a94f16adfe51b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797100"
---
# <a name="sdk-connection-properties"></a><span data-ttu-id="4e459-104">Свойства подключения к пакету SDK</span><span class="sxs-lookup"><span data-stu-id="4e459-104">SDK Connection Properties</span></span>

<span data-ttu-id="4e459-105">Этот образец является экземпляром собственной схемы [еафостконфиг](eaphostconfigschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="4e459-105">This sample is an instance of the [eaphostconfig](eaphostconfigschema-schema.md) native schema.</span></span>

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>40</eapCommon:Type> 
      <eapCommon:AuthorId>100</eapCommon:AuthorId> 
    </EapMethod>
    <Config>
      <EapType>40</EapType> 
      <ConfigData>seatac.bingo.com</ConfigData> 
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a><span data-ttu-id="4e459-106">См. также</span><span class="sxs-lookup"><span data-stu-id="4e459-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e459-107">Свойства соединения</span><span class="sxs-lookup"><span data-stu-id="4e459-107">Connection Properties</span></span>](connection-profiles.md)
</dt> <dt>

[<span data-ttu-id="4e459-108">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4e459-108">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




