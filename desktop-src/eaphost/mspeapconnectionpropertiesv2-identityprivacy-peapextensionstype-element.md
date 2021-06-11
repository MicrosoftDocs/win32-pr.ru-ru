---
title: Идентитиприваци (Пеапекстенсионстипе), элемент
description: Элемент Идентитиприваци (Пеапекстенсионстипе) указывает, отправляется ли в схеме mspeapconnectionpropertiesv2 истинное удостоверение пользователя.
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
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988950"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="2ff84-104">Элемент Идентитиприваци (Пеапекстенсионстипе)</span><span class="sxs-lookup"><span data-stu-id="2ff84-104">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="2ff84-105">Элемент **идентитиприваци (пеапекстенсионстипе)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="2ff84-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="2ff84-106">Элемент **идентитиприваци** определяется элементом [**пеапекстенсионстипе**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff84-106">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff84-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ff84-107">Remarks</span></span>

<span data-ttu-id="2ff84-108">Элемент **идентитиприваци** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2ff84-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff84-109">Требования</span><span class="sxs-lookup"><span data-stu-id="2ff84-109">Requirements</span></span>



| <span data-ttu-id="2ff84-110">Требование</span><span class="sxs-lookup"><span data-stu-id="2ff84-110">Requirement</span></span> | <span data-ttu-id="2ff84-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2ff84-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2ff84-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ff84-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff84-113">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2ff84-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2ff84-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ff84-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff84-115">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ff84-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ff84-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ff84-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ff84-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="2ff84-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2ff84-118">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="2ff84-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="2ff84-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="2ff84-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2ff84-120">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="2ff84-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="2ff84-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2ff84-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2ff84-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2ff84-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2ff84-123">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="2ff84-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2ff84-124">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="2ff84-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





