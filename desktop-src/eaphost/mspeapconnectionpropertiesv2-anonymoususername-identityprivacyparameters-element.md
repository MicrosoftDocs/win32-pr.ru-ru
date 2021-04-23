---
title: Анонимаусусернаме (Идентитиприваципараметерс), элемент
description: Содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя. Он отправляется во время первого этапа проверки подлинности PEAP, когда удостоверение отправляется в виде обычного текста.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Элемент Анонимаусусернаме EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415820"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="2140b-105">Анонимаусусернаме (Идентитиприваципараметерс), элемент</span><span class="sxs-lookup"><span data-stu-id="2140b-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="2140b-106">Элемент **анонимаусусернаме (идентитиприваципараметерс)** содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя.</span><span class="sxs-lookup"><span data-stu-id="2140b-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="2140b-107">Он отправляется во время первого этапа проверки подлинности PEAP, когда **удостоверение** отправляется в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="2140b-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="2140b-108">Использование анонимных удостоверений определяется элементом [**енаблеидентитиприваци**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2140b-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="2140b-109">Элемент **анонимаусусернаме** определяется параметром [идентитиприваципараметерс](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2140b-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="2140b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2140b-110">Remarks</span></span>

<span data-ttu-id="2140b-111">Элемент **анонимаусусернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2140b-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2140b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2140b-112">Requirements</span></span>



| <span data-ttu-id="2140b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2140b-113">Requirement</span></span> | <span data-ttu-id="2140b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2140b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2140b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2140b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2140b-116">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2140b-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2140b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2140b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2140b-118">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2140b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2140b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2140b-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="2140b-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="2140b-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2140b-121">идентитиприваципараметерс</span><span class="sxs-lookup"><span data-stu-id="2140b-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="2140b-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="2140b-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2140b-123">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="2140b-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="2140b-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2140b-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2140b-125">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="2140b-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2140b-126">Элементы схемы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="2140b-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





