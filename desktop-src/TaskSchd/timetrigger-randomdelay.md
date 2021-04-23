---
title: Тиметригжер. Рандомделай, свойство
description: Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера. | Тиметригжер. Рандомделай, свойство
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- планировщик задач свойства Рандомделай
- Планировщик задач свойства Рандомделай, объект Тиметригжер
- Планировщик задач объекта Тиметригжер, свойство Рандомделай
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674612"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="7aaf7-107">Тиметригжер. Рандомделай, свойство</span><span class="sxs-lookup"><span data-stu-id="7aaf7-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="7aaf7-108">Для создания скриптов Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aaf7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7aaf7-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="7aaf7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7aaf7-110">Property value</span></span>

<span data-ttu-id="7aaf7-111">Время задержки, которое случайным образом добавляется к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="7aaf7-112">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="7aaf7-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="7aaf7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7aaf7-113">Requirements</span></span>



| <span data-ttu-id="7aaf7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7aaf7-114">Requirement</span></span> | <span data-ttu-id="7aaf7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7aaf7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aaf7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7aaf7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7aaf7-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7aaf7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7aaf7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7aaf7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7aaf7-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7aaf7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7aaf7-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7aaf7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="7aaf7-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7aaf7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7aaf7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aaf7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





