---
title: Сложный тип Дефинитионтипе
description: Определяет список событий, которые поставщик может заносить в журнал.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Журнал событий сложных типов Дефинитионтипе
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691830"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="81096-104">Сложный тип Дефинитионтипе</span><span class="sxs-lookup"><span data-stu-id="81096-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="81096-105">Определяет список событий, которые поставщик может заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="81096-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="81096-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81096-106">Child elements</span></span>



| <span data-ttu-id="81096-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="81096-107">Element</span></span>                                                           | <span data-ttu-id="81096-108">Тип</span><span class="sxs-lookup"><span data-stu-id="81096-108">Type</span></span>                                                                                       | <span data-ttu-id="81096-109">Описание</span><span class="sxs-lookup"><span data-stu-id="81096-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81096-110">**журнале**</span><span class="sxs-lookup"><span data-stu-id="81096-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="81096-111">**евентдефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="81096-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="81096-112">Определяет событие, которое может регистрироваться поставщиком.</span><span class="sxs-lookup"><span data-stu-id="81096-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="81096-113">**задачи**</span><span class="sxs-lookup"><span data-stu-id="81096-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="81096-114">**таскевентдефинитионтипе**</span><span class="sxs-lookup"><span data-stu-id="81096-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="81096-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="81096-115">Not supported.</span></span><br/> <span data-ttu-id="81096-116">**Windows Server 2008 и Windows Vista:** Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="81096-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="81096-117">(Начиная с компилятора сообщений, который поставляется с версией Windows 7 Windows SDK, события, относящиеся к задачам, больше не поддерживаются.)</span><span class="sxs-lookup"><span data-stu-id="81096-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="81096-118">Требования</span><span class="sxs-lookup"><span data-stu-id="81096-118">Requirements</span></span>



| <span data-ttu-id="81096-119">Требование</span><span class="sxs-lookup"><span data-stu-id="81096-119">Requirement</span></span> | <span data-ttu-id="81096-120">Значение</span><span class="sxs-lookup"><span data-stu-id="81096-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81096-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81096-121">Minimum supported client</span></span><br/> | <span data-ttu-id="81096-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81096-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81096-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81096-123">Minimum supported server</span></span><br/> | <span data-ttu-id="81096-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81096-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





