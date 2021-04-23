---
title: Сложный тип taskType (планировщик задач)
description: Определяет дочерние элементы и сведения о последовательности для элемента Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- планировщик задач сложного типа taskType
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491667"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="6a391-104">Сложный тип taskType</span><span class="sxs-lookup"><span data-stu-id="6a391-104">taskType Complex Type</span></span>

<span data-ttu-id="6a391-105">Определяет дочерние элементы и сведения о последовательности для элемента [**Task**](taskschedulerschema-task-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6a391-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6a391-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6a391-106">Child elements</span></span>



| <span data-ttu-id="6a391-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6a391-107">Element</span></span>                                                                           | <span data-ttu-id="6a391-108">Тип</span><span class="sxs-lookup"><span data-stu-id="6a391-108">Type</span></span>                                                                                 | <span data-ttu-id="6a391-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6a391-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a391-110">**Действия**</span><span class="sxs-lookup"><span data-stu-id="6a391-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="6a391-111">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="6a391-112">Указывает действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="6a391-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="6a391-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="6a391-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="6a391-114">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="6a391-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="6a391-115">Указывает дополнительные данные, связанные с задачей, но не используемые службой планировщик задач в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6a391-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="6a391-116">**Субъекты**</span><span class="sxs-lookup"><span data-stu-id="6a391-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="6a391-117">**принЦипалстипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="6a391-118">Указывает контексты безопасности, которые могут использоваться для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6a391-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="6a391-119">**регистратионинфо**</span><span class="sxs-lookup"><span data-stu-id="6a391-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="6a391-120">**регистратионинфотипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="6a391-121">Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="6a391-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="6a391-122">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="6a391-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="6a391-123">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="6a391-124">Задает параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="6a391-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="6a391-125">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="6a391-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="6a391-126">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="6a391-127">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="6a391-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="6a391-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6a391-128">Attributes</span></span>



| <span data-ttu-id="6a391-129">Имя</span><span class="sxs-lookup"><span data-stu-id="6a391-129">Name</span></span>    | <span data-ttu-id="6a391-130">Тип</span><span class="sxs-lookup"><span data-stu-id="6a391-130">Type</span></span>                                                              | <span data-ttu-id="6a391-131">Description</span><span class="sxs-lookup"><span data-stu-id="6a391-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="6a391-132">version</span><span class="sxs-lookup"><span data-stu-id="6a391-132">version</span></span> | [<span data-ttu-id="6a391-133">**версионтипе**</span><span class="sxs-lookup"><span data-stu-id="6a391-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="6a391-134">Указывает версию задачи.</span><span class="sxs-lookup"><span data-stu-id="6a391-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6a391-135">Требования</span><span class="sxs-lookup"><span data-stu-id="6a391-135">Requirements</span></span>



| <span data-ttu-id="6a391-136">Требование</span><span class="sxs-lookup"><span data-stu-id="6a391-136">Requirement</span></span> | <span data-ttu-id="6a391-137">Значение</span><span class="sxs-lookup"><span data-stu-id="6a391-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a391-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a391-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6a391-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a391-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a391-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a391-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6a391-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a391-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a391-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a391-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a391-143">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="6a391-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6a391-144">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="6a391-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





