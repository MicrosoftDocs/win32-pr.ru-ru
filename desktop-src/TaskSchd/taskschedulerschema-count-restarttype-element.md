---
title: Count (Рестарттипе), элемент
description: Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- планировщик задач элемента count
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489861"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="0da49-104">Count (Рестарттипе), элемент</span><span class="sxs-lookup"><span data-stu-id="0da49-104">Count (restartType) Element</span></span>

<span data-ttu-id="0da49-105">Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="0da49-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0da49-106">Элемент определяется сложным типом [**рестарттипе**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0da49-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0da49-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0da49-107">Parent element</span></span>



| <span data-ttu-id="0da49-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0da49-108">Element</span></span>                                                                               | <span data-ttu-id="0da49-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="0da49-109">Derived from</span></span>                                                       | <span data-ttu-id="0da49-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0da49-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0da49-111">**рестартонфаилуре**</span><span class="sxs-lookup"><span data-stu-id="0da49-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="0da49-112">**рестарттипе**</span><span class="sxs-lookup"><span data-stu-id="0da49-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="0da49-113">Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.</span><span class="sxs-lookup"><span data-stu-id="0da49-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0da49-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0da49-114">Remarks</span></span>

<span data-ttu-id="0da49-115">Если этот элемент указан, необходимо также указать элемент [**Interval**](taskschedulerschema-interval-restarttype-element.md) , чтобы сообщить планировщик задач, сколько времени попытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="0da49-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="0da49-116">Сведения о разработке на языке C++ см. в разделе [**свойство рестарткаунт объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="0da49-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="0da49-117">Сведения о разработке сценариев см. в разделе [**тасксеттингс. рестарткаунт**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="0da49-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0da49-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0da49-118">Requirements</span></span>



| <span data-ttu-id="0da49-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0da49-119">Requirement</span></span> | <span data-ttu-id="0da49-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0da49-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0da49-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0da49-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0da49-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0da49-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0da49-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0da49-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0da49-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0da49-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0da49-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0da49-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da49-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="0da49-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





