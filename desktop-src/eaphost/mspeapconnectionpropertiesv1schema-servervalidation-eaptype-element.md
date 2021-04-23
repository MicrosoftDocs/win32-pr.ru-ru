---
title: Элемент Сервервалидатион (Еаптипе) (PEAP)
description: Сведения об элементе Сервервалидатион (Еаптипе). Этот элемент содержит сведения о выполнении проверки сервера. | Элемент Сервервалидатион (Еаптипе) (PEAP)
ms.assetid: 5b213853-7161-456c-bbba-d3b1118f1786
keywords:
- Элемент Сервервалидатион EAPHost
topic_type:
- apiref
api_name:
- ServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1495da3f1a1f5e69e7a6af9c64e69aa1ea354abc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713369"
---
# <a name="servervalidation-eaptype-element-peap"></a><span data-ttu-id="5fec3-106">Элемент Сервервалидатион (Еаптипе) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="5fec3-106">ServerValidation (EapType) element (PEAP)</span></span>

<span data-ttu-id="5fec3-107">Элемент **сервервалидатион (еаптипе)** содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="5fec3-107">The **ServerValidation (EapType)** element contains information about how to perform server validation.</span></span>

``` syntax
<xs:element name="ServerValidation"
    type="ServerValidationParameters"
 />
```

<span data-ttu-id="5fec3-108">Элемент **сервервалидатион** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5fec3-108">The **ServerValidation** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fec3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fec3-109">Remarks</span></span>

<span data-ttu-id="5fec3-110">Элемент **сервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5fec3-110">The **ServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fec3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5fec3-111">Requirements</span></span>



| <span data-ttu-id="5fec3-112">Роль</span><span class="sxs-lookup"><span data-stu-id="5fec3-112">Role</span></span> | <span data-ttu-id="5fec3-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="5fec3-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="5fec3-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="5fec3-114">Client</span></span><br/> | <span data-ttu-id="5fec3-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fec3-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fec3-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="5fec3-116">Server</span></span><br/> | <span data-ttu-id="5fec3-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fec3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fec3-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fec3-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fec3-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="5fec3-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5fec3-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="5fec3-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="5fec3-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="5fec3-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5fec3-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="5fec3-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="5fec3-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="5fec3-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5fec3-124">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5fec3-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5fec3-125">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5fec3-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





