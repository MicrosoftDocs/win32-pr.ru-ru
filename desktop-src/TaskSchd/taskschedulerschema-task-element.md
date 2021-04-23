---
title: Элемент Task
description: Определяет задачу, выполняемую службой планировщик задач.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- планировщик задач элемента Task
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891609"
---
# <a name="task-element"></a><span data-ttu-id="65942-104">Элемент Task</span><span class="sxs-lookup"><span data-stu-id="65942-104">Task Element</span></span>

<span data-ttu-id="65942-105">Определяет задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="65942-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="65942-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65942-106">Child elements</span></span>



| <span data-ttu-id="65942-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="65942-107">Element</span></span>                                                                           | <span data-ttu-id="65942-108">Тип</span><span class="sxs-lookup"><span data-stu-id="65942-108">Type</span></span>                                                                                 | <span data-ttu-id="65942-109">Описание</span><span class="sxs-lookup"><span data-stu-id="65942-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65942-110">**Действия**</span><span class="sxs-lookup"><span data-stu-id="65942-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="65942-111">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="65942-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="65942-112">Указывает действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="65942-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="65942-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="65942-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="65942-114">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="65942-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="65942-115">Указывает дополнительные данные, связанные с задачей, но не используемые службой планировщик задач в противном случае.</span><span class="sxs-lookup"><span data-stu-id="65942-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="65942-116">**Субъекты**</span><span class="sxs-lookup"><span data-stu-id="65942-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="65942-117">**принЦипалстипе**</span><span class="sxs-lookup"><span data-stu-id="65942-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="65942-118">Указывает контексты безопасности, которые могут использоваться для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="65942-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="65942-119">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="65942-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="65942-120">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="65942-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="65942-121">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="65942-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="65942-122">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="65942-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="65942-123">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="65942-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="65942-124">Задает параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="65942-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="65942-125">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="65942-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="65942-126">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="65942-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="65942-127">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="65942-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="65942-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65942-128">Remarks</span></span>

<span data-ttu-id="65942-129">Сведения о разработке с + + см. в разделе [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="65942-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="65942-130">Сведения о разработке сценариев см. в разделе [**таскдефинитион**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="65942-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65942-131">Требования</span><span class="sxs-lookup"><span data-stu-id="65942-131">Requirements</span></span>



| <span data-ttu-id="65942-132">Требование</span><span class="sxs-lookup"><span data-stu-id="65942-132">Requirement</span></span> | <span data-ttu-id="65942-133">Значение</span><span class="sxs-lookup"><span data-stu-id="65942-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65942-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65942-134">Minimum supported client</span></span><br/> | <span data-ttu-id="65942-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65942-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65942-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65942-136">Minimum supported server</span></span><br/> | <span data-ttu-id="65942-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65942-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





