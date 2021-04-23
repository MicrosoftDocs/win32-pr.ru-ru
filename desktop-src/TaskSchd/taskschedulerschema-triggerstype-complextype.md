---
title: Сложный тип Тригжерстипе
description: Определяет группу (Тригжерграуп) для всех элементов Trigger.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- планировщик задач сложного типа Тригжерстипе
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682127"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="0717d-104">Сложный тип Тригжерстипе</span><span class="sxs-lookup"><span data-stu-id="0717d-104">triggersType Complex Type</span></span>

<span data-ttu-id="0717d-105">Определяет группу ([**тригжерграуп**](taskschedulerschema-triggergroup-group.md)) для всех элементов Trigger.</span><span class="sxs-lookup"><span data-stu-id="0717d-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="0717d-106">Группа [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) содержит список триггеров, которые можно использовать в задаче.</span><span class="sxs-lookup"><span data-stu-id="0717d-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="0717d-107">Требования</span><span class="sxs-lookup"><span data-stu-id="0717d-107">Requirements</span></span>



| <span data-ttu-id="0717d-108">Требование</span><span class="sxs-lookup"><span data-stu-id="0717d-108">Requirement</span></span> | <span data-ttu-id="0717d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="0717d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0717d-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0717d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="0717d-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0717d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0717d-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0717d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="0717d-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0717d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0717d-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0717d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0717d-115">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0717d-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





