---
title: Алловстартондеманд (Сеттингстипе), элемент
description: Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- планировщик задач элемента Алловстартондеманд
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988352"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="941ea-104">Алловстартондеманд (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="941ea-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="941ea-105">Указывает, что задача может быть запущена либо с помощью команды выполнить, либо из контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="941ea-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="941ea-106">Элемент **алловстартондеманд** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="941ea-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="941ea-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="941ea-107">Parent element</span></span>



| <span data-ttu-id="941ea-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="941ea-108">Element</span></span>                                                           | <span data-ttu-id="941ea-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="941ea-109">Derived from</span></span>                                                         | <span data-ttu-id="941ea-110">Описание</span><span class="sxs-lookup"><span data-stu-id="941ea-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="941ea-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="941ea-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="941ea-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="941ea-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="941ea-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="941ea-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="941ea-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="941ea-114">Remarks</span></span>

<span data-ttu-id="941ea-115">Если для этого элемента задано значение true, задача может быть запущена независимо от того, какие триггеры запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="941ea-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="941ea-116">Сведения о разработке на C++ см. в описании [**Свойства алловдемандстарт объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="941ea-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="941ea-117">Сведения о разработке сценариев см. в разделе [**тасксеттингс. алловдемандстарт**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="941ea-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="941ea-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="941ea-118">Examples</span></span>

<span data-ttu-id="941ea-119">Полный пример XML-кода для задачи, которая допускает запуск спроса, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="941ea-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="941ea-120">Требования</span><span class="sxs-lookup"><span data-stu-id="941ea-120">Requirements</span></span>



| <span data-ttu-id="941ea-121">Требование</span><span class="sxs-lookup"><span data-stu-id="941ea-121">Requirement</span></span> | <span data-ttu-id="941ea-122">Значение</span><span class="sxs-lookup"><span data-stu-id="941ea-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="941ea-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="941ea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="941ea-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="941ea-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="941ea-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="941ea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="941ea-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="941ea-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="941ea-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="941ea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="941ea-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="941ea-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





