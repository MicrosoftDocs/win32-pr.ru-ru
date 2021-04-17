---
title: Репетитионпаттерн. Duration, свойство
description: Для создания скриптов Возвращает или задает время повторения шаблона.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Свойство Duration планировщик задач
- Свойство Duration планировщик задач, объект Репетитионпаттерн
- Планировщик задач объекта Репетитионпаттерн, свойство Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681990"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="4fcba-106">Репетитионпаттерн. Duration, свойство</span><span class="sxs-lookup"><span data-stu-id="4fcba-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="4fcba-107">Для создания скриптов Возвращает или задает время повторения шаблона.</span><span class="sxs-lookup"><span data-stu-id="4fcba-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcba-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fcba-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="4fcba-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fcba-109">Property value</span></span>

<span data-ttu-id="4fcba-110">Время повторения шаблона.</span><span class="sxs-lookup"><span data-stu-id="4fcba-110">How long the pattern is repeated.</span></span> <span data-ttu-id="4fcba-111">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="4fcba-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="4fcba-112">Минимальное допустимое время — одна минута.</span><span class="sxs-lookup"><span data-stu-id="4fcba-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="4fcba-113">Если для длительности не указано значение, шаблон повторяется бесконечно.</span><span class="sxs-lookup"><span data-stu-id="4fcba-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fcba-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4fcba-114">Remarks</span></span>

<span data-ttu-id="4fcba-115">Если для задачи задана длительность повторения, необходимо также указать интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="4fcba-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="4fcba-116">При чтении или записи XML для задачи длительность повтора указывается в элементе [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="4fcba-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fcba-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4fcba-117">Requirements</span></span>



| <span data-ttu-id="4fcba-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4fcba-118">Requirement</span></span> | <span data-ttu-id="4fcba-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4fcba-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcba-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fcba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4fcba-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fcba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4fcba-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fcba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4fcba-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4fcba-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fcba-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4fcba-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fcba-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fcba-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fcba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4fcba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fcba-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fcba-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fcba-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fcba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcba-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4fcba-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





