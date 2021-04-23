---
title: Сложный тип Монслисчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебимонс (Календартригжертипе).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- планировщик задач сложного типа Монслисчедулетипе
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681845"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="a9708-104">Сложный тип Монслисчедулетипе</span><span class="sxs-lookup"><span data-stu-id="a9708-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="a9708-105">Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебимонс (календартригжертипе)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a9708-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a9708-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a9708-106">Child elements</span></span>



| <span data-ttu-id="a9708-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a9708-107">Element</span></span>                                                                            | <span data-ttu-id="a9708-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a9708-108">Type</span></span>                                                                       | <span data-ttu-id="a9708-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a9708-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9708-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="a9708-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="a9708-111">**дайсофмонстипе**</span><span class="sxs-lookup"><span data-stu-id="a9708-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="a9708-112">Указывает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="a9708-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="a9708-113">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="a9708-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="a9708-114">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="a9708-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="a9708-115">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="a9708-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a9708-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a9708-116">Requirements</span></span>



| <span data-ttu-id="a9708-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a9708-117">Requirement</span></span> | <span data-ttu-id="a9708-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a9708-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9708-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9708-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9708-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9708-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9708-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9708-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9708-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9708-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9708-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9708-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9708-124">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="a9708-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a9708-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a9708-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





