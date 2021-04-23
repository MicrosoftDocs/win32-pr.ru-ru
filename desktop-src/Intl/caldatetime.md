---
description: Не рекомендуется. Представляет мгновенное время, обычно выраженное как Дата и время суток, и соответствующий календарь.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Структура КАЛДАТЕТИМЕ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684681"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="69b67-104">Структура КАЛДАТЕТИМЕ</span><span class="sxs-lookup"><span data-stu-id="69b67-104">CALDATETIME structure</span></span>

<span data-ttu-id="69b67-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="69b67-105">Deprecated.</span></span> <span data-ttu-id="69b67-106">Представляет мгновенное время, обычно выраженное как Дата и время суток, и соответствующий календарь.</span><span class="sxs-lookup"><span data-stu-id="69b67-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b67-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69b67-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="69b67-108">Члены</span><span class="sxs-lookup"><span data-stu-id="69b67-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69b67-109">**калид**</span><span class="sxs-lookup"><span data-stu-id="69b67-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-110">[Идентификатор календаря](calendar-identifiers.md) для мгновенного выполнения.</span><span class="sxs-lookup"><span data-stu-id="69b67-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-111">**Нашей**</span><span class="sxs-lookup"><span data-stu-id="69b67-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-112">Сведения о эре за текущий момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-113">**Год**</span><span class="sxs-lookup"><span data-stu-id="69b67-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-114">Год на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-115">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="69b67-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-116">Месяц на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-117">**День**</span><span class="sxs-lookup"><span data-stu-id="69b67-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-118">День на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="69b67-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-120">День недели для мгновенного выполнения.</span><span class="sxs-lookup"><span data-stu-id="69b67-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-121">**Час**</span><span class="sxs-lookup"><span data-stu-id="69b67-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-122">Час на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-123">**Интервал**</span><span class="sxs-lookup"><span data-stu-id="69b67-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-124">Минута на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-125">**Секунды**</span><span class="sxs-lookup"><span data-stu-id="69b67-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-126">Второй для мгновенного выполнения.</span><span class="sxs-lookup"><span data-stu-id="69b67-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="69b67-127">**Импульс**</span><span class="sxs-lookup"><span data-stu-id="69b67-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="69b67-128">Такт на момент времени.</span><span class="sxs-lookup"><span data-stu-id="69b67-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69b67-129">Требования</span><span class="sxs-lookup"><span data-stu-id="69b67-129">Requirements</span></span>



| <span data-ttu-id="69b67-130">Требование</span><span class="sxs-lookup"><span data-stu-id="69b67-130">Requirement</span></span> | <span data-ttu-id="69b67-131">Значение</span><span class="sxs-lookup"><span data-stu-id="69b67-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69b67-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69b67-132">Minimum supported client</span></span><br/> | <span data-ttu-id="69b67-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69b67-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69b67-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69b67-134">Minimum supported server</span></span><br/> | <span data-ttu-id="69b67-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69b67-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69b67-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69b67-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b67-137">Структуры поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="69b67-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




