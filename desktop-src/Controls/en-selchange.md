---
title: Код уведомления EN_SELCHANGE (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что текущее выделение изменилось. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803424"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="92b6e-105">\_Код уведомления EN селчанже</span><span class="sxs-lookup"><span data-stu-id="92b6e-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="92b6e-106">Сообщает родительскому окну элемента управления Rich Edit, что текущее выделение изменилось.</span><span class="sxs-lookup"><span data-stu-id="92b6e-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="92b6e-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="92b6e-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="92b6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92b6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92b6e-110">Структура [**селчанже**](/windows/desktop/api/Richedit/ns-richedit-selchange) , которая получает сведения о выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="92b6e-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b6e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92b6e-111">Return value</span></span>

<span data-ttu-id="92b6e-112">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="92b6e-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b6e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92b6e-113">Remarks</span></span>

<span data-ttu-id="92b6e-114">Чтобы получить \_ коды уведомлений EN селчанже, укажите [**енм \_ селчанже**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="92b6e-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="92b6e-115">Этот код уведомления отправляется при изменении позиции курсора и если текст не выбран (выделение пусто).</span><span class="sxs-lookup"><span data-stu-id="92b6e-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="92b6e-116">Позиции курсора могут изменяться, когда пользователь щелкает мышью, вводит или нажимает клавишу со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="92b6e-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b6e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="92b6e-117">Requirements</span></span>



| <span data-ttu-id="92b6e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="92b6e-118">Requirement</span></span> | <span data-ttu-id="92b6e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="92b6e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92b6e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92b6e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92b6e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92b6e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92b6e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92b6e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92b6e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92b6e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92b6e-124">Header</span><span class="sxs-lookup"><span data-stu-id="92b6e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92b6e-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b6e-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b6e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92b6e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="92b6e-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="92b6e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92b6e-128">**селчанже**</span><span class="sxs-lookup"><span data-stu-id="92b6e-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="92b6e-129">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="92b6e-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





