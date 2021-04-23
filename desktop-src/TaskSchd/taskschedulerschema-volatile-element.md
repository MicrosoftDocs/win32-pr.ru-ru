---
title: Элемент volatile
description: Указывает, будет ли задача автоматически отключаться при каждом запуске Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- планировщик задач с временными элементами
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803635"
---
# <a name="volatile-element"></a><span data-ttu-id="665ab-104">Элемент volatile</span><span class="sxs-lookup"><span data-stu-id="665ab-104">Volatile Element</span></span>

<span data-ttu-id="665ab-105">Указывает, будет ли задача автоматически отключаться при каждом запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="665ab-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="665ab-106">Элемент **volatile** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="665ab-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="665ab-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="665ab-107">Parent element</span></span>



| <span data-ttu-id="665ab-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="665ab-108">Element</span></span>                                                           | <span data-ttu-id="665ab-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="665ab-109">Derived from</span></span> | <span data-ttu-id="665ab-110">Описание</span><span class="sxs-lookup"><span data-stu-id="665ab-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="665ab-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="665ab-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="665ab-112">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="665ab-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="665ab-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="665ab-113">Remarks</span></span>

<span data-ttu-id="665ab-114">При программировании на C++ этот параметр простоя указывается с помощью свойства [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .</span><span class="sxs-lookup"><span data-stu-id="665ab-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="665ab-115">Требования</span><span class="sxs-lookup"><span data-stu-id="665ab-115">Requirements</span></span>



| <span data-ttu-id="665ab-116">Требование</span><span class="sxs-lookup"><span data-stu-id="665ab-116">Requirement</span></span> | <span data-ttu-id="665ab-117">Значение</span><span class="sxs-lookup"><span data-stu-id="665ab-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="665ab-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="665ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="665ab-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="665ab-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="665ab-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="665ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="665ab-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="665ab-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="665ab-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="665ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665ab-123">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="665ab-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="665ab-124">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="665ab-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





