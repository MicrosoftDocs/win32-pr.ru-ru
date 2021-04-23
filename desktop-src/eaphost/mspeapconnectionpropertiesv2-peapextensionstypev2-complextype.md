---
title: Сложный тип PeapExtensionsTypeV2
description: Сведения о сложном типе PeapExtensionsTypeV2. Этот тип обеспечивает будущие улучшения схемы.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987897"
---
# <a name="peapextensionstypev2-complex-type"></a><span data-ttu-id="9a3c3-104">Сложный тип PeapExtensionsTypeV2</span><span class="sxs-lookup"><span data-stu-id="9a3c3-104">PeapExtensionsTypeV2 Complex Type</span></span>

<span data-ttu-id="9a3c3-105">Сложный тип **PeapExtensionsTypeV2** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="9a3c3-105">The **PeapExtensionsTypeV2** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="9a3c3-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a3c3-106">Remarks</span></span>

<span data-ttu-id="9a3c3-107">Элемент **PeapExtensionsTypeV2** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a3c3-107">The **PeapExtensionsTypeV2** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a3c3-108">См. также</span><span class="sxs-lookup"><span data-stu-id="9a3c3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a3c3-109">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="9a3c3-109">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9a3c3-110">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="9a3c3-110">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="9a3c3-111">Сложные типы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="9a3c3-111">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9a3c3-112">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="9a3c3-112">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




