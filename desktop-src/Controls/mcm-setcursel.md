---
title: Сообщение MCM_SETCURSEL (Коммктрл. h)
description: Задает текущую выбранную дату для элемента управления "месячный календарь". Если указанная дата не находится в представлении, элемент управления обновляет отображение, чтобы отобразить его в представлении. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткурсел.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Элементы управления Windows для MCM_SETCURSEL сообщений
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654690"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="3f752-106">\_Сообщение MCM сеткурсел</span><span class="sxs-lookup"><span data-stu-id="3f752-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="3f752-107">Задает текущую выбранную дату для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="3f752-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="3f752-108">Если указанная дата не находится в представлении, элемент управления обновляет отображение, чтобы отобразить его в представлении.</span><span class="sxs-lookup"><span data-stu-id="3f752-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="3f752-109">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткурсел**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="3f752-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f752-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f752-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f752-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f752-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3f752-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3f752-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3f752-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f752-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f752-114">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , содержащую дату, которая должна быть выбрана в качестве текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="3f752-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f752-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f752-115">Return value</span></span>

<span data-ttu-id="3f752-116">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f752-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="3f752-117">Это сообщение не будет выполнено, если применяется к элементу управления "месячный календарь", который использует многоэлементный стиль [**MCS \_**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3f752-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f752-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3f752-118">Requirements</span></span>



| <span data-ttu-id="3f752-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3f752-119">Requirement</span></span> | <span data-ttu-id="3f752-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3f752-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f752-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f752-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3f752-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f752-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f752-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f752-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3f752-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f752-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f752-125">Header</span><span class="sxs-lookup"><span data-stu-id="3f752-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f752-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f752-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f752-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f752-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f752-128">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="3f752-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

