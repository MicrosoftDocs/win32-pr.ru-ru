---
title: Сообщение SBM_SETRANGEREDRAW (Winuser. h)
description: Приложение отправляет \_ сообщение СБМ сетранжередрав в элемент управления "полоса прокрутки", чтобы задать минимальное и максимальное значения расположения и перерисовать элемент управления.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Элементы управления Windows для SBM_SETRANGEREDRAW сообщений
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071106"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="62c95-104">\_Сообщение СБМ сетранжередрав</span><span class="sxs-lookup"><span data-stu-id="62c95-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="62c95-105">Приложение отправляет сообщение **СБМ \_ сетранжередрав** в элемент управления "полоса прокрутки", чтобы задать минимальное и максимальное значения расположения и перерисовать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="62c95-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="62c95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62c95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c95-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62c95-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62c95-108">Задает минимальную прокрутку.</span><span class="sxs-lookup"><span data-stu-id="62c95-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="62c95-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62c95-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62c95-110">Задает максимальную точку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="62c95-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c95-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62c95-111">Return value</span></span>

<span data-ttu-id="62c95-112">**ComCtl32.dll версии 5,0**: Если изменяется расположение ползунка, возвращаемое значение является предыдущим положением поля прокрутки; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="62c95-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="62c95-113">**ComCtl32.dll версии 6,0**: текущее расположение поля прокрутки, независимо от того, изменился ли он.</span><span class="sxs-lookup"><span data-stu-id="62c95-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c95-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62c95-114">Remarks</span></span>

<span data-ttu-id="62c95-115">По умолчанию минимальное и максимальное значения позиций равны нулю.</span><span class="sxs-lookup"><span data-stu-id="62c95-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="62c95-116">Разница между значениями, заданными параметрами *wParam* и *lParam* , не должна превышать макслонг.</span><span class="sxs-lookup"><span data-stu-id="62c95-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="62c95-117">Если минимальное и максимальное значения позиционирования равны, элемент управления "полоса прокрутки" скрыт и, по сути, отключен.</span><span class="sxs-lookup"><span data-stu-id="62c95-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c95-118">Требования</span><span class="sxs-lookup"><span data-stu-id="62c95-118">Requirements</span></span>



| <span data-ttu-id="62c95-119">Требование</span><span class="sxs-lookup"><span data-stu-id="62c95-119">Requirement</span></span> | <span data-ttu-id="62c95-120">Значение</span><span class="sxs-lookup"><span data-stu-id="62c95-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c95-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62c95-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62c95-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62c95-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62c95-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62c95-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62c95-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62c95-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62c95-125">Header</span><span class="sxs-lookup"><span data-stu-id="62c95-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c95-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62c95-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c95-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62c95-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="62c95-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="62c95-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62c95-129">**СБМ \_ жетпос**</span><span class="sxs-lookup"><span data-stu-id="62c95-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="62c95-130">**СБМ \_**</span><span class="sxs-lookup"><span data-stu-id="62c95-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="62c95-131">**СБМ \_ сетпос**</span><span class="sxs-lookup"><span data-stu-id="62c95-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="62c95-132">**СБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="62c95-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





