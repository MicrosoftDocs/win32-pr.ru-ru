---
title: Сообщение MCM_SETTODAY (Коммктрл. h)
description: Задает \ 0034; сегодня \ 0034; Выбор элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеттодай.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Элементы управления Windows для MCM_SETTODAY сообщений
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804012"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="7adfd-105">\_Сообщение MCM сеттодай</span><span class="sxs-lookup"><span data-stu-id="7adfd-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="7adfd-106">Задает параметр "сегодня" для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="7adfd-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="7adfd-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеттодай**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .</span><span class="sxs-lookup"><span data-stu-id="7adfd-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7adfd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7adfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adfd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7adfd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7adfd-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7adfd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7adfd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7adfd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7adfd-112">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , содержащую дату, которая должна быть выбрана для элемента управления "сегодня".</span><span class="sxs-lookup"><span data-stu-id="7adfd-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="7adfd-113">Если этот параметр имеет значение **null**, элемент управления возвращается к значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7adfd-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adfd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7adfd-114">Return value</span></span>

<span data-ttu-id="7adfd-115">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="7adfd-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7adfd-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7adfd-116">Remarks</span></span>

<span data-ttu-id="7adfd-117">Если для параметра «сегодня» выбрана любая дата, отличная от значения по умолчанию, применяются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="7adfd-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="7adfd-118">Элемент управления не будет автоматически обновлять выбор "сегодня", когда время прошло полночь текущего дня.</span><span class="sxs-lookup"><span data-stu-id="7adfd-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="7adfd-119">Элемент управления не будет автоматически обновляться на основе изменений языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="7adfd-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adfd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7adfd-120">Requirements</span></span>



| <span data-ttu-id="7adfd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7adfd-121">Requirement</span></span> | <span data-ttu-id="7adfd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7adfd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7adfd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7adfd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7adfd-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7adfd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7adfd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7adfd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7adfd-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7adfd-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7adfd-127">Header</span><span class="sxs-lookup"><span data-stu-id="7adfd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adfd-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7adfd-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adfd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7adfd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adfd-130">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="7adfd-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

