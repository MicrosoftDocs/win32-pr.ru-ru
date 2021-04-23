---
description: Не рекомендуется. Указывает единицы даты для настройки структуры КАЛДАТЕТИМЕ.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: Перечисление CALDATETIME_DATEUNIT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682634"
---
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="6886d-104">\_Перечисление ДАТЕУНИТ калдатетиме</span><span class="sxs-lookup"><span data-stu-id="6886d-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="6886d-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6886d-105">Deprecated.</span></span> <span data-ttu-id="6886d-106">Указывает единицы даты для настройки структуры [**калдатетиме**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="6886d-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6886d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6886d-107">Syntax</span></span>


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a><span data-ttu-id="6886d-108">Константы</span><span class="sxs-lookup"><span data-stu-id="6886d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6886d-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**ераунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-110">Единица времени эры даты.</span><span class="sxs-lookup"><span data-stu-id="6886d-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**еарунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-112">Единица измерения даты и времени года.</span><span class="sxs-lookup"><span data-stu-id="6886d-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**монсунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-114">Единица времени месяца даты.</span><span class="sxs-lookup"><span data-stu-id="6886d-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**викунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-116">Единица времени для даты недели.</span><span class="sxs-lookup"><span data-stu-id="6886d-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**дайунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-118">Единица времени дня и даты.</span><span class="sxs-lookup"><span data-stu-id="6886d-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**хаурунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-120">Единица времени часового периода.</span><span class="sxs-lookup"><span data-stu-id="6886d-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**минутеунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-122">Единица времени в виде минуты.</span><span class="sxs-lookup"><span data-stu-id="6886d-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**секондунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-124">Вторая единица времени даты.</span><span class="sxs-lookup"><span data-stu-id="6886d-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="6886d-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**тиккунит**</span><span class="sxs-lookup"><span data-stu-id="6886d-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="6886d-126">Единица времени даты Tick.</span><span class="sxs-lookup"><span data-stu-id="6886d-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6886d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6886d-127">Requirements</span></span>



| <span data-ttu-id="6886d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6886d-128">Requirement</span></span> | <span data-ttu-id="6886d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6886d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6886d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6886d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6886d-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6886d-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6886d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6886d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6886d-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6886d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6886d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6886d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6886d-135">Типы перечисления поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="6886d-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




