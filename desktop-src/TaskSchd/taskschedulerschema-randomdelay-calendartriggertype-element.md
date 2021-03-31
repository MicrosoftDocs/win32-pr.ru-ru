---
title: Рандомделай (Календартригжертипе), элемент
description: Содержит время задержки, которое случайным образом добавляется к времени начала триггера. | Рандомделай (Календартригжертипе), элемент
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
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
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353382"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="53e01-105">Рандомделай (Календартригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="53e01-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="53e01-106">Содержит время задержки, которое случайным образом добавляется к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="53e01-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="53e01-107">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="53e01-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="53e01-108">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="53e01-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="53e01-109">Элемент **рандомделай** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="53e01-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="53e01-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="53e01-110">Parent element</span></span>



| <span data-ttu-id="53e01-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="53e01-111">Element</span></span>                                                                                            | <span data-ttu-id="53e01-112">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="53e01-112">Derived from</span></span>                                                                       | <span data-ttu-id="53e01-113">Описание</span><span class="sxs-lookup"><span data-stu-id="53e01-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53e01-114">**Календартригжер (Тригжерграуп)**</span><span class="sxs-lookup"><span data-stu-id="53e01-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="53e01-115">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="53e01-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="53e01-116">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="53e01-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="53e01-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53e01-117">Requirements</span></span>



| <span data-ttu-id="53e01-118">Требование</span><span class="sxs-lookup"><span data-stu-id="53e01-118">Requirement</span></span> | <span data-ttu-id="53e01-119">Значение</span><span class="sxs-lookup"><span data-stu-id="53e01-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53e01-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53e01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="53e01-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53e01-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53e01-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53e01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="53e01-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53e01-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





