---
title: Усеунифиедсчедулинженгине (Сеттингстипе), элемент
description: Указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- планировщик задач элемента Усеунифиедсчедулинженгине
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071408"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="0da06-104">Усеунифиедсчедулинженгине (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="0da06-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="0da06-105">Указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.</span><span class="sxs-lookup"><span data-stu-id="0da06-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="0da06-106">Элемент **усеунифиедсчедулинженгине** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0da06-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0da06-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0da06-107">Parent element</span></span>



| <span data-ttu-id="0da06-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0da06-108">Element</span></span>                                                           | <span data-ttu-id="0da06-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="0da06-109">Derived from</span></span>                                                         | <span data-ttu-id="0da06-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0da06-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="0da06-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="0da06-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="0da06-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="0da06-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="0da06-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="0da06-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0da06-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0da06-114">Remarks</span></span>

<span data-ttu-id="0da06-115">Значение по умолчанию для этого элемента — false.</span><span class="sxs-lookup"><span data-stu-id="0da06-115">The default setting for this element is False.</span></span>

<span data-ttu-id="0da06-116">Для разработки на C++ эта информация доступна через свойство [**ITaskSettings2:: усеунифиедсчедулинженгине**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .</span><span class="sxs-lookup"><span data-stu-id="0da06-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0da06-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="0da06-117">Examples</span></span>

<span data-ttu-id="0da06-118">Следующий XML-код определяет элемент Settings, который указывает, что для выполнения этой задачи будет использоваться единый механизм планирования.</span><span class="sxs-lookup"><span data-stu-id="0da06-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="0da06-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0da06-119">Requirements</span></span>



| <span data-ttu-id="0da06-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0da06-120">Requirement</span></span> | <span data-ttu-id="0da06-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0da06-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0da06-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0da06-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0da06-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0da06-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0da06-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0da06-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0da06-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0da06-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0da06-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0da06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da06-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="0da06-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





