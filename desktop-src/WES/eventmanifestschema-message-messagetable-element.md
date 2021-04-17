---
title: Элемент Message (Мессажетабле)
description: Содержит ссылку на строку в разделе локализации манифеста. | Элемент Message (Мессажетабле)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Журнал событий элемента сообщения
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693961"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="f8f11-105">Элемент Message (Мессажетабле)</span><span class="sxs-lookup"><span data-stu-id="f8f11-105">message (messageTable) Element</span></span>

<span data-ttu-id="f8f11-106">Содержит ссылку на строку в разделе локализации манифеста.</span><span class="sxs-lookup"><span data-stu-id="f8f11-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
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
```

<span data-ttu-id="f8f11-107">Элемент **Message** определяется элементом [**мессажетабле**](eventmanifestschema-messagetable-instrumentationtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f11-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="f8f11-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8f11-108">Attributes</span></span>



| <span data-ttu-id="f8f11-109">Имя</span><span class="sxs-lookup"><span data-stu-id="f8f11-109">Name</span></span>    | <span data-ttu-id="f8f11-110">Тип</span><span class="sxs-lookup"><span data-stu-id="f8f11-110">Type</span></span>   | <span data-ttu-id="f8f11-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f8f11-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f11-112">message</span><span class="sxs-lookup"><span data-stu-id="f8f11-112">message</span></span> | <span data-ttu-id="f8f11-113">строка</span><span class="sxs-lookup"><span data-stu-id="f8f11-113">string</span></span> | <span data-ttu-id="f8f11-114">Ссылка на локализованную строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="f8f11-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="f8f11-115">mid</span><span class="sxs-lookup"><span data-stu-id="f8f11-115">mid</span></span>     | <span data-ttu-id="f8f11-116">строка</span><span class="sxs-lookup"><span data-stu-id="f8f11-116">string</span></span> | <span data-ttu-id="f8f11-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f8f11-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="f8f11-118">символ</span><span class="sxs-lookup"><span data-stu-id="f8f11-118">symbol</span></span>  | <span data-ttu-id="f8f11-119">строка</span><span class="sxs-lookup"><span data-stu-id="f8f11-119">string</span></span> | <span data-ttu-id="f8f11-120">Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8f11-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="f8f11-121">value</span><span class="sxs-lookup"><span data-stu-id="f8f11-121">value</span></span>   | <span data-ttu-id="f8f11-122">строка</span><span class="sxs-lookup"><span data-stu-id="f8f11-122">string</span></span> | <span data-ttu-id="f8f11-123">Число, используемое в качестве идентификатора сообщения для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8f11-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="f8f11-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f8f11-124">Requirements</span></span>



| <span data-ttu-id="f8f11-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f8f11-125">Requirement</span></span> | <span data-ttu-id="f8f11-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f8f11-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f8f11-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8f11-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f11-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8f11-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f8f11-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8f11-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f11-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8f11-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8f11-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8f11-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8f11-132">**Родительские элементы**</span><span class="sxs-lookup"><span data-stu-id="f8f11-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="f8f11-133">**Мессажетабле (Евентстипе)**</span><span class="sxs-lookup"><span data-stu-id="f8f11-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="f8f11-134">**Мессажетабле (Метадататипе)**</span><span class="sxs-lookup"><span data-stu-id="f8f11-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





