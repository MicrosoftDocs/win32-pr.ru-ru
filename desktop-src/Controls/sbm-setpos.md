---
title: Сообщение SBM_SETPOS (Winuser. h)
description: Сообщение СБМ \_ сетпос отправляется, чтобы задать расположение ползунка (бегунка) и, при необходимости, перерисовать полосу прокрутки, чтобы отразить новую точку прокрутки.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Элементы управления Windows для SBM_SETPOS сообщений
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493047"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="65a03-104">\_Сообщение СБМ сетпос</span><span class="sxs-lookup"><span data-stu-id="65a03-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="65a03-105">Сообщение **СБМ \_ сетпос** отправляется, чтобы задать расположение ползунка (бегунка) и, при необходимости, перерисовать полосу прокрутки, чтобы отразить новую точку прокрутки.</span><span class="sxs-lookup"><span data-stu-id="65a03-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="65a03-106">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="65a03-106">Applications should not send this message directly.</span></span> <span data-ttu-id="65a03-107">Вместо этого они должны использовать функцию [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="65a03-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="65a03-108">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="65a03-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="65a03-109">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **сетскроллпос** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="65a03-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="65a03-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="65a03-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a03-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65a03-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65a03-112">Задает новое расположение ползунка.</span><span class="sxs-lookup"><span data-stu-id="65a03-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="65a03-113">Он должен находиться в пределах диапазона прокрутки.</span><span class="sxs-lookup"><span data-stu-id="65a03-113">It must be within the scrolling range.</span></span> <span data-ttu-id="65a03-114">Если этот параметр находится за пределами диапазона прокрутки, значение округляется вверх или вниз до ближайшего допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="65a03-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="65a03-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65a03-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65a03-116">Указывает, следует ли перерисовать полосу прокрутки для отражения новой позицией ползунка.</span><span class="sxs-lookup"><span data-stu-id="65a03-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="65a03-117">Если этот параметр имеет **значение true**, полоса прокрутки перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="65a03-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="65a03-118">Если значение равно **false**, полоса прокрутки не перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="65a03-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a03-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65a03-119">Return value</span></span>

<span data-ttu-id="65a03-120">**ComCtl32.dll версии 5,0**: Если изменяется расположение ползунка, возвращаемое значение является предыдущим положением поля прокрутки; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="65a03-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="65a03-121">**ComCtl32.dll версии 6,0**: текущее расположение поля прокрутки, независимо от того, изменился ли он.</span><span class="sxs-lookup"><span data-stu-id="65a03-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a03-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65a03-122">Remarks</span></span>

<span data-ttu-id="65a03-123">Если элемент управления "полоса прокрутки" перерисовывается при последующем вызове другой функции, целесообразно установить параметр *lParam* в **значение false** .</span><span class="sxs-lookup"><span data-stu-id="65a03-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a03-124">Требования</span><span class="sxs-lookup"><span data-stu-id="65a03-124">Requirements</span></span>



| <span data-ttu-id="65a03-125">Требование</span><span class="sxs-lookup"><span data-stu-id="65a03-125">Requirement</span></span> | <span data-ttu-id="65a03-126">Значение</span><span class="sxs-lookup"><span data-stu-id="65a03-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a03-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65a03-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65a03-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65a03-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="65a03-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65a03-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65a03-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65a03-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65a03-131">Header</span><span class="sxs-lookup"><span data-stu-id="65a03-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="65a03-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65a03-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65a03-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65a03-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="65a03-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="65a03-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="65a03-135">**СБМ \_ жетпос**</span><span class="sxs-lookup"><span data-stu-id="65a03-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="65a03-136">**СБМ \_**</span><span class="sxs-lookup"><span data-stu-id="65a03-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="65a03-137">**СБМ \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="65a03-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="65a03-138">**СБМ \_ сетранжередрав**</span><span class="sxs-lookup"><span data-stu-id="65a03-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

