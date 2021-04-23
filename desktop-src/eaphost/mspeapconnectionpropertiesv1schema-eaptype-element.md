---
title: Элемент Еаптипе (mspeapconnectionpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы Басиапконнектионпропертиес. Для mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187753"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="78e79-105">Элемент Еаптипе (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="78e79-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="78e79-106">Элемент **еаптипе** является производным типом элемента [**Еаптипе**](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [басиапконнектионпропертиес](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="78e79-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="78e79-107">Этот производный элемент **еаптипе** содержит следующие элементы: [**сервервалидатион**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**идентитиприваци**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) и [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="78e79-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="78e79-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="78e79-108">Child elements</span></span>



| <span data-ttu-id="78e79-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="78e79-109">Element</span></span>                                                                                                     | <span data-ttu-id="78e79-110">Тип</span><span class="sxs-lookup"><span data-stu-id="78e79-110">Type</span></span>                                                                                                            | <span data-ttu-id="78e79-111">Описание</span><span class="sxs-lookup"><span data-stu-id="78e79-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78e79-112">**Протокола**</span><span class="sxs-lookup"><span data-stu-id="78e79-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="78e79-113">Описывает внутренний метод и конфигурацию метода.</span><span class="sxs-lookup"><span data-stu-id="78e79-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="78e79-114">Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение true, должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) .</span><span class="sxs-lookup"><span data-stu-id="78e79-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="78e79-115">Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение false, то элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) должен отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="78e79-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="78e79-116">**енаблекуарантинечеккс**</span><span class="sxs-lookup"><span data-stu-id="78e79-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="78e79-117">Логическое</span><span class="sxs-lookup"><span data-stu-id="78e79-117">boolean</span></span>                                                                                                         | <span data-ttu-id="78e79-118">Указывает, следует ли выполнять проверки защиты доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="78e79-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="78e79-119">Если элемент [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) имеет значение true, PEAP ВЫПОЛНЯЕТ проверки NAP; Если значение FALSE PEAP не будет выполнять проверки защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="78e79-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="78e79-120">Элемент [**енаблекуарантинечеккс**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="78e79-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="78e79-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="78e79-122">Логическое</span><span class="sxs-lookup"><span data-stu-id="78e79-122">boolean</span></span>                                                                                                         | <span data-ttu-id="78e79-123">Указывает, следует ли выполнять быстрое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="78e79-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="78e79-124">Если элемент [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) имеет значение true, то PEAP пытается выполнить быстрое повторное подключение. Если значение равно FALSE, PEAP выполняет полную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="78e79-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="78e79-125">Элемент [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="78e79-126">**идентитиприваци**</span><span class="sxs-lookup"><span data-stu-id="78e79-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="78e79-127">**идентитиприваципараметерс**</span><span class="sxs-lookup"><span data-stu-id="78e79-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="78e79-128">Windows 7 или более поздней версии: указывает, отправляется ли истинное удостоверение пользователя или анонимное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="78e79-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="78e79-129">Элемент [**идентитиприваци**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="78e79-130">**иннереапоптионал**</span><span class="sxs-lookup"><span data-stu-id="78e79-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="78e79-131">Логическое</span><span class="sxs-lookup"><span data-stu-id="78e79-131">boolean</span></span>                                                                                                         | <span data-ttu-id="78e79-132">Указывает, следует ли выполнять гостевой доступ.</span><span class="sxs-lookup"><span data-stu-id="78e79-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="78e79-133">Если элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) имеет значение true, то должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) , описывающий внутренний метод и его конфигурацию. Если задано значение FALSE, PEAP выполняет гостевой доступ.</span><span class="sxs-lookup"><span data-stu-id="78e79-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="78e79-134">Элемент [**иннереапоптионал**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="78e79-135">**пеапекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="78e79-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="78e79-136">**пеапекстенсионстипе**</span><span class="sxs-lookup"><span data-stu-id="78e79-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="78e79-137">Элемент [**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="78e79-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="78e79-138">Элемент [**пеапекстенсионс**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="78e79-139">**рекуирекриптобиндинг**</span><span class="sxs-lookup"><span data-stu-id="78e79-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="78e79-140">Логическое</span><span class="sxs-lookup"><span data-stu-id="78e79-140">boolean</span></span>                                                                                                         | <span data-ttu-id="78e79-141">Указывает, следует ли выполнять проверку подлинности на серверах, поддерживающих криптобиндинг.</span><span class="sxs-lookup"><span data-stu-id="78e79-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="78e79-142">Если элемент [**рекуирекриптобиндинг**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) имеет значение true, PEAP будет проходить проверку подлинности на серверах, не поддерживающих криптобиндинг. Если значение равно FALSE, PEAP будет проходить проверку подлинности только на серверах, поддерживающих криптобиндинг.</span><span class="sxs-lookup"><span data-stu-id="78e79-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="78e79-143">Элемент [**рекуирекриптобиндинг**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="78e79-144">**сервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="78e79-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="78e79-145">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="78e79-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="78e79-146">Содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="78e79-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="78e79-147">Элемент [**сервервалидатион**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78e79-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="78e79-148">Требования</span><span class="sxs-lookup"><span data-stu-id="78e79-148">Requirements</span></span>



| <span data-ttu-id="78e79-149">Требование</span><span class="sxs-lookup"><span data-stu-id="78e79-149">Requirement</span></span> | <span data-ttu-id="78e79-150">Значение</span><span class="sxs-lookup"><span data-stu-id="78e79-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78e79-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78e79-151">Minimum supported client</span></span><br/> | <span data-ttu-id="78e79-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78e79-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78e79-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78e79-153">Minimum supported server</span></span><br/> | <span data-ttu-id="78e79-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78e79-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78e79-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78e79-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e79-156">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="78e79-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="78e79-157">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="78e79-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="78e79-158">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="78e79-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





