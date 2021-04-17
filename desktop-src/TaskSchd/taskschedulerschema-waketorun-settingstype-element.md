---
title: Вакеторун (Сеттингстипе), элемент
description: Указывает, что планировщик задач будет выводить компьютер из спящего режима во время выполнения задачи.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- планировщик задач элемента Вакеторун
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682094"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="23a0c-104">Вакеторун (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="23a0c-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="23a0c-105">Указывает, что планировщик задач будет выводить компьютер из спящего режима во время выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="23a0c-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="23a0c-106">Элемент **вакеторун** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="23a0c-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="23a0c-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="23a0c-107">Parent element</span></span>



| <span data-ttu-id="23a0c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="23a0c-108">Element</span></span>                                                           | <span data-ttu-id="23a0c-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="23a0c-109">Derived from</span></span>                                                         | <span data-ttu-id="23a0c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="23a0c-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="23a0c-111">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="23a0c-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="23a0c-112">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="23a0c-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="23a0c-113">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="23a0c-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="23a0c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23a0c-114">Remarks</span></span>

<span data-ttu-id="23a0c-115">Когда служба планировщик задач пробуждает компьютер для выполнения задачи, экран может остаться недоступным, даже если компьютер больше не находится в спящем или спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="23a0c-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="23a0c-116">Экран будет включен, когда Windows Vista обнаружит, что пользователь вернулся на использование компьютера.</span><span class="sxs-lookup"><span data-stu-id="23a0c-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="23a0c-117">Сведения о разработке на языке C++ см. в разделе [**свойство вакеторун объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="23a0c-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="23a0c-118">Сведения о разработке сценариев см. в разделе [**тасксеттингс. вакеторун**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="23a0c-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23a0c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="23a0c-119">Requirements</span></span>



| <span data-ttu-id="23a0c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="23a0c-120">Requirement</span></span> | <span data-ttu-id="23a0c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="23a0c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23a0c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23a0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23a0c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23a0c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23a0c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23a0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23a0c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23a0c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23a0c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23a0c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a0c-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="23a0c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="23a0c-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="23a0c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





