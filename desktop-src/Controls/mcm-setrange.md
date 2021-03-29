---
title: Сообщение MCM_SETRANGE (Коммктрл. h)
description: Задает минимальную и максимальную допустимые даты для элемента управления "месячный календарь". Это сообщение можно отправить явно или с помощью \_ макроса монскал SetRange.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Элементы управления Windows для MCM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654640"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="63706-105">\_Сообщение SETRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="63706-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="63706-106">Задает минимальную и максимальную допустимые даты для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="63706-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="63706-107">Это сообщение можно отправить явно или с помощью макроса [**монскал \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .</span><span class="sxs-lookup"><span data-stu-id="63706-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63706-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63706-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63706-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63706-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63706-110">Значения флагов, указывающие, какие ограничения дат задаются.</span><span class="sxs-lookup"><span data-stu-id="63706-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="63706-111">Это значение должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="63706-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="63706-112">Значение</span><span class="sxs-lookup"><span data-stu-id="63706-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="63706-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63706-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="63706-114"><dt>**ГДТР \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="63706-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="63706-115">Устанавливается максимально допустимая дата.</span><span class="sxs-lookup"><span data-stu-id="63706-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="63706-116">Структура [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) в *лпсистимеаррай* \[ 1 \] должна содержать сведения о датах.</span><span class="sxs-lookup"><span data-stu-id="63706-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="63706-117"><dt>**ГДТР \_ мин**</dt></span><span class="sxs-lookup"><span data-stu-id="63706-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="63706-118">Устанавливается минимальная допустимая дата.</span><span class="sxs-lookup"><span data-stu-id="63706-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="63706-119">Структура [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) в *лпсистимеаррай* \[ 0 \] должна содержать сведения о датах.</span><span class="sxs-lookup"><span data-stu-id="63706-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="63706-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63706-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63706-121">Указатель на массив, сокоторый из двух элементов, содержит структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , которые содержат ограничения по датам.</span><span class="sxs-lookup"><span data-stu-id="63706-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="63706-122">Максимальный предел должен быть в *лпсистимеаррай* \[ 1 \] , если указан параметр Гдтр \_ Max, а *лпсистимеаррай* \[ 0 \] должен содержать минимальное ограничение, если \_ задано значение гдтр min.</span><span class="sxs-lookup"><span data-stu-id="63706-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63706-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63706-123">Return value</span></span>

<span data-ttu-id="63706-124">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="63706-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63706-125">Требования</span><span class="sxs-lookup"><span data-stu-id="63706-125">Requirements</span></span>



| <span data-ttu-id="63706-126">Требование</span><span class="sxs-lookup"><span data-stu-id="63706-126">Requirement</span></span> | <span data-ttu-id="63706-127">Значение</span><span class="sxs-lookup"><span data-stu-id="63706-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63706-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63706-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63706-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63706-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63706-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63706-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63706-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63706-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63706-132">Header</span><span class="sxs-lookup"><span data-stu-id="63706-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="63706-133"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="63706-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63706-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63706-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63706-135">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="63706-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

