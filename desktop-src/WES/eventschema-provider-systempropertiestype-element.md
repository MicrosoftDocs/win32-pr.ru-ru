---
title: Элемент Provider (Системпропертиестипе)
description: Определяет поставщика, который зарегистрировал событие.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Журнал событий элемента поставщика
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071277"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="acc8a-104">Элемент Provider (Системпропертиестипе)</span><span class="sxs-lookup"><span data-stu-id="acc8a-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="acc8a-105">Определяет поставщика, который зарегистрировал событие.</span><span class="sxs-lookup"><span data-stu-id="acc8a-105">Identifies the provider that logged the event.</span></span>

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="acc8a-106">Элемент **provider** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="acc8a-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="acc8a-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="acc8a-107">Attributes</span></span>



| <span data-ttu-id="acc8a-108">Имя</span><span class="sxs-lookup"><span data-stu-id="acc8a-108">Name</span></span>            | <span data-ttu-id="acc8a-109">Тип</span><span class="sxs-lookup"><span data-stu-id="acc8a-109">Type</span></span>                                                | <span data-ttu-id="acc8a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="acc8a-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc8a-111">евентсаурценаме</span><span class="sxs-lookup"><span data-stu-id="acc8a-111">EventSourceName</span></span> | <span data-ttu-id="acc8a-112">строка</span><span class="sxs-lookup"><span data-stu-id="acc8a-112">string</span></span>                                              | <span data-ttu-id="acc8a-113">Имя источника события, опубликовавшего событие (если источником события является устаревший API [протоколирования событий](/windows/desktop/EventLog/event-logging) ).</span><span class="sxs-lookup"><span data-stu-id="acc8a-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="acc8a-114">Guid</span><span class="sxs-lookup"><span data-stu-id="acc8a-114">Guid</span></span>            | [<span data-ttu-id="acc8a-115">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="acc8a-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="acc8a-116">Глобальный уникальный идентификатор, который однозначно идентифицирует поставщик.</span><span class="sxs-lookup"><span data-stu-id="acc8a-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="acc8a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="acc8a-117">Name</span></span>            | <span data-ttu-id="acc8a-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="acc8a-118">anyURI</span></span>                                              | <span data-ttu-id="acc8a-119">Имя поставщика событий, который зарегистрировал событие.</span><span class="sxs-lookup"><span data-stu-id="acc8a-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="acc8a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="acc8a-120">Requirements</span></span>



| <span data-ttu-id="acc8a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="acc8a-121">Requirement</span></span> | <span data-ttu-id="acc8a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="acc8a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="acc8a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acc8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="acc8a-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acc8a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="acc8a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acc8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="acc8a-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="acc8a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="acc8a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acc8a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="acc8a-128">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="acc8a-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="acc8a-129">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="acc8a-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

