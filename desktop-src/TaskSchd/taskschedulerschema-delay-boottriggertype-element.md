---
title: Элемент Delay (Буттригжертипе)
description: Указывает промежуток времени между загрузкой системы и началом задачи.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
keywords:
- планировщик задач элемента Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989392"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="96e99-104">Элемент Delay (Буттригжертипе)</span><span class="sxs-lookup"><span data-stu-id="96e99-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="96e99-105">Указывает промежуток времени между загрузкой системы и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="96e99-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="96e99-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="96e99-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="96e99-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="96e99-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="96e99-108">Элемент **delay** определяется сложным типом [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="96e99-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="96e99-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="96e99-109">Parent element</span></span>



| <span data-ttu-id="96e99-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="96e99-110">Element</span></span>                                                                     | <span data-ttu-id="96e99-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="96e99-111">Derived from</span></span>                                                               | <span data-ttu-id="96e99-112">Описание</span><span class="sxs-lookup"><span data-stu-id="96e99-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="96e99-113">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="96e99-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="96e99-114">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="96e99-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="96e99-115">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="96e99-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96e99-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96e99-116">Remarks</span></span>

<span data-ttu-id="96e99-117">Для разработки скриптов задержка триггера события задается свойством [**буттригжер. Delay**](boottrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="96e99-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="96e99-118">Для разработки на C++ задержка триггера события задается свойством [**ибуттригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="96e99-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e99-119">Требования</span><span class="sxs-lookup"><span data-stu-id="96e99-119">Requirements</span></span>



| <span data-ttu-id="96e99-120">Требование</span><span class="sxs-lookup"><span data-stu-id="96e99-120">Requirement</span></span> | <span data-ttu-id="96e99-121">Значение</span><span class="sxs-lookup"><span data-stu-id="96e99-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96e99-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96e99-122">Minimum supported client</span></span><br/> | <span data-ttu-id="96e99-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96e99-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96e99-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96e99-124">Minimum supported server</span></span><br/> | <span data-ttu-id="96e99-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96e99-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96e99-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96e99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e99-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="96e99-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="96e99-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="96e99-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





