---
title: Свойство Trigger. Стартбаундари
description: Для создания скриптов Возвращает или задает дату и время активации триггера.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- планировщик задач свойства Стартбаундари
- Планировщик задач свойства Стартбаундари, объект Trigger
- Планировщик задач объекта триггера, свойство Стартбаундари
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801745"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="5f87f-106">Свойство Trigger. Стартбаундари</span><span class="sxs-lookup"><span data-stu-id="5f87f-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="5f87f-107">Для создания скриптов Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="5f87f-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f87f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f87f-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="5f87f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5f87f-109">Property value</span></span>

<span data-ttu-id="5f87f-110">Дата и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="5f87f-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="5f87f-111">Дата и время должны быть в следующем формате: гггг-мм-DDTHH: мм: СС (+-) чч: мм.</span><span class="sxs-lookup"><span data-stu-id="5f87f-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="5f87f-112">Например, дата 11 октября 2005 по 1:21:17 в тихоокеанском часовом поясе будет записана как 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="5f87f-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="5f87f-113">Раздел (+-) чч: мм в формате описывает часовой пояс как определенное число часов перед временем в формате UTC (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="5f87f-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f87f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f87f-114">Remarks</span></span>

<span data-ttu-id="5f87f-115">При чтении или записи XML для задачи начальная граница триггера задается в элементе [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="5f87f-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f87f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5f87f-116">Requirements</span></span>



| <span data-ttu-id="5f87f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5f87f-117">Requirement</span></span> | <span data-ttu-id="5f87f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f87f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f87f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f87f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f87f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f87f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f87f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f87f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f87f-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f87f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f87f-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5f87f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f87f-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f87f-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f87f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f87f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f87f-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f87f-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f87f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f87f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f87f-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5f87f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





