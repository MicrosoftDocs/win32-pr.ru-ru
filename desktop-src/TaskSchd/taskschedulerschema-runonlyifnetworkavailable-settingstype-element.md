---
title: Рунонлифнетворкаваилабле (Сеттингстипе), элемент
description: Указывает, что планировщик задач будет выполнять задачу только при доступности сети.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- планировщик задач элемента Рунонлифнетворкаваилабле
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989146"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="9c18f-104">Рунонлифнетворкаваилабле (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="9c18f-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="9c18f-105">Указывает, что планировщик задач будет выполнять задачу только при доступности сети.</span><span class="sxs-lookup"><span data-stu-id="9c18f-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="9c18f-106">Элемент **рунонлифнетворкаваилабле** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9c18f-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9c18f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="9c18f-107">Parent element</span></span>



| <span data-ttu-id="9c18f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9c18f-108">Element</span></span>                                                           | <span data-ttu-id="9c18f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="9c18f-109">Derived from</span></span>                                                         | <span data-ttu-id="9c18f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9c18f-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c18f-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="9c18f-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="9c18f-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="9c18f-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="9c18f-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="9c18f-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c18f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c18f-114">Remarks</span></span>

<span data-ttu-id="9c18f-115">Сведения о разработке на языке C++ см. в разделе [**свойство рунонлифнетворкаваилабле объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="9c18f-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="9c18f-116">Сведения о разработке сценариев см. в разделе [**тасксеттингс. рунонлифнетворкаваилабле**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="9c18f-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9c18f-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9c18f-117">Examples</span></span>

<span data-ttu-id="9c18f-118">Следующий XML-код определяет элемент Settings, который позволяет задаче запускаться только в случае доступности сети.</span><span class="sxs-lookup"><span data-stu-id="9c18f-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="9c18f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9c18f-119">Requirements</span></span>



| <span data-ttu-id="9c18f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9c18f-120">Requirement</span></span> | <span data-ttu-id="9c18f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9c18f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c18f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c18f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c18f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c18f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c18f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c18f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c18f-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c18f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c18f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c18f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c18f-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="9c18f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





