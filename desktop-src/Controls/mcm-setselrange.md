---
title: Сообщение MCM_SETSELRANGE (Коммктрл. h)
description: Задает для элемента управления "месячный календарь" определенный диапазон дат. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетселранже.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Элементы управления Windows для MCM_SETSELRANGE сообщений
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071185"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="e7c63-105">\_Сообщение MCM сетселранже</span><span class="sxs-lookup"><span data-stu-id="e7c63-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="e7c63-106">Задает для элемента управления "месячный календарь" определенный диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="e7c63-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="e7c63-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетселранже**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .</span><span class="sxs-lookup"><span data-stu-id="e7c63-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7c63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7c63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c63-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7c63-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7c63-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e7c63-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7c63-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7c63-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c63-112">Указатель на массив элементов [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами, содержащий сведения о дате, представляющие ограничения выбора.</span><span class="sxs-lookup"><span data-stu-id="e7c63-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="e7c63-113">Первая выбранная дата должна быть указана в *лпсистимеаррай* \[ 0 \] , а последняя выбранная дата должна быть указана в *лпсистимеаррай* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e7c63-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c63-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7c63-114">Return value</span></span>

<span data-ttu-id="e7c63-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e7c63-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="e7c63-116">Это сообщение не будет выполнено, если применяется к элементу управления "месячный календарь", который не использует многоэлементный стиль [**MCS \_**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c63-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c63-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e7c63-117">Requirements</span></span>



| <span data-ttu-id="e7c63-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e7c63-118">Requirement</span></span> | <span data-ttu-id="e7c63-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e7c63-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c63-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7c63-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c63-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7c63-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7c63-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7c63-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c63-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7c63-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7c63-124">Header</span><span class="sxs-lookup"><span data-stu-id="e7c63-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c63-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c63-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c63-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7c63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c63-127">Время в элементе управления ' календарь на месяц '</span><span class="sxs-lookup"><span data-stu-id="e7c63-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

