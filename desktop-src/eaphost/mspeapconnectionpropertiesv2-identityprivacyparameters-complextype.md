---
title: Сложный тип Идентитиприваципараметерс
description: Содержит сведения об использовании анонимных удостоверений во время аутентификации PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104133370"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="15a4f-103">Сложный тип Идентитиприваципараметерс</span><span class="sxs-lookup"><span data-stu-id="15a4f-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="15a4f-104">Сложный тип **идентитиприваципараметерс** содержит сведения об использовании анонимных удостоверений во время аутентификации PEAP.</span><span class="sxs-lookup"><span data-stu-id="15a4f-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="15a4f-105">Элемент</span><span class="sxs-lookup"><span data-stu-id="15a4f-105">Element</span></span>                                                                                                               | <span data-ttu-id="15a4f-106">Тип</span><span class="sxs-lookup"><span data-stu-id="15a4f-106">Type</span></span>    | <span data-ttu-id="15a4f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="15a4f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15a4f-108">**енаблеидентитиприваци**</span><span class="sxs-lookup"><span data-stu-id="15a4f-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="15a4f-109">Логическое</span><span class="sxs-lookup"><span data-stu-id="15a4f-109">boolean</span></span> | <span data-ttu-id="15a4f-110">Указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="15a4f-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="15a4f-111">**анонимаусусернаме**</span><span class="sxs-lookup"><span data-stu-id="15a4f-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="15a4f-112">строка</span><span class="sxs-lookup"><span data-stu-id="15a4f-112">string</span></span>  | <span data-ttu-id="15a4f-113">содержит анонимное удостоверение, используемое вместо истинной идентификации пользователя.</span><span class="sxs-lookup"><span data-stu-id="15a4f-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="15a4f-114">Он отправляется во время первого этапа проверки подлинности PEAP, когда **удостоверение** отправляется в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="15a4f-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="15a4f-115">Использование анонимных удостоверений определяется элементом [**енаблеидентитиприваци**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="15a4f-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="15a4f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15a4f-116">Remarks</span></span>

<span data-ttu-id="15a4f-117">Элемент Идентитиприваципараметерс является необязательным.</span><span class="sxs-lookup"><span data-stu-id="15a4f-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a4f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="15a4f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a4f-119">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="15a4f-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="15a4f-120">Схема mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="15a4f-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="15a4f-121">Сложные типы mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="15a4f-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




