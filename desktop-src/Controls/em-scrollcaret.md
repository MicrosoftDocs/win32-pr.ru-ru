---
title: Сообщение EM_SCROLLCARET (Winuser. h)
description: Прокручивает курсор на представление в элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- Элементы управления Windows для EM_SCROLLCARET сообщений
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137622"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="e5c42-105">\_Сообщение СКРОЛЛКАРЕТ EM</span><span class="sxs-lookup"><span data-stu-id="e5c42-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="e5c42-106">Прокручивает курсор на представление в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e5c42-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="e5c42-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e5c42-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5c42-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5c42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5c42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c42-110">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="e5c42-110">This parameter is reserved.</span></span> <span data-ttu-id="e5c42-111">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5c42-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e5c42-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5c42-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5c42-113">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="e5c42-113">This parameter is reserved.</span></span> <span data-ttu-id="e5c42-114">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5c42-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c42-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5c42-115">Return value</span></span>

<span data-ttu-id="e5c42-116">Возвращаемое значение не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="e5c42-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5c42-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5c42-117">Remarks</span></span>

<span data-ttu-id="e5c42-118">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e5c42-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e5c42-119">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e5c42-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c42-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e5c42-120">Requirements</span></span>



| <span data-ttu-id="e5c42-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e5c42-121">Requirement</span></span> | <span data-ttu-id="e5c42-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e5c42-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c42-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5c42-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5c42-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5c42-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5c42-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5c42-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5c42-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5c42-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5c42-127">Header</span><span class="sxs-lookup"><span data-stu-id="e5c42-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5c42-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5c42-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c42-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5c42-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5c42-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e5c42-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5c42-131">**EM \_ линескролл**</span><span class="sxs-lookup"><span data-stu-id="e5c42-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="e5c42-132">**\_прокрутка EM**</span><span class="sxs-lookup"><span data-stu-id="e5c42-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="e5c42-133">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="e5c42-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





