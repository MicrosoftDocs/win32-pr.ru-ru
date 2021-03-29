---
title: Сообщение MCM_GETSELRANGE (Коммктрл. h)
description: Извлекает сведения о датах, представляющие верхний и нижний пределы диапазона дат, выбранного пользователем в текущий момент. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетселранже.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Элементы управления Windows для MCM_GETSELRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988478"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="b0383-105">\_Сообщение MCM жетселранже</span><span class="sxs-lookup"><span data-stu-id="b0383-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="b0383-106">Извлекает сведения о датах, представляющие верхний и нижний пределы диапазона дат, выбранного пользователем в текущий момент.</span><span class="sxs-lookup"><span data-stu-id="b0383-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="b0383-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетселранже**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .</span><span class="sxs-lookup"><span data-stu-id="b0383-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0383-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0383-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0383-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0383-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b0383-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b0383-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b0383-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0383-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0383-112">Указатель на массив структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами, который будет принимать нижнюю и верхнюю границы выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0383-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="b0383-113">Нижний и верхний пределы помещаются в *лпргсистимеаррай* \[ 0 \] и *лпргсистимеаррай* \[ 1 \] соответственно.</span><span class="sxs-lookup"><span data-stu-id="b0383-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="b0383-114">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0383-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0383-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0383-115">Return value</span></span>

<span data-ttu-id="b0383-116">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b0383-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="b0383-117">**MCM \_ ЖЕТСЕЛРАНЖЕ** не будет работать, если применяется к элементу управления "месячный календарь", который не использует многоэлементный стиль [**MCS \_**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b0383-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0383-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b0383-118">Requirements</span></span>



| <span data-ttu-id="b0383-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b0383-119">Requirement</span></span> | <span data-ttu-id="b0383-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b0383-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0383-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0383-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b0383-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0383-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0383-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0383-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b0383-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0383-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0383-125">Header</span><span class="sxs-lookup"><span data-stu-id="b0383-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0383-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0383-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0383-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0383-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0383-128">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="b0383-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

