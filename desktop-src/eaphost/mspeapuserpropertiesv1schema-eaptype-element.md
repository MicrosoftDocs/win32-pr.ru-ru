---
title: Элемент Еаптипе (mspeapuserpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187837"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="9725c-105">Элемент Еаптипе (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="9725c-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="9725c-106">Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="9725c-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="9725c-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9725c-107">Child elements</span></span>



| <span data-ttu-id="9725c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9725c-108">Element</span></span>                                                                               | <span data-ttu-id="9725c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="9725c-109">Type</span></span>                                                                                      | <span data-ttu-id="9725c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9725c-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9725c-111">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="9725c-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="9725c-112">Элемент [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) определяет внутренний метод и учетные данные для использования с этим методом.</span><span class="sxs-lookup"><span data-stu-id="9725c-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="9725c-113">Если конфигурация PEAP настроена для гостевого доступа по протоколу PEAP, этот элемент отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9725c-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="9725c-114">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="9725c-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="9725c-115">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="9725c-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="9725c-116">Элемент [**пеапекстенсионс**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="9725c-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="9725c-117">Элемент [**пеапекстенсионс**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9725c-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9725c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9725c-118">Requirements</span></span>



| <span data-ttu-id="9725c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9725c-119">Requirement</span></span> | <span data-ttu-id="9725c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9725c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9725c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9725c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9725c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9725c-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9725c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9725c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9725c-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9725c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9725c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9725c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9725c-126">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="9725c-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9725c-127">Схема mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9725c-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





