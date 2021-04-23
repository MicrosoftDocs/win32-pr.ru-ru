---
title: Сложный тип Пеапекстенсионстипе
description: Содержит улучшения схемы, вносимые в Windows 7. Будущие улучшения схемы будут обрабатываться PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
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
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803281"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="4bc3d-105">Сложный тип Пеапекстенсионстипе</span><span class="sxs-lookup"><span data-stu-id="4bc3d-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="4bc3d-106">Сложный тип **пеапекстенсионстипе** содержит улучшения схемы, вносимые в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="4bc3d-107">Будущие улучшения схемы будут обрабатываться [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="4bc3d-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4bc3d-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4bc3d-108">Child elements</span></span>



| <span data-ttu-id="4bc3d-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="4bc3d-109">Element</span></span>                                                                                                                               | <span data-ttu-id="4bc3d-110">Тип</span><span class="sxs-lookup"><span data-stu-id="4bc3d-110">Type</span></span> | <span data-ttu-id="4bc3d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4bc3d-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bc3d-112">**Екстендедпеап: Перформсервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="4bc3d-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="4bc3d-113">Windows 7 и более поздние версии: указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="4bc3d-114">**Екстендедпеап: Акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="4bc3d-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="4bc3d-115">Windows 7 и более поздние версии: указывает, считывается ли имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="4bc3d-116">**Екстендедпеап: Идентитиприваци**</span><span class="sxs-lookup"><span data-stu-id="4bc3d-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="4bc3d-117">Windows 7 и более поздние версии: указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="4bc3d-118">**Екстендедпеап: PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="4bc3d-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="4bc3d-119">Windows 7 и более поздние версии: включает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="4bc3d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bc3d-120">Remarks</span></span>

<span data-ttu-id="4bc3d-121">Элемент **пеапекстенсионстипе** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4bc3d-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc3d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4bc3d-122">Requirements</span></span>



| <span data-ttu-id="4bc3d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4bc3d-123">Requirement</span></span> | <span data-ttu-id="4bc3d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4bc3d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4bc3d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bc3d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc3d-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4bc3d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4bc3d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bc3d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc3d-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bc3d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bc3d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bc3d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc3d-130">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4bc3d-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4bc3d-131">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4bc3d-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4bc3d-132">Сложные типы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4bc3d-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





