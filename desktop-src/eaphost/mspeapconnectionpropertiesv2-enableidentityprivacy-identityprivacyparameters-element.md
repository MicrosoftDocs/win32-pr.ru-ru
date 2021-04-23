---
title: Енаблеидентитиприваци (Идентитиприваципараметерс), элемент
description: Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение. | Енаблеидентитиприваци (Идентитиприваципараметерс), элемент
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Элемент Енаблеидентитиприваци EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353772"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="f522a-105">Енаблеидентитиприваци (Идентитиприваципараметерс), элемент</span><span class="sxs-lookup"><span data-stu-id="f522a-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="f522a-106">Элемент **енаблеидентитиприваци (идентитиприваципараметерс)** указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="f522a-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="f522a-107">Элемент **енаблеидентитиприваци** определяется параметром [идентитиприваципараметерс](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f522a-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="f522a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f522a-108">Remarks</span></span>

<span data-ttu-id="f522a-109">Элемент **енаблеидентитиприваци** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f522a-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f522a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f522a-110">Requirements</span></span>



| <span data-ttu-id="f522a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f522a-111">Requirement</span></span> | <span data-ttu-id="f522a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f522a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f522a-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f522a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f522a-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f522a-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f522a-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f522a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f522a-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f522a-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f522a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f522a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f522a-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="f522a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f522a-119">идентитиприваципараметерс</span><span class="sxs-lookup"><span data-stu-id="f522a-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="f522a-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="f522a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f522a-121">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="f522a-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f522a-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f522a-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f522a-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="f522a-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f522a-124">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f522a-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f522a-125">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f522a-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





