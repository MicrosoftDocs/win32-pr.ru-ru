---
title: Код уведомления EN_LINK (RichEdit. h)
description: Форматированный элемент управления "поле ввода" отправляет \_ коды уведомлений о ссылках на короткое время при получении различных сообщений, например, когда пользователь нажимает кнопку мыши или когда указатель мыши находится над текстом, имеющим \_ результат CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492447"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="e7b66-104">\_Код уведомления о ссылке EN</span><span class="sxs-lookup"><span data-stu-id="e7b66-104">EN\_LINK notification code</span></span>

<span data-ttu-id="e7b66-105">Форматированный элемент управления "поле ввода" отправляет \_ коды уведомлений о ссылках на короткое время при получении различных сообщений, например, когда пользователь нажимает кнопку мыши или когда указатель мыши находится над текстом, имеющим результат **CFE \_** .</span><span class="sxs-lookup"><span data-stu-id="e7b66-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="e7b66-106">Безоконный элемент управления "поле ввода" не отправляет это уведомление с помощью метода [**итекссост:: ткснотифи**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="e7b66-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="e7b66-107">Родительское окно элемента управления получает этот код уведомления через сообщение [**\_ уведомления WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b66-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7b66-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7b66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b66-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7b66-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b66-110">ИДЕНТИФИКАТОР окна, полученный путем вызова функции [**жетвиндовлонг**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) со \_ значением идентификатора ГВЛ.</span><span class="sxs-lookup"><span data-stu-id="e7b66-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="e7b66-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7b66-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b66-112">Указатель на структуру [**енлинк**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="e7b66-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="e7b66-113">Структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , сведения о коде уведомления и структуру [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , которая указывает диапазон символов, имеющих результат **\_ связи CFE** .</span><span class="sxs-lookup"><span data-stu-id="e7b66-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b66-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7b66-114">Return value</span></span>

<span data-ttu-id="e7b66-115">Возвращает ноль, чтобы разрешить элементу управления продолжать нормальную обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7b66-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="e7b66-116">Возврат ненулевого значения для предотвращения обработки сообщения элементом управления.</span><span class="sxs-lookup"><span data-stu-id="e7b66-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="e7b66-117">**Windows 8**: возврат **\_ ссылки en \_ \_ по умолчанию используется** для направления элемента управления Rich Edit для выполнения действия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7b66-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b66-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7b66-118">Remarks</span></span>

<span data-ttu-id="e7b66-119">Чтобы получать коды уведомлений по **\_ ссылке** , если ссылка имеет фокус, укажите флаг [**\_ ссылки енм**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b66-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="e7b66-120">Если ссылка не имеет фокуса, для получения кодов уведомлений по **короткой \_ ссылке** укажите флаг **SES \_ нофокуслинкнотифи** в маске, отправляемой с сообщением [**\_ сетедитстиле EM**](em-seteditstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b66-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="e7b66-121">Форматированный элемент управления "поле ввода" отправляет коды уведомления о **\_ ссылке** , когда он получает следующие сообщения, когда указатель мыши находится над текстом, имеющим результат **CFE \_ Link** :</span><span class="sxs-lookup"><span data-stu-id="e7b66-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="e7b66-122">**WM \_ лбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="e7b66-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="e7b66-123">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="e7b66-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="e7b66-124">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="e7b66-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="e7b66-125">**WM \_ MOUSEMOVE**</span><span class="sxs-lookup"><span data-stu-id="e7b66-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="e7b66-126">**WM \_ рбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="e7b66-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="e7b66-127">**WM \_ рбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="e7b66-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="e7b66-128">**WM \_ рбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="e7b66-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="e7b66-129">**WM \_ сеткурсор**</span><span class="sxs-lookup"><span data-stu-id="e7b66-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="e7b66-130">Как правило, **CFE \_ ссылка** определяет диапазон текста, который содержит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e7b66-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="e7b66-131">Приложения могут управлять \_ кодом уведомления о ссылке, изменяя указатель мыши, когда он находится над URL-адресом, или запустив браузер для просмотра расположения, определенного URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="e7b66-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="e7b66-132">Если вы отправляете сообщение [**EM \_ аутаурлдетект**](em-autourldetect.md) для включения автоматического обнаружения URL-адресов, элемент управления Rich Editing автоматически **устанавливает для измененного текста значение, \_** которое он идентифицирует как URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e7b66-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b66-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e7b66-133">Requirements</span></span>



| <span data-ttu-id="e7b66-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e7b66-134">Requirement</span></span> | <span data-ttu-id="e7b66-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e7b66-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b66-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7b66-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b66-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7b66-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7b66-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7b66-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b66-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7b66-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7b66-140">Header</span><span class="sxs-lookup"><span data-stu-id="e7b66-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b66-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b66-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b66-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7b66-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b66-143">**чарранже**</span><span class="sxs-lookup"><span data-stu-id="e7b66-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="e7b66-144">**EM \_ аутаурлдетект**</span><span class="sxs-lookup"><span data-stu-id="e7b66-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="e7b66-145">**енлинк**</span><span class="sxs-lookup"><span data-stu-id="e7b66-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="e7b66-146">**ITextRange2:: SetURL**</span><span class="sxs-lookup"><span data-stu-id="e7b66-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="e7b66-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="e7b66-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

