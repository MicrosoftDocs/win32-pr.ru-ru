---
title: Мессажетабле (Метадататипе), элемент
description: Содержит ссылки на строки, используемые в разделе метаданных манифеста для инструментария событий. Строки хранятся в группе элементов сообщений и идентификаторов вместе.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- Журнал событий элемента Мессажетабле
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135315"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="7a9e5-105">Мессажетабле (Метадататипе), элемент</span><span class="sxs-lookup"><span data-stu-id="7a9e5-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="7a9e5-106">Содержит ссылки на строки, используемые в разделе метаданных манифеста для инструментария событий.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="7a9e5-107">Строки хранятся в группе элементов [**сообщений**](eventmanifestschema-message-messagetable-element.md) и идентификаторов вместе.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7a9e5-108">Элемент **мессажетабле** определяется сложным типом [**метадататипе**](eventmanifestschema-metadatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7a9e5-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7a9e5-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7a9e5-109">Child elements</span></span>



| <span data-ttu-id="7a9e5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="7a9e5-110">Element</span></span>                                                             | <span data-ttu-id="7a9e5-111">Тип</span><span class="sxs-lookup"><span data-stu-id="7a9e5-111">Type</span></span> | <span data-ttu-id="7a9e5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7a9e5-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a9e5-113">**message**</span><span class="sxs-lookup"><span data-stu-id="7a9e5-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="7a9e5-114">Задает ссылку на строку в разделе локализации манифеста.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="7a9e5-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7a9e5-115">Attributes</span></span>



| <span data-ttu-id="7a9e5-116">Имя</span><span class="sxs-lookup"><span data-stu-id="7a9e5-116">Name</span></span>    | <span data-ttu-id="7a9e5-117">Тип</span><span class="sxs-lookup"><span data-stu-id="7a9e5-117">Type</span></span>   | <span data-ttu-id="7a9e5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7a9e5-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="7a9e5-119">message</span><span class="sxs-lookup"><span data-stu-id="7a9e5-119">message</span></span> | <span data-ttu-id="7a9e5-120">строка</span><span class="sxs-lookup"><span data-stu-id="7a9e5-120">string</span></span> | <span data-ttu-id="7a9e5-121">Ссылка на локализованную строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="7a9e5-122">mid</span><span class="sxs-lookup"><span data-stu-id="7a9e5-122">mid</span></span>     | <span data-ttu-id="7a9e5-123">строка</span><span class="sxs-lookup"><span data-stu-id="7a9e5-123">string</span></span> | <span data-ttu-id="7a9e5-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="7a9e5-125">символ</span><span class="sxs-lookup"><span data-stu-id="7a9e5-125">symbol</span></span>  | <span data-ttu-id="7a9e5-126">строка</span><span class="sxs-lookup"><span data-stu-id="7a9e5-126">string</span></span> | <span data-ttu-id="7a9e5-127">Символ, используемый для ссылки на сообщение.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="7a9e5-128">value</span><span class="sxs-lookup"><span data-stu-id="7a9e5-128">value</span></span>   | <span data-ttu-id="7a9e5-129">строка</span><span class="sxs-lookup"><span data-stu-id="7a9e5-129">string</span></span> | <span data-ttu-id="7a9e5-130">Число, используемое в качестве идентификатора сообщения для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="7a9e5-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7a9e5-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7a9e5-131">Requirements</span></span>



| <span data-ttu-id="7a9e5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7a9e5-132">Requirement</span></span> | <span data-ttu-id="7a9e5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7a9e5-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a9e5-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a9e5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7a9e5-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a9e5-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a9e5-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a9e5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7a9e5-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a9e5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a9e5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a9e5-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a9e5-139">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="7a9e5-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7a9e5-140">**метадататипе**</span><span class="sxs-lookup"><span data-stu-id="7a9e5-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="7a9e5-141">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="7a9e5-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7a9e5-142">**метаданные (Инструментатионманифест)**</span><span class="sxs-lookup"><span data-stu-id="7a9e5-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





