---
title: Элемент Delay (Логонтригжертипе)
description: Промежуток времени между входом пользователя в систему и запуском задачи.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492795"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="54b73-104">Элемент Delay (Логонтригжертипе)</span><span class="sxs-lookup"><span data-stu-id="54b73-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="54b73-105">Промежуток времени между входом пользователя в систему и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="54b73-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="54b73-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="54b73-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="54b73-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="54b73-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="54b73-108">Элемент **delay** определяется сложным типом [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54b73-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="54b73-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="54b73-109">Parent element</span></span>



| <span data-ttu-id="54b73-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="54b73-110">Element</span></span>                                                                       | <span data-ttu-id="54b73-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="54b73-111">Derived from</span></span>                                                                 | <span data-ttu-id="54b73-112">Описание</span><span class="sxs-lookup"><span data-stu-id="54b73-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="54b73-113">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="54b73-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="54b73-114">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="54b73-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="54b73-115">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="54b73-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="54b73-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54b73-116">Remarks</span></span>

<span data-ttu-id="54b73-117">Для разработки сценариев задержка триггера входа указывается с помощью свойства [**логонтригжер. Delay**](logontrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="54b73-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="54b73-118">Для разработки на C++ идентификатор пользователя для триггера LOGON указывается с помощью свойства [**илогонтригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="54b73-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b73-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54b73-119">Requirements</span></span>



| <span data-ttu-id="54b73-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54b73-120">Requirement</span></span> | <span data-ttu-id="54b73-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54b73-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54b73-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54b73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54b73-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54b73-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54b73-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54b73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54b73-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54b73-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54b73-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54b73-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b73-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="54b73-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="54b73-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="54b73-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





