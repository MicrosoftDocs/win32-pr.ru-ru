---
title: Еафостусеркредентиалс, элемент
description: Содержит элемент Еапмесод, а также учетные данные или элемент Кредентиалсблоб.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Элемент Еафостусеркредентиалс EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136694"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="3cb60-104">Еафостусеркредентиалс, элемент</span><span class="sxs-lookup"><span data-stu-id="3cb60-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="3cb60-105">Элемент **еафостусеркредентиалс** содержит элемент [**еапмесод**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) , а также [**учетные данные**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) или элемент [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb60-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="3cb60-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3cb60-106">Child elements</span></span>



| <span data-ttu-id="3cb60-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3cb60-107">Element</span></span>                                                                                                | <span data-ttu-id="3cb60-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3cb60-108">Type</span></span>                                                                                                                | <span data-ttu-id="3cb60-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3cb60-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cb60-110">**Учетные данные**</span><span class="sxs-lookup"><span data-stu-id="3cb60-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="3cb60-111">**басиапмесодусеркредентиалс**</span><span class="sxs-lookup"><span data-stu-id="3cb60-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="3cb60-112">Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="3cb60-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="3cb60-113">**кредентиалсблоб**</span><span class="sxs-lookup"><span data-stu-id="3cb60-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="3cb60-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="3cb60-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="3cb60-115">Используется, когда конфигурация метода является двоичным BLOB-объектом, а не в текстовом формате XML.</span><span class="sxs-lookup"><span data-stu-id="3cb60-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="3cb60-116">**еапмесод**</span><span class="sxs-lookup"><span data-stu-id="3cb60-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="3cb60-117">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="3cb60-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="3cb60-118">Определяет метод, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="3cb60-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="3cb60-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cb60-119">Remarks</span></span>

<span data-ttu-id="3cb60-120">Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и [**кредентиалсблоб**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) нельзя одновременно использовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="3cb60-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="3cb60-121">Существует точка расширения для других пространств имен.</span><span class="sxs-lookup"><span data-stu-id="3cb60-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="3cb60-122">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="3cb60-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="3cb60-123">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3cb60-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb60-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb60-124">Requirements</span></span>



| <span data-ttu-id="3cb60-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb60-125">Requirement</span></span> | <span data-ttu-id="3cb60-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb60-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3cb60-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cb60-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb60-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cb60-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3cb60-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cb60-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb60-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3cb60-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cb60-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cb60-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb60-132">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3cb60-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3cb60-133">Схема еафостусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="3cb60-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





