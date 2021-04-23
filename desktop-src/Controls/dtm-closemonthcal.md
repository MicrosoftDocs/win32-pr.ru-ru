---
title: Сообщение DTM_CLOSEMONTHCAL (Коммктрл. h)
description: Закрывает элемент управления "Выбор даты и времени" (DTP). Отправляйте это сообщение явным образом или с помощью \_ макроса DateTime клосемонскал.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Элементы управления Windows для DTM_CLOSEMONTHCAL сообщений
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071202"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="ca05c-105">\_Сообщение DTM клосемонскал</span><span class="sxs-lookup"><span data-stu-id="ca05c-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="ca05c-106">Закрывает элемент управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="ca05c-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="ca05c-107">Отправляйте это сообщение явным образом или с помощью макроса [**DateTime \_ клосемонскал**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .</span><span class="sxs-lookup"><span data-stu-id="ca05c-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca05c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca05c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca05c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca05c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca05c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ca05c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca05c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca05c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca05c-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ca05c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca05c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca05c-113">Return value</span></span>

<span data-ttu-id="ca05c-114">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ca05c-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca05c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca05c-115">Remarks</span></span>

<span data-ttu-id="ca05c-116">Уничтожает элемент управления и отправляет уведомление [ДТН \_ крупный план](dtn-closeup.md) о том, что элемент управления закрывается (в отличие от раскрывающегося уведомления [ДТН \_ ](dtn-dropdown.md) ) к родителю элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ca05c-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca05c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ca05c-117">Requirements</span></span>



| <span data-ttu-id="ca05c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ca05c-118">Requirement</span></span> | <span data-ttu-id="ca05c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ca05c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca05c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca05c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca05c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca05c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca05c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca05c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca05c-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca05c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca05c-124">Header</span><span class="sxs-lookup"><span data-stu-id="ca05c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca05c-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca05c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca05c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca05c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca05c-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ca05c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ca05c-128">\_раскрывающийся список ДТН</span><span class="sxs-lookup"><span data-stu-id="ca05c-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="ca05c-129">ДТН \_ крупный план</span><span class="sxs-lookup"><span data-stu-id="ca05c-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





