---
title: Элемент Delay (Сессионстатечанжетригжертипе)
description: Содержит значение, указывающее длину задержки для времени начала задачи при обнаружении изменения состояния сеанса сервера терминалов.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
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
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137698"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="577d5-104">Элемент Delay (Сессионстатечанжетригжертипе)</span><span class="sxs-lookup"><span data-stu-id="577d5-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="577d5-105">Содержит значение, указывающее длину задержки для времени начала задачи при обнаружении изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="577d5-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="577d5-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="577d5-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="577d5-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="577d5-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="577d5-108">Элемент **delay** определяется сложным типом [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="577d5-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="577d5-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="577d5-109">Parent element</span></span>



| <span data-ttu-id="577d5-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="577d5-110">Element</span></span>                       | <span data-ttu-id="577d5-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="577d5-111">Derived from</span></span>                                                                                           | <span data-ttu-id="577d5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="577d5-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577d5-113">**сессионстатечанжетригжер**</span><span class="sxs-lookup"><span data-stu-id="577d5-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="577d5-114">**сессионстатечанжетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="577d5-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="577d5-115">Указывает триггер, который запускает задачу при изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="577d5-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="577d5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="577d5-116">Remarks</span></span>

<span data-ttu-id="577d5-117">Для разработки сценариев задержка триггера изменения состояния сеанса указывается с помощью свойства [**сессионстатечанжетригжер. Delay**](sessionstatechangetrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="577d5-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="577d5-118">Для разработки на C++ задержка триггера изменения состояния сеанса указывается с помощью [**свойства Delay объекта исессионстатечанжетригжер**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span><span class="sxs-lookup"><span data-stu-id="577d5-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="577d5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="577d5-119">Requirements</span></span>



| <span data-ttu-id="577d5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="577d5-120">Requirement</span></span> | <span data-ttu-id="577d5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="577d5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="577d5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="577d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="577d5-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="577d5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="577d5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="577d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="577d5-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="577d5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





