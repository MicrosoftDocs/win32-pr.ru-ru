---
title: Рестартонфаилуре (Сеттингстипе), элемент
description: Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- планировщик задач элемента Рестартонфаилуре
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262227"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="38951-104">Рестартонфаилуре (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="38951-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="38951-105">Указывает, что планировщик задач попытается перезапустить задачу в случае сбоя задачи по какой бы то ни было причине.</span><span class="sxs-lookup"><span data-stu-id="38951-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="38951-106">Элемент **рестартонфаилуре** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="38951-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="38951-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="38951-107">Parent element</span></span>



| <span data-ttu-id="38951-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="38951-108">Element</span></span>                                                           | <span data-ttu-id="38951-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="38951-109">Derived from</span></span>                                                         | <span data-ttu-id="38951-110">Описание</span><span class="sxs-lookup"><span data-stu-id="38951-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="38951-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="38951-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="38951-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="38951-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="38951-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="38951-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="38951-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="38951-114">Child elements</span></span>



| <span data-ttu-id="38951-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="38951-115">Element</span></span>                                                              | <span data-ttu-id="38951-116">Тип</span><span class="sxs-lookup"><span data-stu-id="38951-116">Type</span></span>         | <span data-ttu-id="38951-117">Описание</span><span class="sxs-lookup"><span data-stu-id="38951-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38951-118">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="38951-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="38951-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="38951-119">unsignedByte</span></span> | <span data-ttu-id="38951-120">Указывает, сколько раз планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="38951-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="38951-121">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="38951-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="38951-122">длительность</span><span class="sxs-lookup"><span data-stu-id="38951-122">duration</span></span>     | <span data-ttu-id="38951-123">Указывает, как долго планировщик задач будет пытаться перезапустить задачу.</span><span class="sxs-lookup"><span data-stu-id="38951-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="38951-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38951-124">Remarks</span></span>

<span data-ttu-id="38951-125">Если приложение задает параметры задачи, доступ к этим данным осуществляется через свойства [**рестарткаунт**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) и [**рестартинтервал**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) интерфейса [**итасксеттингс**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) .</span><span class="sxs-lookup"><span data-stu-id="38951-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="38951-126">Для создания скриптов эти сведения доступны через свойства [**тасксеттингс. рестарткаунт**](tasksettings-restartcount.md) и [**тасксеттингс. рестартинтервал**](tasksettings-restartinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="38951-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="38951-127">Оба дочерних элемента должны быть заданы, чтобы указать, как планировщик задач перезапускает задачу.</span><span class="sxs-lookup"><span data-stu-id="38951-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="38951-128">Требования</span><span class="sxs-lookup"><span data-stu-id="38951-128">Requirements</span></span>



| <span data-ttu-id="38951-129">Требование</span><span class="sxs-lookup"><span data-stu-id="38951-129">Requirement</span></span> | <span data-ttu-id="38951-130">Значение</span><span class="sxs-lookup"><span data-stu-id="38951-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38951-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38951-131">Minimum supported client</span></span><br/> | <span data-ttu-id="38951-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38951-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38951-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38951-133">Minimum supported server</span></span><br/> | <span data-ttu-id="38951-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38951-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38951-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38951-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38951-136">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="38951-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





