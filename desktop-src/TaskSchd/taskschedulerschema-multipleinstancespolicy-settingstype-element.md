---
title: Мултиплеинстанцесполици (Сеттингстипе), элемент
description: Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- планировщик задач элемента Мултиплеинстанцесполици
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672733"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="4edc9-104">Мултиплеинстанцесполици (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4edc9-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="4edc9-105">Указывает политику, определяющую, как планировщик задач работает с несколькими экземплярами задачи.</span><span class="sxs-lookup"><span data-stu-id="4edc9-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="4edc9-106">Элемент **мултиплеинстанцесполици** определяется простым типом [**мултиплеинстанцесполицитипе**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="4edc9-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4edc9-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4edc9-107">Parent element</span></span>



| <span data-ttu-id="4edc9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4edc9-108">Element</span></span>                                                           | <span data-ttu-id="4edc9-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4edc9-109">Derived from</span></span>                                                         | <span data-ttu-id="4edc9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4edc9-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4edc9-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="4edc9-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="4edc9-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="4edc9-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="4edc9-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="4edc9-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4edc9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4edc9-114">Remarks</span></span>

<span data-ttu-id="4edc9-115">Сведения о разработке на языке C++ см. в разделе [**свойство мултиплеинстанцес объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="4edc9-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="4edc9-116">Сведения о разработке сценариев см. в разделе [**тасксеттингс. мултиплеинстанцес**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="4edc9-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="4edc9-117">Ограниченные значения</span><span class="sxs-lookup"><span data-stu-id="4edc9-117">Restricted Values</span></span>

<span data-ttu-id="4edc9-118">Этот элемент ограничен следующими значениями.</span><span class="sxs-lookup"><span data-stu-id="4edc9-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="4edc9-119">Parallel: запускает новый экземпляр во время работы существующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4edc9-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="4edc9-120">Queue: запускает новый экземпляр Task после завершения всех остальных экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="4edc9-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="4edc9-121">Игноренев: по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4edc9-121">IgnoreNew: Default.</span></span> <span data-ttu-id="4edc9-122">Не запускает новый экземпляр, если запущен существующий экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="4edc9-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="4edc9-123">Стопексистинг: останавливает существующий экземпляр задачи перед запуском нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4edc9-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="4edc9-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="4edc9-124">Examples</span></span>

<span data-ttu-id="4edc9-125">Следующий XML-код определяет элемент Settings, позволяющий параллельно выполнять несколько экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="4edc9-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="4edc9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4edc9-126">Requirements</span></span>



| <span data-ttu-id="4edc9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4edc9-127">Requirement</span></span> | <span data-ttu-id="4edc9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4edc9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4edc9-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4edc9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4edc9-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4edc9-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4edc9-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4edc9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4edc9-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4edc9-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4edc9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4edc9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edc9-134">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4edc9-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





