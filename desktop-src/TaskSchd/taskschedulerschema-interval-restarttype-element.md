---
title: Элемент Interval (Рестарттипе)
description: Указывает, как долго планировщик задач будет пытаться перезапустить задачу.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Элемент Interval планировщик задач
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734189"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="c9963-104">Элемент Interval (Рестарттипе)</span><span class="sxs-lookup"><span data-stu-id="c9963-104">Interval (restartType) Element</span></span>

<span data-ttu-id="c9963-105">Указывает, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="c9963-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="c9963-106">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, "PT5M" — 5 минут, "PT1H" — 1 час, а "PT20M" — 20 минут).</span><span class="sxs-lookup"><span data-stu-id="c9963-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="c9963-107">Максимально допустимое время — 31 день. минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="c9963-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="c9963-108">Элемент определяется сложным типом [**рестарттипе**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9963-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c9963-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c9963-109">Parent element</span></span>



| <span data-ttu-id="c9963-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="c9963-110">Element</span></span>                                                                               | <span data-ttu-id="c9963-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c9963-111">Derived from</span></span>                                                       | <span data-ttu-id="c9963-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c9963-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9963-113">**рестартонфаилуре**</span><span class="sxs-lookup"><span data-stu-id="c9963-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="c9963-114">**рестарттипе**</span><span class="sxs-lookup"><span data-stu-id="c9963-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="c9963-115">Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.</span><span class="sxs-lookup"><span data-stu-id="c9963-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c9963-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9963-116">Remarks</span></span>

<span data-ttu-id="c9963-117">Если этот элемент указан, необходимо также указать элемент [**Count**](taskschedulerschema-count-restarttype-element.md) , чтобы сообщить планировщик задач, сколько раз оно должно попытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="c9963-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="c9963-118">Сведения о разработке на языке C++ см. в разделе [**свойство рестартинтервал объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span><span class="sxs-lookup"><span data-stu-id="c9963-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="c9963-119">Сведения о разработке сценариев см. в разделе [**тасксеттингс. рестартинтервал**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="c9963-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9963-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c9963-120">Requirements</span></span>



| <span data-ttu-id="c9963-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c9963-121">Requirement</span></span> | <span data-ttu-id="c9963-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c9963-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9963-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9963-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9963-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9963-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9963-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9963-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9963-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9963-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9963-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9963-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9963-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c9963-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





