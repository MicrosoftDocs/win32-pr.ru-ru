---
description: Сообщение WM \_ нкпаинт отправляется в окно, когда его кадр должен быть окрашен.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Сообщение WM_NCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908935"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="35ce4-103">\_Сообщение НКПАИНТ WM</span><span class="sxs-lookup"><span data-stu-id="35ce4-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="35ce4-104">Сообщение **WM \_ нкпаинт** отправляется в окно, когда его кадр должен быть окрашен.</span><span class="sxs-lookup"><span data-stu-id="35ce4-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="35ce4-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="35ce4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="35ce4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ce4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35ce4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ce4-108">Маркер области обновления окна.</span><span class="sxs-lookup"><span data-stu-id="35ce4-108">A handle to the update region of the window.</span></span> <span data-ttu-id="35ce4-109">Регион обновления обрезается по рамке окна.</span><span class="sxs-lookup"><span data-stu-id="35ce4-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="35ce4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35ce4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ce4-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="35ce4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ce4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35ce4-112">Return value</span></span>

<span data-ttu-id="35ce4-113">Приложение возвращает нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="35ce4-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ce4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="35ce4-114">Remarks</span></span>

<span data-ttu-id="35ce4-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) закрашивает рамку окна.</span><span class="sxs-lookup"><span data-stu-id="35ce4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="35ce4-116">Приложение может перехватить **сообщение \_ нкпаинт WM** и закрасить собственную настраиваемую рамку окна.</span><span class="sxs-lookup"><span data-stu-id="35ce4-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="35ce4-117">Область обрезки для окна всегда прямоугольная, даже при изменении формы рамки.</span><span class="sxs-lookup"><span data-stu-id="35ce4-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="35ce4-118">Значение *wParam* можно передать в [**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="35ce4-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="35ce4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="35ce4-119">Requirements</span></span>



| <span data-ttu-id="35ce4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="35ce4-120">Requirement</span></span> | <span data-ttu-id="35ce4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="35ce4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ce4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35ce4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="35ce4-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35ce4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35ce4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35ce4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="35ce4-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35ce4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35ce4-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="35ce4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ce4-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ce4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ce4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ce4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ce4-129">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="35ce4-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="35ce4-130">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="35ce4-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="35ce4-131">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="35ce4-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="35ce4-132">**жетвиндовдк**</span><span class="sxs-lookup"><span data-stu-id="35ce4-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="35ce4-133">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="35ce4-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="35ce4-134">**жетдцекс**</span><span class="sxs-lookup"><span data-stu-id="35ce4-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
