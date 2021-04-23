---
description: Отправляются в окно, размер, расположение или место в Z-порядке которого собирается измениться в результате вызова функции SetWindowPos или другой функции управления окнами.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Сообщение WM_WINDOWPOSCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816305"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="be5e5-103">\_Сообщение ВИНДОВПОСЧАНГИНГ WM</span><span class="sxs-lookup"><span data-stu-id="be5e5-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="be5e5-104">Отправляются в окно, размер, расположение или место в Z-порядке которого собирается измениться в результате вызова функции [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) или другой функции управления окнами.</span><span class="sxs-lookup"><span data-stu-id="be5e5-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="be5e5-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be5e5-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="be5e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be5e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be5e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be5e5-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="be5e5-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be5e5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be5e5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be5e5-110">Указатель на структуру [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) , которая содержит сведения о новом размере и позиции окна.</span><span class="sxs-lookup"><span data-stu-id="be5e5-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be5e5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be5e5-111">Return value</span></span>

<span data-ttu-id="be5e5-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="be5e5-112">Type: **LRESULT**</span></span>

<span data-ttu-id="be5e5-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="be5e5-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5e5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be5e5-114">Remarks</span></span>

<span data-ttu-id="be5e5-115">Для окна с стилем [**WS \_ OVERLAPPED**](window-styles.md) или **WS \_ Сиккфраме** функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщение [**WM \_ жетминмаксинфо**](wm-getminmaxinfo.md) в окно.</span><span class="sxs-lookup"><span data-stu-id="be5e5-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="be5e5-116">Это делается для проверки нового размера и расположения окна, а также для применения стилей клиента [CS \_ БИТЕАЛИГНКЛИЕНТ](about-window-classes.md) и CS \_ битеалигнвиндов.</span><span class="sxs-lookup"><span data-stu-id="be5e5-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="be5e5-117">Если не передать сообщение **WM \_ виндовпосчангинг** в функцию **дефвиндовпрок** , приложение может переопределить эти значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be5e5-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="be5e5-118">Во время обработки этого сообщения изменение любого значения в [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) влияет на новый размер, позицию или место в Z-порядке окна.</span><span class="sxs-lookup"><span data-stu-id="be5e5-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="be5e5-119">Приложение может препятствовать изменениям в окне, установив или сняв соответствующие биты в элементе **flags** элемента **WINDOWPOS**.</span><span class="sxs-lookup"><span data-stu-id="be5e5-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5e5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="be5e5-120">Requirements</span></span>



| <span data-ttu-id="be5e5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="be5e5-121">Requirement</span></span> | <span data-ttu-id="be5e5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="be5e5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5e5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be5e5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be5e5-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be5e5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be5e5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be5e5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be5e5-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be5e5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be5e5-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be5e5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be5e5-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be5e5-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5e5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be5e5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="be5e5-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="be5e5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be5e5-131">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="be5e5-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="be5e5-132">**енддефервиндовпос**</span><span class="sxs-lookup"><span data-stu-id="be5e5-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="be5e5-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="be5e5-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="be5e5-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="be5e5-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="be5e5-135">**WM \_ жетминмаксинфо**</span><span class="sxs-lookup"><span data-stu-id="be5e5-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="be5e5-136">**\_Перемещение WM**</span><span class="sxs-lookup"><span data-stu-id="be5e5-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="be5e5-137">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="be5e5-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="be5e5-138">**WM \_ виндовпосчанжед**</span><span class="sxs-lookup"><span data-stu-id="be5e5-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="be5e5-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="be5e5-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be5e5-140">Windows</span><span class="sxs-lookup"><span data-stu-id="be5e5-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
