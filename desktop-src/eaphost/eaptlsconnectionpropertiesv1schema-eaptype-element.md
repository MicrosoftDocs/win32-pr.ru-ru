---
title: Элемент Еаптипе (eaptlsconnectionpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы Басиапконнектионпропертиес. Для eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188005"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="1de13-105">Элемент Еаптипе (eaptlsconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="1de13-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="1de13-106">Элемент **еаптипе** является производным типом элемента [**Еаптипе**](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [басиапконнектионпропертиес](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1de13-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="1de13-107">Этот производный элемент **еаптипе** содержит следующие элементы: [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**перформсервервалидатион**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)и [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span><span class="sxs-lookup"><span data-stu-id="1de13-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="1de13-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1de13-108">Child elements</span></span>



| <span data-ttu-id="1de13-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1de13-109">Element</span></span>                                                                                                                               | <span data-ttu-id="1de13-110">Тип</span><span class="sxs-lookup"><span data-stu-id="1de13-110">Type</span></span>                                                                                                              | <span data-ttu-id="1de13-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1de13-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1de13-112">**Екстендедтлс: Перформсервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="1de13-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="1de13-113">Windows 7 и более поздние версии: указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="1de13-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="1de13-114">**Екстендедтлс: Акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="1de13-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="1de13-115">Windows 7 и более поздние версии: указывает, считывается ли имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1de13-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1de13-116">**Екстендедтлс: Тлсекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="1de13-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="1de13-117">Windows 7 и более поздние версии: включает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="1de13-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1de13-118">**кредентиалссаурце**</span><span class="sxs-lookup"><span data-stu-id="1de13-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="1de13-119">**кредентиалссаурцепараметерс**</span><span class="sxs-lookup"><span data-stu-id="1de13-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="1de13-120">Содержит сведения о расположении сертификата безопасности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="1de13-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="1de13-121">Элемент [**кредентиалссаурце**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1de13-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1de13-122">**дифферентусернаме**</span><span class="sxs-lookup"><span data-stu-id="1de13-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="1de13-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="1de13-123">boolean</span></span>                                                                                                           | <span data-ttu-id="1de13-124">Определяет, какое имя пользователя использует EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="1de13-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="1de13-125">Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение true**, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате.</span><span class="sxs-lookup"><span data-stu-id="1de13-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="1de13-126">Если элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) имеет **значение false**, то EAP-TLS использует имя пользователя, которое отображается в сертификате.</span><span class="sxs-lookup"><span data-stu-id="1de13-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="1de13-127">Элемент [**дифферентусернаме**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1de13-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="1de13-128">**сервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="1de13-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="1de13-129">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="1de13-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="1de13-130">Содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="1de13-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="1de13-131">Элемент [**сервервалидатион**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1de13-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="1de13-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1de13-132">Requirements</span></span>



| <span data-ttu-id="1de13-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1de13-133">Requirement</span></span> | <span data-ttu-id="1de13-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1de13-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1de13-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1de13-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1de13-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1de13-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1de13-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1de13-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1de13-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1de13-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1de13-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1de13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de13-140">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="1de13-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1de13-141">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1de13-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1de13-142">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1de13-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





