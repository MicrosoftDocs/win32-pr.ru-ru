---
title: Идентитиприваци (Пеапекстенсионстипе), элемент
description: Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение. | Идентитиприваци (Пеапекстенсионстипе), элемент
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Элемент Идентитиприваци EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547551"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="a5ed6-105">Элемент Идентитиприваци (Пеапекстенсионстипе)</span><span class="sxs-lookup"><span data-stu-id="a5ed6-105">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="a5ed6-106">Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="a5ed6-107">Элемент **идентитиприваци** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ed6-107">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ed6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ed6-108">Remarks</span></span>

<span data-ttu-id="a5ed6-109">Элемент **идентитиприваци** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5ed6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a5ed6-110">Requirements</span></span>



| <span data-ttu-id="a5ed6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a5ed6-111">Requirement</span></span> | <span data-ttu-id="a5ed6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a5ed6-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a5ed6-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5ed6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ed6-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5ed6-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a5ed6-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5ed6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ed6-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5ed6-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5ed6-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5ed6-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5ed6-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a5ed6-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a5ed6-119">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="a5ed6-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="a5ed6-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a5ed6-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a5ed6-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="a5ed6-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="a5ed6-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a5ed6-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="a5ed6-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="a5ed6-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a5ed6-124">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a5ed6-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a5ed6-125">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a5ed6-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





