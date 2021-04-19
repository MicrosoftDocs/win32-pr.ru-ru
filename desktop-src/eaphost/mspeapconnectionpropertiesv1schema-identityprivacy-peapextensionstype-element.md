---
title: Элемент Идентитиприваци (Пеапекстенсионстипе) (v1)
description: Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение. | Идентитиприваци (Пеапекстенсионстипе), элемент
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 748cf3ae8d5a4da4f8885332a72326bced45b398
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389075"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="c9caa-105">Идентитиприваци (Пеапекстенсионстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c9caa-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="c9caa-106">Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="c9caa-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="c9caa-107">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9caa-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9caa-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="c9caa-108">Remarks</span></span>

<span data-ttu-id="c9caa-109">Элемент **идентитиприваци** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c9caa-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9caa-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c9caa-110">Requirements</span></span>



| <span data-ttu-id="c9caa-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c9caa-111">Requirement</span></span> | <span data-ttu-id="c9caa-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c9caa-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c9caa-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9caa-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c9caa-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9caa-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c9caa-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9caa-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c9caa-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9caa-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9caa-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c9caa-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9caa-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="c9caa-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c9caa-119">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="c9caa-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="c9caa-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="c9caa-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c9caa-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="c9caa-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="c9caa-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c9caa-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c9caa-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="c9caa-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c9caa-124">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c9caa-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c9caa-125">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c9caa-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c9caa-126">**Идентитиприваци (Пеапекстенсионстипе)**</span><span class="sxs-lookup"><span data-stu-id="c9caa-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





