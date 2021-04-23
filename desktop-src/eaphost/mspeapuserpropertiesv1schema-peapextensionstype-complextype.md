---
title: Сложный тип Пеапекстенсионстипе (свойства соединения)
description: Сведения о сложном типе Пеапекстенсионстипе. Этот тип обеспечивает будущие улучшения схемы.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Пеапекстенсионстипе сложный тип EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339276"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="579f8-105">Сложный тип Пеапекстенсионстипе (свойства соединения)</span><span class="sxs-lookup"><span data-stu-id="579f8-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="579f8-106">Сложный тип **пеапекстенсионстипе** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="579f8-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="579f8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="579f8-107">Remarks</span></span>

<span data-ttu-id="579f8-108">Сложный тип **пеапекстенсионстипе** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="579f8-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="579f8-109">Требования</span><span class="sxs-lookup"><span data-stu-id="579f8-109">Requirements</span></span>



| <span data-ttu-id="579f8-110">Роль</span><span class="sxs-lookup"><span data-stu-id="579f8-110">Role</span></span> | <span data-ttu-id="579f8-111">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="579f8-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="579f8-112">Клиент</span><span class="sxs-lookup"><span data-stu-id="579f8-112">Client</span></span><br/> | <span data-ttu-id="579f8-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="579f8-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="579f8-114">Сервер</span><span class="sxs-lookup"><span data-stu-id="579f8-114">Server</span></span><br/> | <span data-ttu-id="579f8-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="579f8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="579f8-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="579f8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579f8-117">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="579f8-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="579f8-118">Схема mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="579f8-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





