---
title: Мессажетабле (Евентстипе), элемент
description: Содержит ссылку на строку в разделе локализации манифеста. | Мессажетабле (Евентстипе), элемент
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
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
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693960"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="5588b-105">Мессажетабле (Евентстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="5588b-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="5588b-106">Содержит ссылку на строку в разделе локализации манифеста.</span><span class="sxs-lookup"><span data-stu-id="5588b-106">Contains a reference to a string in the localization section of the manifest.</span></span>

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

<span data-ttu-id="5588b-107">Элемент **мессажетабле** определяется сложным типом [**евентстипе**](eventmanifestschema-eventstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5588b-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5588b-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5588b-108">Child elements</span></span>



| <span data-ttu-id="5588b-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="5588b-109">Element</span></span>                                                             | <span data-ttu-id="5588b-110">Тип</span><span class="sxs-lookup"><span data-stu-id="5588b-110">Type</span></span> | <span data-ttu-id="5588b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5588b-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5588b-112">**message**</span><span class="sxs-lookup"><span data-stu-id="5588b-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="5588b-113">Задает ссылку на строку в разделе локализации манифеста.</span><span class="sxs-lookup"><span data-stu-id="5588b-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="5588b-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5588b-114">Attributes</span></span>



| <span data-ttu-id="5588b-115">Имя</span><span class="sxs-lookup"><span data-stu-id="5588b-115">Name</span></span>    | <span data-ttu-id="5588b-116">Тип</span><span class="sxs-lookup"><span data-stu-id="5588b-116">Type</span></span>   | <span data-ttu-id="5588b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5588b-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5588b-118">message</span><span class="sxs-lookup"><span data-stu-id="5588b-118">message</span></span> | <span data-ttu-id="5588b-119">строка</span><span class="sxs-lookup"><span data-stu-id="5588b-119">string</span></span> | <span data-ttu-id="5588b-120">Ссылка на локализованную строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="5588b-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="5588b-121">mid</span><span class="sxs-lookup"><span data-stu-id="5588b-121">mid</span></span>     | <span data-ttu-id="5588b-122">строка</span><span class="sxs-lookup"><span data-stu-id="5588b-122">string</span></span> | <span data-ttu-id="5588b-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5588b-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="5588b-124">символ</span><span class="sxs-lookup"><span data-stu-id="5588b-124">symbol</span></span>  | <span data-ttu-id="5588b-125">строка</span><span class="sxs-lookup"><span data-stu-id="5588b-125">string</span></span> | <span data-ttu-id="5588b-126">Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="5588b-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="5588b-127">value</span><span class="sxs-lookup"><span data-stu-id="5588b-127">value</span></span>   | <span data-ttu-id="5588b-128">строка</span><span class="sxs-lookup"><span data-stu-id="5588b-128">string</span></span> | <span data-ttu-id="5588b-129">Число, используемое в качестве идентификатора сообщения для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="5588b-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="5588b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5588b-130">Requirements</span></span>



| <span data-ttu-id="5588b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5588b-131">Requirement</span></span> | <span data-ttu-id="5588b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5588b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5588b-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5588b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5588b-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5588b-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5588b-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5588b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5588b-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5588b-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5588b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5588b-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="5588b-138">**Родительские элементы**</span><span class="sxs-lookup"><span data-stu-id="5588b-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="5588b-139">**Элемент Events (Инструментатионтипе)**</span><span class="sxs-lookup"><span data-stu-id="5588b-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





