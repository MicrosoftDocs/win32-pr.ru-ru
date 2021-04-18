---
title: Сложный тип Даилисчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебидай.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- планировщик задач сложного типа Даилисчедулетипе
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682007"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="a94f4-104">Сложный тип Даилисчедулетипе</span><span class="sxs-lookup"><span data-stu-id="a94f4-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="a94f4-105">Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a94f4-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a94f4-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a94f4-106">Child elements</span></span>



| <span data-ttu-id="a94f4-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a94f4-107">Element</span></span>                                                                            | <span data-ttu-id="a94f4-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a94f4-108">Type</span></span> | <span data-ttu-id="a94f4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a94f4-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="a94f4-110">**дайсинтервал**</span><span class="sxs-lookup"><span data-stu-id="a94f4-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="a94f4-111">Указывает интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="a94f4-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="a94f4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a94f4-112">Requirements</span></span>



| <span data-ttu-id="a94f4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a94f4-113">Requirement</span></span> | <span data-ttu-id="a94f4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a94f4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a94f4-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a94f4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a94f4-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a94f4-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a94f4-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a94f4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a94f4-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a94f4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a94f4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a94f4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94f4-120">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="a94f4-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a94f4-121">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a94f4-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





