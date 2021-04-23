---
title: Простой тип emptyString
description: Сведения о простом типе emptyString, который не используется. См. раздел требования и просмотрите дополнительные доступные ресурсы.
ms.assetid: e561b8d5-8683-41a1-bd72-73b1a767b6cf
keywords:
- emptyString простой тип EAPHost
topic_type:
- apiref
api_name:
- emptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 756c8976c8b989cf77be921491770fcff9ea62d5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070643"
---
# <a name="emptystring-simple-type"></a><span data-ttu-id="ca771-105">Простой тип emptyString</span><span class="sxs-lookup"><span data-stu-id="ca771-105">emptyString Simple Type</span></span>

<span data-ttu-id="ca771-106">Простой тип **emptyString** не используется.</span><span class="sxs-lookup"><span data-stu-id="ca771-106">The **emptyString** simple type is not in use.</span></span>

``` syntax
<xs:simpleType name="emptyString">
    <xs:restriction
        base="string"
    >
        <xs:maxLength
            value="0"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="ca771-107">Требования</span><span class="sxs-lookup"><span data-stu-id="ca771-107">Requirements</span></span>



| <span data-ttu-id="ca771-108">Роль</span><span class="sxs-lookup"><span data-stu-id="ca771-108">Role</span></span> | <span data-ttu-id="ca771-109">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="ca771-109">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ca771-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="ca771-110">Client</span></span><br/> | <span data-ttu-id="ca771-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca771-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ca771-112">Сервер</span><span class="sxs-lookup"><span data-stu-id="ca771-112">Server</span></span><br/> | <span data-ttu-id="ca771-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca771-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca771-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca771-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca771-115">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="ca771-115">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ca771-116">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ca771-116">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ca771-117">Простые типы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ca771-117">eaptlsconnectionpropertiesv1 Schema Simple Types</span></span>](eaptlsconnectionpropertiesv1schema-simple-types.md)
</dt> </dl>

 

 





