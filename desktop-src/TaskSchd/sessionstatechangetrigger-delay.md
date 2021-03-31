---
title: Сессионстатечанжетригжер. Delay, свойство
description: Для создания скриптов Возвращает или задает значение, которое указывает, как долго происходит задержка перед запуском задачи после обнаружения изменения состояния сеанса сервера терминалов.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- планировщик задач свойства Delay
- Свойство Delay планировщик задач, объект Сессионстатечанжетригжер
- Планировщик задач объекта Сессионстатечанжетригжер, свойство Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135423"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="4fafe-106">Сессионстатечанжетригжер. Delay, свойство</span><span class="sxs-lookup"><span data-stu-id="4fafe-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="4fafe-107">Для создания скриптов Возвращает или задает значение, которое указывает, как долго происходит задержка перед запуском задачи после обнаружения изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="4fafe-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="4fafe-108">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="4fafe-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fafe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fafe-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="4fafe-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4fafe-110">Property value</span></span>

<span data-ttu-id="4fafe-111">Задержка, выполняемая перед запуском задачи после обнаружения изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="4fafe-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fafe-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4fafe-112">Requirements</span></span>



| <span data-ttu-id="4fafe-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4fafe-113">Requirement</span></span> | <span data-ttu-id="4fafe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafe-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fafe-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fafe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4fafe-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fafe-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4fafe-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fafe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4fafe-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4fafe-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fafe-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4fafe-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fafe-120"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fafe-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fafe-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4fafe-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fafe-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fafe-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





