---
title: Сообщение WM_NOTIFY (Winuser. h)
description: Посылается обычным элементом управления в его родительское окно, когда произошло событие или для элемента управления требуются некоторые сведения.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Элементы управления Windows для WM_NOTIFY сообщений
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988898"
---
# <a name="wm_notify-message"></a><span data-ttu-id="e261e-104">\_Уведомить сообщение WM</span><span class="sxs-lookup"><span data-stu-id="e261e-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="e261e-105">Посылается обычным элементом управления в его родительское окно, когда произошло событие или для элемента управления требуются некоторые сведения.</span><span class="sxs-lookup"><span data-stu-id="e261e-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="e261e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e261e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e261e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e261e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e261e-108">Идентификатор общего элемента управления, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="e261e-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="e261e-109">Этот идентификатор не обязательно должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="e261e-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="e261e-110">Для обнаружения элемента управления приложение должно использовать элемент **хвндфром** или **идфром** структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (переданный как параметр *lParam* ).</span><span class="sxs-lookup"><span data-stu-id="e261e-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="e261e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e261e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e261e-112">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую код уведомления и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e261e-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="e261e-113">Для некоторых сообщений с уведомлениями этот параметр указывает на большую структуру, в которой структура **NMHDR** является первым элементом.</span><span class="sxs-lookup"><span data-stu-id="e261e-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e261e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e261e-114">Return value</span></span>

<span data-ttu-id="e261e-115">Возвращаемое значение игнорируется, за исключением сообщений уведомления, в которых указано иное.</span><span class="sxs-lookup"><span data-stu-id="e261e-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e261e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e261e-116">Remarks</span></span>

<span data-ttu-id="e261e-117">Место назначения сообщения должно быть **HWND** родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e261e-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="e261e-118">Это значение можно получить с помощью функции- [**родителя**](/windows/desktop/api/winuser/nf-winuser-getparent), как показано в следующем примере, где *m \_ контролхвнд* — это **HWND** самого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e261e-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="e261e-119">Приложения обрабатывают сообщение в процедуре окна родительского окна, как показано в следующем примере, который обрабатывает сообщение уведомления, отправленное пользовательским элементом управления в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="e261e-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="e261e-120">Некоторые уведомления, которые находятся в API в течение длительного времени, отправляются в виде [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e261e-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="e261e-121">Дополнительные сведения см. в разделе [Управление сообщениями](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e261e-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="e261e-122">Если обработчик сообщений находится в процедуре диалогового окна, необходимо использовать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) с DWL \_ мсгресулт, чтобы задать возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="e261e-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="e261e-123">Для систем Windows Vista и более поздних версий сообщение **WM \_ Notify** не может быть отправлено между процессами.</span><span class="sxs-lookup"><span data-stu-id="e261e-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="e261e-124">Многие уведомления доступны в форматах ANSI и Юникод.</span><span class="sxs-lookup"><span data-stu-id="e261e-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="e261e-125">Окно, отправляющее сообщение **WM \_ Notify** , использует сообщение [**WM \_ нотифиформат**](wm-notifyformat.md) для определения формата, который следует использовать.</span><span class="sxs-lookup"><span data-stu-id="e261e-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="e261e-126">Дополнительные сведения см. в разделе **WM \_ нотифиформат** .</span><span class="sxs-lookup"><span data-stu-id="e261e-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="e261e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e261e-127">Requirements</span></span>



| <span data-ttu-id="e261e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e261e-128">Requirement</span></span> | <span data-ttu-id="e261e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e261e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e261e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e261e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e261e-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e261e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e261e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e261e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e261e-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e261e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e261e-134">Header</span><span class="sxs-lookup"><span data-stu-id="e261e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e261e-135"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e261e-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e261e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e261e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e261e-137">**WM \_ нотифиформат**</span><span class="sxs-lookup"><span data-stu-id="e261e-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

