---
title: Свойство Trigger. Ендбаундари
description: Для создания скриптов Возвращает или задает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- планировщик задач свойства Ендбаундари
- Планировщик задач свойства Ендбаундари, объект Trigger
- Планировщик задач объекта триггера, свойство Ендбаундари
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071406"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="21d4d-107">Свойство Trigger. Ендбаундари</span><span class="sxs-lookup"><span data-stu-id="21d4d-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="21d4d-108">Для создания скриптов Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="21d4d-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="21d4d-109">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="21d4d-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d4d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21d4d-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="21d4d-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="21d4d-111">Property value</span></span>

<span data-ttu-id="21d4d-112">Дата и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="21d4d-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="21d4d-113">Дата и время должны быть в следующем формате: гггг-мм-DDTHH: мм: СС (+-) чч: мм.</span><span class="sxs-lookup"><span data-stu-id="21d4d-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="21d4d-114">Например, дата 11 октября 2005 по 1:21:17 в тихоокеанском часовом поясе будет записана как 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="21d4d-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="21d4d-115">Раздел (+-) чч: мм в формате описывает часовой пояс как определенное число часов перед временем в формате UTC (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="21d4d-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="21d4d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21d4d-116">Remarks</span></span>

<span data-ttu-id="21d4d-117">При чтении или записи XML для задачи свойство Enabled указывается с помощью элемента [**ендбаундари**](taskschedulerschema-endboundary-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="21d4d-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d4d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="21d4d-118">Requirements</span></span>



| <span data-ttu-id="21d4d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="21d4d-119">Requirement</span></span> | <span data-ttu-id="21d4d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="21d4d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21d4d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21d4d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21d4d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21d4d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="21d4d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21d4d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21d4d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21d4d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21d4d-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="21d4d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="21d4d-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21d4d-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21d4d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="21d4d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21d4d-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21d4d-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21d4d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21d4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d4d-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="21d4d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





