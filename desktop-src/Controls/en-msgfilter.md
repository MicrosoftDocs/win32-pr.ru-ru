---
title: Код уведомления EN_MSGFILTER (RichEdit. h)
description: Уведомляет родительское окно элемента управления Rich Edit с клавиатурой или событием мыши в элементе управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136066"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="d34ca-105">\_Код уведомления EN мсгфилтер</span><span class="sxs-lookup"><span data-stu-id="d34ca-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="d34ca-106">Уведомляет родительское окно элемента управления Rich Edit с клавиатурой или событием мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="d34ca-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="d34ca-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d34ca-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d34ca-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d34ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34ca-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d34ca-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d34ca-110">Структура [**мсгфилтер**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) , содержащая сведения о клавиатуре или сообщении мыши.</span><span class="sxs-lookup"><span data-stu-id="d34ca-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="d34ca-111">Если родительское окно изменяет эту структуру и возвращает ненулевое значение, то измененное сообщение обрабатывается вместо исходного.</span><span class="sxs-lookup"><span data-stu-id="d34ca-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34ca-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d34ca-112">Return value</span></span>

<span data-ttu-id="d34ca-113">Возвращает нуль, если элемент управления должен обработать событие клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="d34ca-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="d34ca-114">Возвращает ненулевое значение, если элемент управления должен игнорировать событие клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="d34ca-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34ca-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d34ca-115">Remarks</span></span>

<span data-ttu-id="d34ca-116">Чтобы получить \_ коды уведомлений EN мсгфилтер для событий, укажите один или несколько из следующих флагов в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d34ca-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="d34ca-117">Flag</span><span class="sxs-lookup"><span data-stu-id="d34ca-117">Flag</span></span>                                                                             | <span data-ttu-id="d34ca-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d34ca-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d34ca-119">**ЕНМ \_ кэйевентс**</span><span class="sxs-lookup"><span data-stu-id="d34ca-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="d34ca-120">Для получения кодов уведомлений о событиях клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d34ca-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="d34ca-121">**ЕНМ \_ маусивентс**</span><span class="sxs-lookup"><span data-stu-id="d34ca-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="d34ca-122">Для получения кодов уведомлений о событиях мыши.</span><span class="sxs-lookup"><span data-stu-id="d34ca-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="d34ca-123">**ЕНМ \_ скроллевентс**</span><span class="sxs-lookup"><span data-stu-id="d34ca-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="d34ca-124">Для получения кодов уведомлений для события колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="d34ca-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d34ca-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d34ca-125">Requirements</span></span>



| <span data-ttu-id="d34ca-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d34ca-126">Requirement</span></span> | <span data-ttu-id="d34ca-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d34ca-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ca-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d34ca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d34ca-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d34ca-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d34ca-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d34ca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d34ca-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d34ca-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d34ca-132">Header</span><span class="sxs-lookup"><span data-stu-id="d34ca-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d34ca-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34ca-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34ca-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d34ca-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="d34ca-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d34ca-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d34ca-136">**мсгфилтер**</span><span class="sxs-lookup"><span data-stu-id="d34ca-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="d34ca-137">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="d34ca-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





