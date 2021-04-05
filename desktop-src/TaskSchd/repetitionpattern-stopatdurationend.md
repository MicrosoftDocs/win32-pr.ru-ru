---
title: Репетитионпаттерн. Стопатдуратионенд, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, останавливается ли работающий экземпляр задачи в конце шаблона повторения.
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- планировщик задач свойства Стопатдуратионенд
- Планировщик задач свойства Стопатдуратионенд, объект Репетитионпаттерн
- Планировщик задач объекта Репетитионпаттерн, свойство Стопатдуратионенд
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802980"
---
# <a name="repetitionpatternstopatdurationend-property"></a><span data-ttu-id="78517-106">Репетитионпаттерн. Стопатдуратионенд, свойство</span><span class="sxs-lookup"><span data-stu-id="78517-106">RepetitionPattern.StopAtDurationEnd property</span></span>

<span data-ttu-id="78517-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, останавливается ли работающий экземпляр задачи в конце шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="78517-107">For scripting, gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="syntax"></a><span data-ttu-id="78517-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78517-108">Syntax</span></span>


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="78517-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="78517-109">Property value</span></span>

<span data-ttu-id="78517-110">Логическое значение, указывающее, останавливается ли работающий экземпляр задачи в конце шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="78517-110">A Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="78517-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78517-111">Remarks</span></span>

<span data-ttu-id="78517-112">При чтении или записи XML для задачи эти сведения указываются в элементе [**стопатдуратионенд**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="78517-112">When reading or writing XML for a task, this information is specified in the [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="78517-113">Требования</span><span class="sxs-lookup"><span data-stu-id="78517-113">Requirements</span></span>



| <span data-ttu-id="78517-114">Требование</span><span class="sxs-lookup"><span data-stu-id="78517-114">Requirement</span></span> | <span data-ttu-id="78517-115">Значение</span><span class="sxs-lookup"><span data-stu-id="78517-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78517-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78517-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78517-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78517-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="78517-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78517-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78517-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78517-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78517-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="78517-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="78517-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="78517-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="78517-122">DLL</span><span class="sxs-lookup"><span data-stu-id="78517-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78517-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78517-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78517-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78517-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78517-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="78517-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





