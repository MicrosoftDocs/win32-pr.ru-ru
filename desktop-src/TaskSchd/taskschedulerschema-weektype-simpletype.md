---
title: Простой тип Виктипе
description: Определяет значения, которые могут использоваться в элементе Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- планировщик задач простого типа Виктипе
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135511"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="1e0fa-104">Простой тип Виктипе</span><span class="sxs-lookup"><span data-stu-id="1e0fa-104">weekType Simple Type</span></span>

<span data-ttu-id="1e0fa-105">Определяет значения, которые могут использоваться в элементе [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0fa-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="1e0fa-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="1e0fa-106">Patterns</span></span>

<span data-ttu-id="1e0fa-107">Простой тип **виктипе** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="1e0fa-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="1e0fa-108">Указывает первую за четвертую неделю месяца (1-4) или всегда за последнюю неделю месяца.</span><span class="sxs-lookup"><span data-stu-id="1e0fa-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0fa-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1e0fa-109">Requirements</span></span>



| <span data-ttu-id="1e0fa-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1e0fa-110">Requirement</span></span> | <span data-ttu-id="1e0fa-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1e0fa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e0fa-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e0fa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1e0fa-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e0fa-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e0fa-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e0fa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1e0fa-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e0fa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e0fa-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e0fa-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0fa-117">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="1e0fa-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="1e0fa-118">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="1e0fa-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





