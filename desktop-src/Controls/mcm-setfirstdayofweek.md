---
title: Сообщение MCM_SETFIRSTDAYOFWEEK (Коммктрл. h)
description: Задает первый день недели для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетфирстдайофвик.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Элементы управления Windows для MCM_SETFIRSTDAYOFWEEK сообщений
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654688"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="5cccb-105">\_Сообщение MCM сетфирстдайофвик</span><span class="sxs-lookup"><span data-stu-id="5cccb-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="5cccb-106">Задает первый день недели для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="5cccb-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="5cccb-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетфирстдайофвик**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="5cccb-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cccb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cccb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cccb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cccb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5cccb-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5cccb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5cccb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cccb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cccb-112">Значение типа **int** , представляющее день, который должен быть установлен в качестве первого дня недели, где 0 — понедельник, 1 — вторник и т. д.</span><span class="sxs-lookup"><span data-stu-id="5cccb-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cccb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cccb-113">Return value</span></span>

<span data-ttu-id="5cccb-114">Возвращает значение **типа DWORD** , содержащее два значения.</span><span class="sxs-lookup"><span data-stu-id="5cccb-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="5cccb-115">Верхнее слово — это **логическое** значение, отличное от нуля, если предыдущий первый день недели не РАВЕН ифирстдайофвик локали \_ или если в противном случае ноль.</span><span class="sxs-lookup"><span data-stu-id="5cccb-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="5cccb-116">Младшее слово — это значение INT, представляющее предыдущий первый день недели.</span><span class="sxs-lookup"><span data-stu-id="5cccb-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cccb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cccb-117">Remarks</span></span>

<span data-ttu-id="5cccb-118">Если для первого дня недели задано значение, отличное от значения по умолчанию (LOCALE \_ ифирстдайофвик), то элемент управления не будет автоматически обновляться в первый день на основе изменений языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="5cccb-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cccb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5cccb-119">Requirements</span></span>



| <span data-ttu-id="5cccb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5cccb-120">Requirement</span></span> | <span data-ttu-id="5cccb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5cccb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cccb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cccb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5cccb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cccb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cccb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cccb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5cccb-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5cccb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cccb-126">Header</span><span class="sxs-lookup"><span data-stu-id="5cccb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cccb-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cccb-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





