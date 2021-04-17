---
title: opcode, элемент (Таскевентдефинитионтипе)
description: Содержит код операции для события, относящийся к конкретной задаче. Предполагается, что все определения кодов операций относятся к задачам, содержащим определения событий.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- Журнал событий элемента кода операции
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691934"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="0440a-105">opcode, элемент (Таскевентдефинитионтипе)</span><span class="sxs-lookup"><span data-stu-id="0440a-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="0440a-106">\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK для Windows 7, этот элемент больше не доступен.\]</span><span class="sxs-lookup"><span data-stu-id="0440a-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="0440a-107">Содержит код операции для события, относящийся к конкретной задаче.</span><span class="sxs-lookup"><span data-stu-id="0440a-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="0440a-108">Предполагается, что все определения кодов операций относятся к задачам, содержащим определения событий.</span><span class="sxs-lookup"><span data-stu-id="0440a-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0440a-109">Элемент **кода операции** определяется сложным типом [**таскевентдефинитионтипе**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0440a-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0440a-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0440a-110">Child elements</span></span>



| <span data-ttu-id="0440a-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="0440a-111">Element</span></span>                                                   | <span data-ttu-id="0440a-112">Тип</span><span class="sxs-lookup"><span data-stu-id="0440a-112">Type</span></span>                                                                               | <span data-ttu-id="0440a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0440a-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0440a-114">**журнале**</span><span class="sxs-lookup"><span data-stu-id="0440a-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="0440a-115">**евентдефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="0440a-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="0440a-116">Событие, публикуемое с задачей.</span><span class="sxs-lookup"><span data-stu-id="0440a-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0440a-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0440a-117">Attributes</span></span>



| <span data-ttu-id="0440a-118">Имя</span><span class="sxs-lookup"><span data-stu-id="0440a-118">Name</span></span> | <span data-ttu-id="0440a-119">Тип</span><span class="sxs-lookup"><span data-stu-id="0440a-119">Type</span></span>      | <span data-ttu-id="0440a-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0440a-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="0440a-121">name</span><span class="sxs-lookup"><span data-stu-id="0440a-121">name</span></span> | <span data-ttu-id="0440a-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="0440a-122">**QName**</span></span> | <span data-ttu-id="0440a-123">Имя кода операции, относящегося к задаче.</span><span class="sxs-lookup"><span data-stu-id="0440a-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0440a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0440a-124">Requirements</span></span>



| <span data-ttu-id="0440a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0440a-125">Requirement</span></span> | <span data-ttu-id="0440a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0440a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0440a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0440a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0440a-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0440a-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0440a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0440a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0440a-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0440a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0440a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0440a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="0440a-132">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="0440a-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="0440a-133">**задача (Дефинитионтипе)**</span><span class="sxs-lookup"><span data-stu-id="0440a-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





