---
title: Элемент Data (taskType)
description: Определяет дополнительные данные, связанные с задачей, но в противном случае не используется службой планировщик задач.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Элемент данных планировщик задач
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801769"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="06529-104">Элемент Data (taskType)</span><span class="sxs-lookup"><span data-stu-id="06529-104">Data (taskType) Element</span></span>

<span data-ttu-id="06529-105">Определяет дополнительные данные, связанные с задачей, но в противном случае не используется службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="06529-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="06529-106">Элемент **Data** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="06529-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="06529-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="06529-107">Parent element</span></span>



| <span data-ttu-id="06529-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="06529-108">Element</span></span>                                          | <span data-ttu-id="06529-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="06529-109">Derived from</span></span>                                                 | <span data-ttu-id="06529-110">Описание</span><span class="sxs-lookup"><span data-stu-id="06529-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="06529-111">**Задача**</span><span class="sxs-lookup"><span data-stu-id="06529-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="06529-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="06529-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="06529-113">Определяет задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="06529-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06529-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06529-114">Remarks</span></span>

<span data-ttu-id="06529-115">В качестве примера данных этого типа служба журналы и оповещения производительности использует это свойство в качестве контейнера хранилища для запроса счетчика производительности, связанного с задачей.</span><span class="sxs-lookup"><span data-stu-id="06529-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="06529-116">Для разработки на C++ данные задачи указываются с помощью [**свойства Data объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span><span class="sxs-lookup"><span data-stu-id="06529-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="06529-117">При разработке сценариев данные задачи указываются с помощью свойства [**таскдефинитион. Data**](taskdefinition-data.md) .</span><span class="sxs-lookup"><span data-stu-id="06529-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="06529-118">Требования</span><span class="sxs-lookup"><span data-stu-id="06529-118">Requirements</span></span>



| <span data-ttu-id="06529-119">Требование</span><span class="sxs-lookup"><span data-stu-id="06529-119">Requirement</span></span> | <span data-ttu-id="06529-120">Значение</span><span class="sxs-lookup"><span data-stu-id="06529-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06529-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06529-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06529-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06529-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06529-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06529-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06529-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06529-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06529-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06529-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06529-126">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="06529-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="06529-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="06529-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





