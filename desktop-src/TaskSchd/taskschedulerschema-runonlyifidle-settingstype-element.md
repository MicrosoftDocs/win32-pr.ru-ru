---
title: Рунонлифидле (Сеттингстипе), элемент
description: Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- планировщик задач элемента Рунонлифидле
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071885"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="1679d-104">Рунонлифидле (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="1679d-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="1679d-105">Указывает, что задача выполняется только в том случае, если компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="1679d-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="1679d-106">Элемент **рунонлифидле** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1679d-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1679d-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="1679d-107">Parent element</span></span>



| <span data-ttu-id="1679d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="1679d-108">Element</span></span>                                                           | <span data-ttu-id="1679d-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="1679d-109">Derived from</span></span>                                                         | <span data-ttu-id="1679d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1679d-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1679d-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="1679d-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1679d-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="1679d-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1679d-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="1679d-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1679d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1679d-114">Remarks</span></span>

<span data-ttu-id="1679d-115">Сведения о разработке на языке C++ см. в разделе [**свойство рунонлифидле объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="1679d-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="1679d-116">Сведения о разработке сценариев см. в разделе [**тасксеттингс. рунонлифидле**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="1679d-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1679d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1679d-117">Requirements</span></span>



| <span data-ttu-id="1679d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1679d-118">Requirement</span></span> | <span data-ttu-id="1679d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1679d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1679d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1679d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1679d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1679d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1679d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1679d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1679d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1679d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1679d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1679d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1679d-125">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="1679d-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1679d-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="1679d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





