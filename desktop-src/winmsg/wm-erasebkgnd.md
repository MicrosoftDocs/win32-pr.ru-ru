---
description: Посылается, когда фон окна должен быть стерт (например, при изменении размера окна). Сообщение отправляется для подготовки недействительной части окна для рисования.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Сообщение WM_ERASEBKGND (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265438"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="e22b8-104">\_Сообщение ЕРАСЕБКГНД WM</span><span class="sxs-lookup"><span data-stu-id="e22b8-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="e22b8-105">Посылается, когда фон окна должен быть стерт (например, при изменении размера окна).</span><span class="sxs-lookup"><span data-stu-id="e22b8-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="e22b8-106">Сообщение отправляется для подготовки недействительной части окна для рисования.</span><span class="sxs-lookup"><span data-stu-id="e22b8-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="e22b8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e22b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22b8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e22b8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e22b8-109">Маркер контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="e22b8-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="e22b8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e22b8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e22b8-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e22b8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22b8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e22b8-112">Return value</span></span>

<span data-ttu-id="e22b8-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="e22b8-113">Type: **LRESULT**</span></span>

<span data-ttu-id="e22b8-114">Приложение должно вернуть ненулевое значение, если удаляет фон. в противном случае он должен вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="e22b8-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e22b8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e22b8-115">Remarks</span></span>

<span data-ttu-id="e22b8-116">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) удаляет фон, используя кисть фона класса, заданную элементом **хбрбаккграунд** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) .</span><span class="sxs-lookup"><span data-stu-id="e22b8-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="e22b8-117">Если **хбрбаккграунд** имеет **значение NULL**, приложение должно обработать сообщение **WM \_ ерасебкгнд** и стереть фон.</span><span class="sxs-lookup"><span data-stu-id="e22b8-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="e22b8-118">Приложение должно вернуть ненулевое значение в ответ на **\_ ерасебкгнд WM** , если оно обрабатывает сообщение и стирает фон. Это означает, что дальнейшая очистка не требуется.</span><span class="sxs-lookup"><span data-stu-id="e22b8-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="e22b8-119">Если приложение возвращает ноль, окно остается помеченным для стирания.</span><span class="sxs-lookup"><span data-stu-id="e22b8-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="e22b8-120">(Как правило, это означает, что элемент **ферасе** структуры [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) будет иметь **значение true**.)</span><span class="sxs-lookup"><span data-stu-id="e22b8-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="e22b8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e22b8-121">Requirements</span></span>



| <span data-ttu-id="e22b8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e22b8-122">Requirement</span></span> | <span data-ttu-id="e22b8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e22b8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22b8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e22b8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e22b8-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e22b8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e22b8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e22b8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e22b8-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e22b8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e22b8-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e22b8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e22b8-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e22b8-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22b8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e22b8-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e22b8-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e22b8-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e22b8-132">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="e22b8-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e22b8-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="e22b8-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="e22b8-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e22b8-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e22b8-135">Значки</span><span class="sxs-lookup"><span data-stu-id="e22b8-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="e22b8-136">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e22b8-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e22b8-137">**бегинпаинт**</span><span class="sxs-lookup"><span data-stu-id="e22b8-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="e22b8-138">**PAINTSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="e22b8-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
