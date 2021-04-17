---
title: Сложный тип Таскевентдефинитионтипе
description: Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал. | Сложный тип Таскевентдефинитионтипе
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Журнал событий сложных типов Таскевентдефинитионтипе
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694045"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="9cae5-105">Сложный тип Таскевентдефинитионтипе</span><span class="sxs-lookup"><span data-stu-id="9cae5-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="9cae5-106">\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK Windows 7, сложный тип Таскевентдефинитионтипе больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="9cae5-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="9cae5-107">Вместо этого используйте коды операций для конкретных задач, чтобы предоставить те же функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="9cae5-108">Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="9cae5-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9cae5-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9cae5-109">Child elements</span></span>



| <span data-ttu-id="9cae5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="9cae5-110">Element</span></span>                                                                      | <span data-ttu-id="9cae5-111">Тип</span><span class="sxs-lookup"><span data-stu-id="9cae5-111">Type</span></span>                                                                               | <span data-ttu-id="9cae5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9cae5-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9cae5-113">**event**</span><span class="sxs-lookup"><span data-stu-id="9cae5-113">**event**</span></span>                                                                    | [<span data-ttu-id="9cae5-114">**евентдефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="9cae5-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="9cae5-115">Событие, относящееся к задаче, опубликованное с помощью задачи.</span><span class="sxs-lookup"><span data-stu-id="9cae5-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="9cae5-116">**транслируют**</span><span class="sxs-lookup"><span data-stu-id="9cae5-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="9cae5-117">Код операции, относящийся к задаче, для события.</span><span class="sxs-lookup"><span data-stu-id="9cae5-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="9cae5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9cae5-118">Attributes</span></span>



| <span data-ttu-id="9cae5-119">Имя</span><span class="sxs-lookup"><span data-stu-id="9cae5-119">Name</span></span> | <span data-ttu-id="9cae5-120">Тип</span><span class="sxs-lookup"><span data-stu-id="9cae5-120">Type</span></span>      | <span data-ttu-id="9cae5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9cae5-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="9cae5-122">name</span><span class="sxs-lookup"><span data-stu-id="9cae5-122">name</span></span> | <span data-ttu-id="9cae5-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="9cae5-123">**QName**</span></span> | <span data-ttu-id="9cae5-124">Имя кода операции, относящегося к задаче.</span><span class="sxs-lookup"><span data-stu-id="9cae5-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="9cae5-125">name</span><span class="sxs-lookup"><span data-stu-id="9cae5-125">name</span></span> | <span data-ttu-id="9cae5-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="9cae5-126">anyURI</span></span>    | <span data-ttu-id="9cae5-127">Имя данной задачи.</span><span class="sxs-lookup"><span data-stu-id="9cae5-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="9cae5-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9cae5-128">Requirements</span></span>



| <span data-ttu-id="9cae5-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9cae5-129">Requirement</span></span> | <span data-ttu-id="9cae5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9cae5-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9cae5-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cae5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9cae5-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9cae5-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cae5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9cae5-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cae5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





