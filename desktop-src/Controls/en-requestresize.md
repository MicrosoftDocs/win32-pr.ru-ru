---
title: Код уведомления EN_REQUESTRESIZE (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что содержимое элемента управления меньше или превышает размер окна элемента управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136443"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="ea48c-105">\_Код уведомления EN рекуестресизе</span><span class="sxs-lookup"><span data-stu-id="ea48c-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="ea48c-106">Сообщает родительскому окну элемента управления Rich Edit, что содержимое элемента управления меньше или превышает размер окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ea48c-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="ea48c-107">Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ea48c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ea48c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea48c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea48c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea48c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea48c-110">Структура [**рекресизе**](/windows/desktop/api/Richedit/ns-richedit-reqresize) , которая получает запрошенный размер.</span><span class="sxs-lookup"><span data-stu-id="ea48c-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea48c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea48c-111">Return value</span></span>

<span data-ttu-id="ea48c-112">Этот код уведомления не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ea48c-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea48c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea48c-113">Remarks</span></span>

<span data-ttu-id="ea48c-114">Для поддержки нижнего поведения элемента управления Rich Edit родительское окно должно изменить размер элемента управления при получении этого кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="ea48c-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="ea48c-115">Чтобы получить \_ коды уведомлений EN рекуестресизе, укажите [**енм \_ рекуестресизе**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="ea48c-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea48c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ea48c-116">Requirements</span></span>



| <span data-ttu-id="ea48c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ea48c-117">Requirement</span></span> | <span data-ttu-id="ea48c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ea48c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea48c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea48c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea48c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea48c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea48c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea48c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea48c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea48c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea48c-123">Header</span><span class="sxs-lookup"><span data-stu-id="ea48c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea48c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea48c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea48c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea48c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea48c-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ea48c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea48c-127">**рекресизе**</span><span class="sxs-lookup"><span data-stu-id="ea48c-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="ea48c-128">**\_уведомление WM**</span><span class="sxs-lookup"><span data-stu-id="ea48c-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





