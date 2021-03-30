---
title: Сообщение MCM_GETRANGE (Коммктрл. h)
description: Возвращает минимальную и максимальную допустимые даты, заданные для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Элементы управления Windows для MCM_GETRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892638"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="edd70-105">Сообщение MCMного \_ диапазона</span><span class="sxs-lookup"><span data-stu-id="edd70-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="edd70-106">Возвращает минимальную и максимальную допустимые даты, заданные для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="edd70-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="edd70-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .</span><span class="sxs-lookup"><span data-stu-id="edd70-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="edd70-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edd70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd70-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edd70-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edd70-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="edd70-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="edd70-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edd70-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edd70-112">Указатель на массив элементов [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами, который получит сведения о предельной дате.</span><span class="sxs-lookup"><span data-stu-id="edd70-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="edd70-113">Минимальный предел задается в *лпргсистимеаррай* \[ 0 \] , а *лпргсистимеаррай* \[ 1 — \] максимально допустимое.</span><span class="sxs-lookup"><span data-stu-id="edd70-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="edd70-114">Если для любого из элементов задано значение все нули, то для элемента управления "месячный календарь" не будет установлен соответствующий предел.</span><span class="sxs-lookup"><span data-stu-id="edd70-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="edd70-115">Этот параметр должен быть допустимым адресом и не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="edd70-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd70-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edd70-116">Return value</span></span>

<span data-ttu-id="edd70-117">Возвращает **DWORD** , который может быть равен нулю (ограничения не заданы) или сочетание следующих значений, задающих сведения об ограничении:</span><span class="sxs-lookup"><span data-stu-id="edd70-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="edd70-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="edd70-118">Return code</span></span>                                                                              | <span data-ttu-id="edd70-119">Описание</span><span class="sxs-lookup"><span data-stu-id="edd70-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="edd70-120"><dt>**ГДТР \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="edd70-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="edd70-121">Для элемента управления задано ограничение максимального значения; *лпргсистимеаррай* \[ 0 \] является допустимым и содержит применимые сведения о датах.</span><span class="sxs-lookup"><span data-stu-id="edd70-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="edd70-122"><dt>**ГДТР \_ мин**</dt></span><span class="sxs-lookup"><span data-stu-id="edd70-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="edd70-123">Для элемента управления задано минимальное ограничение; *лпргсистимеаррай* \[ 1 \] является допустимым и содержит применимые сведения о датах.</span><span class="sxs-lookup"><span data-stu-id="edd70-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="edd70-124">Требования</span><span class="sxs-lookup"><span data-stu-id="edd70-124">Requirements</span></span>



| <span data-ttu-id="edd70-125">Требование</span><span class="sxs-lookup"><span data-stu-id="edd70-125">Requirement</span></span> | <span data-ttu-id="edd70-126">Значение</span><span class="sxs-lookup"><span data-stu-id="edd70-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edd70-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edd70-127">Minimum supported client</span></span><br/> | <span data-ttu-id="edd70-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edd70-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edd70-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edd70-129">Minimum supported server</span></span><br/> | <span data-ttu-id="edd70-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edd70-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edd70-131">Header</span><span class="sxs-lookup"><span data-stu-id="edd70-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd70-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="edd70-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd70-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edd70-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd70-134">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="edd70-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

