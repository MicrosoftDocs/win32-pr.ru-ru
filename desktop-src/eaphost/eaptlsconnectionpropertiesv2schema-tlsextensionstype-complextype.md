---
title: Сложный тип Тлсекстенсионстипе
description: Сведения о сложном типе Тлсекстенсионстипе. Этот тип обеспечивает будущие улучшения схемы.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793897"
---
# <a name="tlsextensionstype-complex-type"></a><span data-ttu-id="f82a2-104">Сложный тип Тлсекстенсионстипе</span><span class="sxs-lookup"><span data-stu-id="f82a2-104">TLSExtensionsType Complex Type</span></span>

<span data-ttu-id="f82a2-105">Сложный тип **тлсекстенсионстипе** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="f82a2-105">The **TLSExtensionsType** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="TLSExtensionsType">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="f82a2-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f82a2-106">Remarks</span></span>

<span data-ttu-id="f82a2-107">Элемент **тлсекстенсионстипе** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f82a2-107">The **TLSExtensionsType** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f82a2-108">См. также</span><span class="sxs-lookup"><span data-stu-id="f82a2-108">Related topics</span></span>

<dl> <span data-ttu-id="f82a2-109"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f82a2-109"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f82a2-110">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="f82a2-110">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f82a2-111">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f82a2-111">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f82a2-112">Сложные типы eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f82a2-112">eaptlsconnectionpropertiesv2 Complex Types</span></span>](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f82a2-113">**Тлсекстенсионс (Тлсекстенсионстипе)**</span><span class="sxs-lookup"><span data-stu-id="f82a2-113">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




