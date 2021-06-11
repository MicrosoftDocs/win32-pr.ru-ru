---
title: Элемент Идентитиприваци (Пеапекстенсионстипе) (v1)
description: Элемент Идентитиприваци (Пеапекстенсионстипе) указывает, отправляется ли в схеме mspeapconnectionpropertiesv1 истинное удостоверение пользователя.
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
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989219"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="e8e28-104">Идентитиприваци (Пеапекстенсионстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="e8e28-104">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="e8e28-105">Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="e8e28-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="e8e28-106">Элемент определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e8e28-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e28-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="e8e28-107">Remarks</span></span>

<span data-ttu-id="e8e28-108">Элемент **идентитиприваци** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e8e28-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e28-109">Требования</span><span class="sxs-lookup"><span data-stu-id="e8e28-109">Requirements</span></span>



| <span data-ttu-id="e8e28-110">Требование</span><span class="sxs-lookup"><span data-stu-id="e8e28-110">Requirement</span></span> | <span data-ttu-id="e8e28-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e28-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e8e28-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8e28-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e28-113">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8e28-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e8e28-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8e28-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e28-115">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8e28-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8e28-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8e28-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8e28-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="e8e28-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e8e28-118">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="e8e28-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="e8e28-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="e8e28-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e8e28-120">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="e8e28-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="e8e28-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e8e28-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e8e28-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="e8e28-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e8e28-123">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e8e28-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e8e28-124">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e8e28-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e8e28-125">**Идентитиприваци (Пеапекстенсионстипе)**</span><span class="sxs-lookup"><span data-stu-id="e8e28-125">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





