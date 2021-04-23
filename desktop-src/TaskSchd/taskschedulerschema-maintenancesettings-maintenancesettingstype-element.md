---
title: Маинтенанцесеттингс (Маинтенанцесеттингстипе), элемент
description: Указывает, как планировщик задач выполняет задачи во время автоматического обслуживания.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- планировщик задач элемента Маинтенанцесеттингс
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136923"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="194ed-104">Маинтенанцесеттингс (Маинтенанцесеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="194ed-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="194ed-105">Указывает, как планировщик задач выполняет задачи во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="194ed-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="194ed-106">Элемент **маинтенанцесеттингс** определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="194ed-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="194ed-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="194ed-107">Parent element</span></span>



| <span data-ttu-id="194ed-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="194ed-108">Element</span></span>                                                           | <span data-ttu-id="194ed-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="194ed-109">Derived from</span></span>                                                         | <span data-ttu-id="194ed-110">Описание</span><span class="sxs-lookup"><span data-stu-id="194ed-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="194ed-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="194ed-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="194ed-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="194ed-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="194ed-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="194ed-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="194ed-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="194ed-114">Child elements</span></span>



| <span data-ttu-id="194ed-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="194ed-115">Element</span></span>                                                    | <span data-ttu-id="194ed-116">Тип</span><span class="sxs-lookup"><span data-stu-id="194ed-116">Type</span></span>    | <span data-ttu-id="194ed-117">Описание</span><span class="sxs-lookup"><span data-stu-id="194ed-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="194ed-118">**Крайний срок**</span><span class="sxs-lookup"><span data-stu-id="194ed-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="194ed-119">Указывает период времени, по истечении которого планировщик заданий будет пытаться запустить задачу во время аварийного автоматического обслуживания, если это не удалось завершить во время регулярного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="194ed-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="194ed-120">**Монопольный доступ**</span><span class="sxs-lookup"><span data-stu-id="194ed-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="194ed-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="194ed-121">boolean</span></span> | <span data-ttu-id="194ed-122">Если задано значение true, задача будет запускаться только в других задачах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="194ed-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="194ed-123">**Периода**</span><span class="sxs-lookup"><span data-stu-id="194ed-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="194ed-124">Указывает, как часто задача должна запускаться во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="194ed-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="194ed-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="194ed-125">Remarks</span></span>

<span data-ttu-id="194ed-126">При программировании на C++ этот параметр простоя указывается с помощью свойства [**ITaskSettings3:: маинтенанцесеттингс**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .</span><span class="sxs-lookup"><span data-stu-id="194ed-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="194ed-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="194ed-127">Examples</span></span>

<span data-ttu-id="194ed-128">Следующий XML-код определяет элемент Settings, который указывает планировщик задач выполнить задачу один раз в течение 5 дней во время регулярного автоматического обслуживания. в случае сбоя в течение 15 дней запустите попытку выполнения задачи во время аварийного автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="194ed-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="194ed-129">Требования</span><span class="sxs-lookup"><span data-stu-id="194ed-129">Requirements</span></span>



| <span data-ttu-id="194ed-130">Требование</span><span class="sxs-lookup"><span data-stu-id="194ed-130">Requirement</span></span> | <span data-ttu-id="194ed-131">Значение</span><span class="sxs-lookup"><span data-stu-id="194ed-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="194ed-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="194ed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="194ed-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="194ed-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="194ed-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="194ed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="194ed-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="194ed-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="194ed-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="194ed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194ed-137">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="194ed-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="194ed-138">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="194ed-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





