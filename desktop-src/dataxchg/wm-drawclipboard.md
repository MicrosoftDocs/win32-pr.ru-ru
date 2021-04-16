---
title: Сообщение WM_DRAWCLIPBOARD (Winuser. h)
description: Отправляется в первое окно в цепочке окна просмотра буфера обмена при изменении содержимого буфера обмена. Это позволяет окну просмотра буфера обмена отображать новое содержимое буфера обмена. Окно получает это сообщение через функцию WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Обмен данными с сообщениями WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661899"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="57723-106">\_Сообщение ДРАВКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="57723-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="57723-107">Отправляется в первое окно в цепочке окна просмотра буфера обмена при изменении содержимого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="57723-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="57723-108">Это позволяет окну просмотра буфера обмена отображать новое содержимое буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="57723-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="57723-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="57723-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="57723-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="57723-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57723-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57723-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57723-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="57723-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57723-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57723-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57723-114">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="57723-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57723-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57723-115">Remarks</span></span>

<span data-ttu-id="57723-116">Это сообщение получит только окно просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="57723-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="57723-117">Это окна, добавленные в цепочку средства просмотра буфера обмена с помощью функции [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="57723-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="57723-118">Каждое окно, получающее **сообщение \_ дравклипбоард WM** , должно вызывать функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) для передачи сообщения в следующее окно в цепочке окна просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="57723-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="57723-119">Маркер для следующего окна в цепочке возвращается [**сетклипбоардвиевер**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)и может измениться в ответ на сообщение [**\_ чанжекбчаин WM**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="57723-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="57723-120">Требования</span><span class="sxs-lookup"><span data-stu-id="57723-120">Requirements</span></span>



| <span data-ttu-id="57723-121">Требование</span><span class="sxs-lookup"><span data-stu-id="57723-121">Requirement</span></span> | <span data-ttu-id="57723-122">Значение</span><span class="sxs-lookup"><span data-stu-id="57723-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57723-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57723-123">Minimum supported client</span></span><br/> | <span data-ttu-id="57723-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57723-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57723-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57723-125">Minimum supported server</span></span><br/> | <span data-ttu-id="57723-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57723-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57723-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57723-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="57723-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57723-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57723-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57723-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="57723-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="57723-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57723-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="57723-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="57723-132">**сетклипбоардвиевер**</span><span class="sxs-lookup"><span data-stu-id="57723-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="57723-133">**WM \_ чанжекбчаин**</span><span class="sxs-lookup"><span data-stu-id="57723-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="57723-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="57723-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57723-135">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="57723-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

