---
title: Еафостконфиг, элемент
description: Содержит элемент Еапмесод и элемент конфигурации или Конфигблоб. Элементы config и Конфигблоб не могут одновременно использоваться одновременно.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Элемент Еафостконфиг EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071046"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="2e704-105">Еафостконфиг, элемент</span><span class="sxs-lookup"><span data-stu-id="2e704-105">EapHostConfig Element</span></span>

<span data-ttu-id="2e704-106">Элемент **еафостконфиг** содержит элемент [**Еапмесод**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) и элемент [**config**](eaphostconfigschema-config-eaphostconfig-element.md) или [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2e704-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="2e704-107">Элементы [**config**](eaphostconfigschema-config-eaphostconfig-element.md) и [**конфигблоб**](eaphostconfigschema-configblob-eaphostconfig-element.md) не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="2e704-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
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

## <a name="child-elements"></a><span data-ttu-id="2e704-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2e704-108">Child elements</span></span>



| <span data-ttu-id="2e704-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="2e704-109">Element</span></span>                                                                    | <span data-ttu-id="2e704-110">Тип</span><span class="sxs-lookup"><span data-stu-id="2e704-110">Type</span></span>                                                                                     | <span data-ttu-id="2e704-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2e704-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e704-112">**Config**</span><span class="sxs-lookup"><span data-stu-id="2e704-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="2e704-113">**басиапмесодконфиг**</span><span class="sxs-lookup"><span data-stu-id="2e704-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="2e704-114">Используется, когда конфигурация метода находится в текстовом формате XML вместо двоичного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="2e704-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="2e704-115">**конфигблоб**</span><span class="sxs-lookup"><span data-stu-id="2e704-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="2e704-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="2e704-116">hexBinary</span></span>                                                                                | <span data-ttu-id="2e704-117">Используется, когда конфигурация метода находится в двоичном виде двоичного объекта, а не в виде строки текста.</span><span class="sxs-lookup"><span data-stu-id="2e704-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="2e704-118">**еапмесод**</span><span class="sxs-lookup"><span data-stu-id="2e704-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="2e704-119">**еапмесодтипе**</span><span class="sxs-lookup"><span data-stu-id="2e704-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="2e704-120">Определяет метод, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="2e704-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="2e704-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e704-121">Remarks</span></span>

<span data-ttu-id="2e704-122">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="2e704-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="2e704-123">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2e704-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e704-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2e704-124">Requirements</span></span>



| <span data-ttu-id="2e704-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2e704-125">Requirement</span></span> | <span data-ttu-id="2e704-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2e704-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e704-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e704-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e704-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e704-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e704-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e704-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e704-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e704-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e704-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e704-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e704-132">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2e704-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2e704-133">Схема еафостконфиг</span><span class="sxs-lookup"><span data-stu-id="2e704-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





