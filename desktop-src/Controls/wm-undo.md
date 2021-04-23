---
title: Сообщение WM_UNDO (Winuser. h)
description: Приложение отправляет \_ сообщение об отмене WM в элемент управления "поле ввода" для отмены последней операции. При отправке этого сообщения в элемент управления правки ранее удаленный текст восстанавливается или удаляется ранее добавленный текст.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Элементы управления Windows для WM_UNDO сообщений
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491418"
---
# <a name="wm_undo-message"></a><span data-ttu-id="0aaff-105">\_Сообщение об отмене WM</span><span class="sxs-lookup"><span data-stu-id="0aaff-105">WM\_UNDO message</span></span>

<span data-ttu-id="0aaff-106">Приложение отправляет сообщение об **\_ отмене WM** в элемент управления "поле ввода" для отмены последней операции.</span><span class="sxs-lookup"><span data-stu-id="0aaff-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="0aaff-107">При отправке этого сообщения в элемент управления правки ранее удаленный текст восстанавливается или удаляется ранее добавленный текст.</span><span class="sxs-lookup"><span data-stu-id="0aaff-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="0aaff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aaff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aaff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0aaff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aaff-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0aaff-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0aaff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0aaff-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0aaff-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0aaff-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aaff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aaff-113">Return value</span></span>

<span data-ttu-id="0aaff-114">Если сообщение прошло удачно, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0aaff-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="0aaff-115">Если сообщение не выполняется, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="0aaff-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aaff-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0aaff-116">Remarks</span></span>

<span data-ttu-id="0aaff-117">**Расширенное редактирование:** Вместо команды **\_ отмены WM** рекомендуется использовать [**\_ отмену EM**](em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="0aaff-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aaff-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0aaff-118">Requirements</span></span>



| <span data-ttu-id="0aaff-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0aaff-119">Requirement</span></span> | <span data-ttu-id="0aaff-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0aaff-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aaff-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0aaff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0aaff-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0aaff-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0aaff-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0aaff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0aaff-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0aaff-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0aaff-125">Header</span><span class="sxs-lookup"><span data-stu-id="0aaff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aaff-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aaff-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aaff-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aaff-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aaff-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="0aaff-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0aaff-129">**WM \_ clear**</span><span class="sxs-lookup"><span data-stu-id="0aaff-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="0aaff-130">**\_копия WM**</span><span class="sxs-lookup"><span data-stu-id="0aaff-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="0aaff-131">**Вырезание WM \_**</span><span class="sxs-lookup"><span data-stu-id="0aaff-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="0aaff-132">**\_Вставка WM**</span><span class="sxs-lookup"><span data-stu-id="0aaff-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

