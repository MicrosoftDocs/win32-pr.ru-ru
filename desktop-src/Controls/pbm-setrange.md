---
title: Сообщение PBM_SETRANGE (Коммктрл. h)
description: Задает минимальное и максимальное значения индикатора выполнения и перерисовывает линию для отражения нового диапазона.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Элементы управления Windows для PBM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892281"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="1d9eb-104">\_Message SETRANGE, сообщение</span><span class="sxs-lookup"><span data-stu-id="1d9eb-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="1d9eb-105">Задает минимальное и максимальное значения индикатора выполнения и перерисовывает линию для отражения нового диапазона.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d9eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d9eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d9eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9eb-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1d9eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d9eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9eb-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает минимальное значение диапазона, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает максимальное значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="1d9eb-111">Минимальное значение диапазона не должно быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="1d9eb-112">По умолчанию минимальное значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="1d9eb-113">Максимальное значение диапазона должно быть больше минимального значения диапазона.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="1d9eb-114">По умолчанию максимальное значение диапазона — 100.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d9eb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d9eb-115">Return value</span></span>

<span data-ttu-id="1d9eb-116">Возвращает предыдущие значения диапазона в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="1d9eb-117">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает предыдущее минимальное значение, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает предыдущее максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d9eb-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d9eb-118">Remarks</span></span>

<span data-ttu-id="1d9eb-119">Если значения в диапазоне не заданы, система устанавливает минимальное значение 0, а максимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="1d9eb-120">Поскольку это сообщение выражается как 16-разрядное целое число без знака, оно может быть в диапазоне от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="1d9eb-121">Минимальное значение в диапазоне может быть от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="1d9eb-122">Точно так же максимальное значение может быть от 0 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="1d9eb-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="1d9eb-123">Чтобы задать больший диапазон, вызовите [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="1d9eb-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9eb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1d9eb-124">Requirements</span></span>



| <span data-ttu-id="1d9eb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1d9eb-125">Requirement</span></span> | <span data-ttu-id="1d9eb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1d9eb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9eb-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d9eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9eb-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d9eb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d9eb-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d9eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9eb-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d9eb-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d9eb-131">Header</span><span class="sxs-lookup"><span data-stu-id="1d9eb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d9eb-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d9eb-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d9eb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d9eb-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d9eb-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1d9eb-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d9eb-135">**PBM/ \_ Range**</span><span class="sxs-lookup"><span data-stu-id="1d9eb-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="1d9eb-136">**\_SETRANGE32 PBM**</span><span class="sxs-lookup"><span data-stu-id="1d9eb-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

