---
title: Элемент Delay (Регистратионтригжертипе)
description: Указывает промежуток времени между регистрацией задачи и началом задачи.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803983"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="dd097-104">Элемент Delay (Регистратионтригжертипе)</span><span class="sxs-lookup"><span data-stu-id="dd097-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="dd097-105">Указывает промежуток времени между регистрацией задачи и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="dd097-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="dd097-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="dd097-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="dd097-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="dd097-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="dd097-108">Элемент **delay** определяется сложным типом [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dd097-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dd097-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="dd097-109">Parent element</span></span>



| <span data-ttu-id="dd097-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="dd097-110">Element</span></span>                                                                                     | <span data-ttu-id="dd097-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="dd097-111">Derived from</span></span>                                                                               | <span data-ttu-id="dd097-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dd097-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="dd097-113">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="dd097-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="dd097-114">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="dd097-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="dd097-115">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="dd097-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dd097-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd097-116">Remarks</span></span>

<span data-ttu-id="dd097-117">Для разработки сценариев задержка триггера регистрации указывается с помощью свойства [**регистратионтригжер. Delay**](registrationtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="dd097-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="dd097-118">Для разработки на C++ задержка триггера регистрации указывается с помощью свойства [**ирегистратионтригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="dd097-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="dd097-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd097-119">Examples</span></span>

<span data-ttu-id="dd097-120">Следующий XML-код определяет задержку триггера регистрации, которая допускает задержку в 5 минут между регистрацией задачи и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="dd097-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="dd097-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dd097-121">Requirements</span></span>



| <span data-ttu-id="dd097-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dd097-122">Requirement</span></span> | <span data-ttu-id="dd097-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dd097-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd097-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd097-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd097-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd097-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd097-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd097-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd097-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd097-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd097-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd097-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd097-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="dd097-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dd097-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="dd097-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





