---
title: Сообщение DTM_GETMONTHCAL (Коммктрл. h)
description: Возвращает маркер для элемента управления "Календарь дочернего месяца выбора даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Жетмонскал DateTime.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Элементы управления Windows для DTM_GETMONTHCAL сообщений
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989018"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="9f2a3-105">\_Сообщение DTM жетмонскал</span><span class="sxs-lookup"><span data-stu-id="9f2a3-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="9f2a3-106">Возвращает маркер для элемента управления "Календарь дочернего месяца выбора даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="9f2a3-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="9f2a3-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетмонскал DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .</span><span class="sxs-lookup"><span data-stu-id="9f2a3-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f2a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f2a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f2a3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9f2a3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9f2a3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9f2a3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f2a3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f2a3-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9f2a3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2a3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f2a3-113">Return value</span></span>

<span data-ttu-id="9f2a3-114">Возвращает маркер для элемента управления "Календарь дочернего месяца" элемента управления DTP, если он успешно, или **null** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9f2a3-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2a3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f2a3-115">Remarks</span></span>

<span data-ttu-id="9f2a3-116">Элементы управления DTP создают элемент управления "Календарь на дочернем месяце", когда пользователь щелкает стрелку раскрывающегося[ \_ списка](dtn-dropdown.md) (всплывающее уведомление ДТН).</span><span class="sxs-lookup"><span data-stu-id="9f2a3-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="9f2a3-117">Если месячный календарь больше не нужен, он уничтожается (уведомление [ДТН \_ крупный план](dtn-closeup.md) отправляется при уничтожении).</span><span class="sxs-lookup"><span data-stu-id="9f2a3-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="9f2a3-118">Поэтому ваше приложение не должно полагаться на статический маркер для дочернего месяца элемента управления DTP.</span><span class="sxs-lookup"><span data-stu-id="9f2a3-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2a3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9f2a3-119">Requirements</span></span>



| <span data-ttu-id="9f2a3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9f2a3-120">Requirement</span></span> | <span data-ttu-id="9f2a3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9f2a3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2a3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f2a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2a3-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f2a3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f2a3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f2a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2a3-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f2a3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f2a3-126">Header</span><span class="sxs-lookup"><span data-stu-id="9f2a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f2a3-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2a3-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2a3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f2a3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f2a3-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9f2a3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f2a3-130">ДТН \_ крупный план</span><span class="sxs-lookup"><span data-stu-id="9f2a3-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="9f2a3-131">\_раскрывающийся список ДТН</span><span class="sxs-lookup"><span data-stu-id="9f2a3-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





