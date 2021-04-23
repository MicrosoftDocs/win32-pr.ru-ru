---
description: Уведомляет окно о том, что удаляется неклиентская область. Функция Дестройвиндов отправляет \_ сообщение WM нкдестрой в окно после \_ сообщения WM destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Сообщение WM_NCDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998572"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="7f661-104">\_Сообщение НКДЕСТРОЙ WM</span><span class="sxs-lookup"><span data-stu-id="7f661-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="7f661-105">Уведомляет окно о том, что удаляется неклиентская область.</span><span class="sxs-lookup"><span data-stu-id="7f661-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="7f661-106">Функция [**дестройвиндов**](/windows/win32/api/winuser/nf-winuser-destroywindow) отправляет сообщение **WM \_ нкдестрой** в окно после сообщения [**WM \_ destroy**](wm-destroy.md) .[**WM \_ destroy**](wm-destroy.md) используется для высвобождения выделенного объекта памяти, связанного с окном.</span><span class="sxs-lookup"><span data-stu-id="7f661-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="7f661-107">Сообщение **WM \_ нкдестрой** отправляется после уничтожения дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="7f661-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="7f661-108">Напротив, [**WM \_ destroy**](wm-destroy.md) отправляется перед уничтожением дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="7f661-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="7f661-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7f661-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="7f661-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f661-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f661-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f661-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f661-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7f661-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f661-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f661-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f661-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7f661-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f661-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f661-115">Return value</span></span>

<span data-ttu-id="7f661-116">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="7f661-116">Type: **LRESULT**</span></span>

<span data-ttu-id="7f661-117">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="7f661-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f661-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f661-118">Remarks</span></span>

<span data-ttu-id="7f661-119">Это сообщение освобождает память, выделенную для окна.</span><span class="sxs-lookup"><span data-stu-id="7f661-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f661-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7f661-120">Requirements</span></span>



| <span data-ttu-id="7f661-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7f661-121">Requirement</span></span> | <span data-ttu-id="7f661-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7f661-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f661-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f661-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f661-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f661-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7f661-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f661-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f661-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f661-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f661-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f661-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f661-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f661-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f661-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f661-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f661-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7f661-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f661-131">**дестройвиндов**</span><span class="sxs-lookup"><span data-stu-id="7f661-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="7f661-132">**WM \_ destroy**</span><span class="sxs-lookup"><span data-stu-id="7f661-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="7f661-133">**WM \_ нккреате**</span><span class="sxs-lookup"><span data-stu-id="7f661-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="7f661-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7f661-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f661-135">Windows</span><span class="sxs-lookup"><span data-stu-id="7f661-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
