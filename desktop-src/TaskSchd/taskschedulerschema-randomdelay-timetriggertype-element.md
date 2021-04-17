---
title: Рандомделай (Тиметригжертипе), элемент
description: Содержит время задержки, которое случайным образом добавляется к времени начала триггера. | Рандомделай (Тиметригжертипе), элемент
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- планировщик задач элемента Рандомделай
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674637"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="131fa-105">Рандомделай (Тиметригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="131fa-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="131fa-106">Содержит время задержки, которое случайным образом добавляется к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="131fa-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="131fa-107">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="131fa-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="131fa-108">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="131fa-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="131fa-109">Элемент определяется сложным типом [**тиметригжертипе**](taskschedulerschema-timetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="131fa-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="131fa-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="131fa-110">Parent element</span></span>



| <span data-ttu-id="131fa-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="131fa-111">Element</span></span>                                                                                    | <span data-ttu-id="131fa-112">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="131fa-112">Derived from</span></span>                                                               | <span data-ttu-id="131fa-113">Описание</span><span class="sxs-lookup"><span data-stu-id="131fa-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="131fa-114">**Тиметригжер (Тригжерграуп)**</span><span class="sxs-lookup"><span data-stu-id="131fa-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="131fa-115">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="131fa-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="131fa-116">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="131fa-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="131fa-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="131fa-117">Remarks</span></span>

<span data-ttu-id="131fa-118">Сведения о разработке на языке C++ см. в разделе [**свойство рандомделай объекта итиметригжер**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span><span class="sxs-lookup"><span data-stu-id="131fa-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="131fa-119">Сведения о разработке сценариев см. в разделе [**тиметригжер. рандомделай**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="131fa-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="131fa-120">Требования</span><span class="sxs-lookup"><span data-stu-id="131fa-120">Requirements</span></span>



| <span data-ttu-id="131fa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="131fa-121">Requirement</span></span> | <span data-ttu-id="131fa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="131fa-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="131fa-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="131fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="131fa-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="131fa-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="131fa-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="131fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="131fa-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="131fa-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





