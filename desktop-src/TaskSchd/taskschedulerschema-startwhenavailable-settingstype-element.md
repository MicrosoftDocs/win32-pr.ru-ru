---
title: Стартвхенаваилабле (Сеттингстипе), элемент
description: Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- планировщик задач элемента Стартвхенаваилабле
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988349"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="86b0d-104">Стартвхенаваилабле (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="86b0d-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="86b0d-105">Указывает, что планировщик задач может запустить задачу в любое время после прохождения запланированного времени.</span><span class="sxs-lookup"><span data-stu-id="86b0d-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="86b0d-106">Элемент **стартвхенаваилабле** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="86b0d-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="86b0d-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="86b0d-107">Parent element</span></span>



| <span data-ttu-id="86b0d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="86b0d-108">Element</span></span>                                                           | <span data-ttu-id="86b0d-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="86b0d-109">Derived from</span></span>                                                         | <span data-ttu-id="86b0d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="86b0d-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="86b0d-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="86b0d-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="86b0d-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="86b0d-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="86b0d-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="86b0d-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="86b0d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86b0d-114">Remarks</span></span>

<span data-ttu-id="86b0d-115">Это свойство применимо только к задачам с превышением времени.</span><span class="sxs-lookup"><span data-stu-id="86b0d-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="86b0d-116">Сведения о разработке на языке C++ см. в разделе [**свойство стартвхенаваилабле объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="86b0d-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="86b0d-117">Сведения о разработке сценариев см. в разделе [**тасксеттингс. стартвхенаваилабле**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="86b0d-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="86b0d-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="86b0d-118">Examples</span></span>

<span data-ttu-id="86b0d-119">Следующий XML-код определяет элемент Settings, позволяющий планировщик задач запускать задачу, когда она доступна.</span><span class="sxs-lookup"><span data-stu-id="86b0d-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="86b0d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="86b0d-120">Requirements</span></span>



| <span data-ttu-id="86b0d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="86b0d-121">Requirement</span></span> | <span data-ttu-id="86b0d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="86b0d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86b0d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86b0d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86b0d-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86b0d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="86b0d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86b0d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86b0d-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86b0d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86b0d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86b0d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b0d-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="86b0d-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





