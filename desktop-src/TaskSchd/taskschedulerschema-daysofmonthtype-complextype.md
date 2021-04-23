---
title: Сложный тип Дайсофмонстипе
description: Определяет дочерний элемент и сведения о последовательности для элемента DaysOfMonth (Монслисчедулетипе).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- планировщик задач сложного типа Дайсофмонстипе
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415948"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="dab78-104">Сложный тип Дайсофмонстипе</span><span class="sxs-lookup"><span data-stu-id="dab78-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="dab78-105">Определяет дочерний элемент и сведения о последовательности для элемента [**DaysOfMonth (монслисчедулетипе)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dab78-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dab78-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dab78-106">Child elements</span></span>



| <span data-ttu-id="dab78-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="dab78-107">Element</span></span>                                                        | <span data-ttu-id="dab78-108">Тип</span><span class="sxs-lookup"><span data-stu-id="dab78-108">Type</span></span>                                                                    | <span data-ttu-id="dab78-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dab78-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="dab78-110">**День**</span><span class="sxs-lookup"><span data-stu-id="dab78-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="dab78-111">**дайофмонстипе**</span><span class="sxs-lookup"><span data-stu-id="dab78-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="dab78-112">Указывает день месяца, в который выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="dab78-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="dab78-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dab78-113">Requirements</span></span>



| <span data-ttu-id="dab78-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dab78-114">Requirement</span></span> | <span data-ttu-id="dab78-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dab78-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dab78-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dab78-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dab78-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dab78-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dab78-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dab78-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dab78-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dab78-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dab78-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dab78-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab78-121">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="dab78-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="dab78-122">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="dab78-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





