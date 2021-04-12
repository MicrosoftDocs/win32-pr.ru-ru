---
title: Сложный тип Виклисчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебивик.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- планировщик задач сложного типа Виклисчедулетипе
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415224"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="47077-104">Сложный тип Виклисчедулетипе</span><span class="sxs-lookup"><span data-stu-id="47077-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="47077-105">Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="47077-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="47077-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="47077-106">Child elements</span></span>



| <span data-ttu-id="47077-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="47077-107">Element</span></span>                                                                               | <span data-ttu-id="47077-108">Тип</span><span class="sxs-lookup"><span data-stu-id="47077-108">Type</span></span>                                                                     | <span data-ttu-id="47077-109">Описание</span><span class="sxs-lookup"><span data-stu-id="47077-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="47077-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="47077-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="47077-111">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="47077-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="47077-112">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="47077-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="47077-113">**виксинтервал**</span><span class="sxs-lookup"><span data-stu-id="47077-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="47077-114">Указывает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="47077-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="47077-115">Требования</span><span class="sxs-lookup"><span data-stu-id="47077-115">Requirements</span></span>



| <span data-ttu-id="47077-116">Требование</span><span class="sxs-lookup"><span data-stu-id="47077-116">Requirement</span></span> | <span data-ttu-id="47077-117">Значение</span><span class="sxs-lookup"><span data-stu-id="47077-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="47077-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47077-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47077-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47077-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="47077-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47077-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47077-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47077-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47077-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47077-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47077-123">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="47077-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





