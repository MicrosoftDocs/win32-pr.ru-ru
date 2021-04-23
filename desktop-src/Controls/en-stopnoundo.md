---
title: Код уведомления EN_STOPNOUNDO (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что произошло действие, для которого элемент управления не может выделить достаточно памяти для сохранения состояния отмены. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137143"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="f9959-105">\_Код уведомления EN стопнаундо</span><span class="sxs-lookup"><span data-stu-id="f9959-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="f9959-106">Сообщает родительскому окну элемента управления Rich Edit, что произошло действие, для которого элемент управления не может выделить достаточно памяти для сохранения состояния отмены.</span><span class="sxs-lookup"><span data-stu-id="f9959-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="f9959-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f9959-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f9959-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9959-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9959-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9959-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9959-110">Структура [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="f9959-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9959-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9959-111">Return value</span></span>

<span data-ttu-id="f9959-112">Возвращает ноль, чтобы продолжить операцию **отмены** .</span><span class="sxs-lookup"><span data-stu-id="f9959-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="f9959-113">Чтобы отменить операцию **отмены** , возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f9959-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9959-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9959-114">Remarks</span></span>

<span data-ttu-id="f9959-115">Родительское окно всегда будет получать сообщение [**WM \_ Notify**](wm-notify.md) для этого события, оно не требует отправки маски уведомления с [**\_ SETEVENTMASK EM**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="f9959-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9959-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f9959-116">Requirements</span></span>



| <span data-ttu-id="f9959-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f9959-117">Requirement</span></span> | <span data-ttu-id="f9959-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f9959-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9959-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9959-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9959-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9959-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9959-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9959-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9959-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9959-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9959-123">Header</span><span class="sxs-lookup"><span data-stu-id="f9959-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9959-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9959-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9959-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9959-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9959-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f9959-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9959-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="f9959-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="f9959-128">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="f9959-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





