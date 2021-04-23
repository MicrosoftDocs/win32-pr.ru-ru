---
description: Отправляется при уничтожении окна. Он отправляется в окно процедуры, которое уничтожается после удаления окна с экрана.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Сообщение WM_DESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265439"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="7a4db-104">\_Сообщение об уничтожении WM</span><span class="sxs-lookup"><span data-stu-id="7a4db-104">WM\_DESTROY message</span></span>

<span data-ttu-id="7a4db-105">Отправляется при уничтожении окна.</span><span class="sxs-lookup"><span data-stu-id="7a4db-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="7a4db-106">Он отправляется в окно процедуры, которое уничтожается после удаления окна с экрана.</span><span class="sxs-lookup"><span data-stu-id="7a4db-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="7a4db-107">Это сообщение отправляется первым в удаляемое окно, а затем в дочерние окна (если они есть) при их уничтожении.</span><span class="sxs-lookup"><span data-stu-id="7a4db-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="7a4db-108">Во время обработки сообщения можно предположить, что все остальные дочерние окна все еще существуют.</span><span class="sxs-lookup"><span data-stu-id="7a4db-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="7a4db-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7a4db-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="7a4db-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a4db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a4db-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a4db-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a4db-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7a4db-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7a4db-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a4db-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a4db-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7a4db-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a4db-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a4db-115">Return value</span></span>

<span data-ttu-id="7a4db-116">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="7a4db-116">Type: **LRESULT**</span></span>

<span data-ttu-id="7a4db-117">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="7a4db-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a4db-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a4db-118">Remarks</span></span>

<span data-ttu-id="7a4db-119">Если удаляемое окно является частью цепочки окна просмотра буфера обмена (задается вызовом функции [**сетклипбоардвиевер**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), окно должно удалить себя из цепочки, обрабатывая функцию [**чанжеклипбоардчаин**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) перед возвратом из сообщения **WM \_ destroy** .</span><span class="sxs-lookup"><span data-stu-id="7a4db-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4db-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7a4db-120">Requirements</span></span>



| <span data-ttu-id="7a4db-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7a4db-121">Requirement</span></span> | <span data-ttu-id="7a4db-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7a4db-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4db-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a4db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4db-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a4db-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a4db-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a4db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4db-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7a4db-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a4db-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7a4db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4db-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a4db-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4db-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a4db-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a4db-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7a4db-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a4db-131">**чанжеклипбоардчаин**</span><span class="sxs-lookup"><span data-stu-id="7a4db-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="7a4db-132">**дестройвиндов**</span><span class="sxs-lookup"><span data-stu-id="7a4db-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="7a4db-133">**посткуитмессаже**</span><span class="sxs-lookup"><span data-stu-id="7a4db-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="7a4db-134">**сетклипбоардвиевер**</span><span class="sxs-lookup"><span data-stu-id="7a4db-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="7a4db-135">**\_Закрыть WM**</span><span class="sxs-lookup"><span data-stu-id="7a4db-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="7a4db-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7a4db-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7a4db-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7a4db-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
