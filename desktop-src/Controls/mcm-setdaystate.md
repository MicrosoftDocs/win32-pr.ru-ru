---
title: Сообщение MCM_SETDAYSTATE (Коммктрл. h)
description: Устанавливает дни недели для всех месяцев, которые в настоящее время видны в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетдайстате.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Элементы управления Windows для MCM_SETDAYSTATE сообщений
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492849"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="41ecc-105">\_Сообщение MCM сетдайстате</span><span class="sxs-lookup"><span data-stu-id="41ecc-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="41ecc-106">Устанавливает дни недели для всех месяцев, которые в настоящее время видны в элементе управления ' календарь на месяц '.</span><span class="sxs-lookup"><span data-stu-id="41ecc-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="41ecc-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетдайстате**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .</span><span class="sxs-lookup"><span data-stu-id="41ecc-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41ecc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41ecc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ecc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41ecc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41ecc-110">Значение, указывающее, сколько элементов находится в массиве, на который указывает *lParam* .</span><span class="sxs-lookup"><span data-stu-id="41ecc-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="41ecc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41ecc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41ecc-112">Указатель на массив значений [**монсдайстате**](monthdaystate.md) , определяющих, как элемент управления "календарь месяца" будет рисовать каждый день в своем дисплее.</span><span class="sxs-lookup"><span data-stu-id="41ecc-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ecc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41ecc-113">Return value</span></span>

<span data-ttu-id="41ecc-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="41ecc-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ecc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41ecc-115">Remarks</span></span>

<span data-ttu-id="41ecc-116">Приложение может явно задать сведения о состоянии дня, отправив это сообщение, но состояние не будет сохраняться при прокрутке другой части календаря на представление.</span><span class="sxs-lookup"><span data-stu-id="41ecc-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="41ecc-117">Сведения о состоянии дня обычно задаются в ответ на код уведомления [МКН \_ жетдайстате](mcn-getdaystate.md) , который отправляется каждый раз, когда необходимо обновить элемент управления.</span><span class="sxs-lookup"><span data-stu-id="41ecc-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="41ecc-118">Массив в параметре *lParam* должен содержать столько элементов, сколько имеет значение, возвращаемое следующим макросом:</span><span class="sxs-lookup"><span data-stu-id="41ecc-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="41ecc-119">Помните, что массив в параметре *lParam* должен содержать значения [**монсдайстате**](monthdaystate.md) , которые соответствуют всем месяцам, которые в настоящее время отображаются в элементе управления, в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="41ecc-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="41ecc-120">Сюда входят два месяца, которые могут быть частично отображены до первого месяца и после последнего месяца.</span><span class="sxs-lookup"><span data-stu-id="41ecc-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ecc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="41ecc-121">Requirements</span></span>



| <span data-ttu-id="41ecc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="41ecc-122">Requirement</span></span> | <span data-ttu-id="41ecc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="41ecc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41ecc-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41ecc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41ecc-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41ecc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41ecc-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41ecc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41ecc-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41ecc-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41ecc-128">Header</span><span class="sxs-lookup"><span data-stu-id="41ecc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41ecc-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="41ecc-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ecc-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41ecc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ecc-131">Использование элементов управления "календарь месяца"</span><span class="sxs-lookup"><span data-stu-id="41ecc-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





