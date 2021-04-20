---
title: Даилитригжер. Рандомделай, свойство
description: Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера. | Даилитригжер. Рандомделай, свойство
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- планировщик задач свойства Рандомделай
- Планировщик задач свойства Рандомделай, объект Даилитригжер
- Планировщик задач объекта Даилитригжер, свойство Рандомделай
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734109"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="d748e-107">Даилитригжер. Рандомделай, свойство</span><span class="sxs-lookup"><span data-stu-id="d748e-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="d748e-108">Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="d748e-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="d748e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d748e-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="d748e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d748e-110">Property value</span></span>

<span data-ttu-id="d748e-111">Время задержки, которое случайным образом добавляется к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="d748e-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="d748e-112">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, P2DT5S имеет 2 дня, 5 секунд задержки).</span><span class="sxs-lookup"><span data-stu-id="d748e-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="d748e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d748e-113">Requirements</span></span>



| <span data-ttu-id="d748e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d748e-114">Requirement</span></span> | <span data-ttu-id="d748e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d748e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d748e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d748e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d748e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d748e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d748e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d748e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d748e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d748e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d748e-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d748e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d748e-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d748e-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d748e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d748e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d748e-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d748e-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d748e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d748e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d748e-125">**даилитригжер**</span><span class="sxs-lookup"><span data-stu-id="d748e-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="d748e-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d748e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





