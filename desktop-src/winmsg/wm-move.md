---
description: Посылается после перемещения окна.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Сообщение WM_MOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673824"
---
# <a name="wm_move-message"></a><span data-ttu-id="3d895-103">\_Сообщение о перемещении WM</span><span class="sxs-lookup"><span data-stu-id="3d895-103">WM\_MOVE message</span></span>

<span data-ttu-id="3d895-104">Посылается после перемещения окна.</span><span class="sxs-lookup"><span data-stu-id="3d895-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="3d895-105">Окно получает это сообщение через функцию [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="3d895-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="3d895-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d895-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d895-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d895-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3d895-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3d895-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d895-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d895-110">Координаты x и y верхнего левого угла клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="3d895-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="3d895-111">Слово низкого порядка содержит координату по оси x, в то время как слово с высоким порядком содержит координату y.</span><span class="sxs-lookup"><span data-stu-id="3d895-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d895-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d895-112">Return value</span></span>

<span data-ttu-id="3d895-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="3d895-113">Type: **LRESULT**</span></span>

<span data-ttu-id="3d895-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3d895-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d895-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d895-115">Remarks</span></span>

<span data-ttu-id="3d895-116">Параметры задаются в экранных координатах для перекрывающихся и всплывающих окон, а также в координатах родительского клиента для дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="3d895-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="3d895-117">В следующем примере показано, как получить расположение из параметра *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3d895-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="3d895-118">Можно также использовать макрос [**макепоинтс**](/windows/win32/api/wingdi/nf-wingdi-makepoints) для преобразования параметра *lParam* в структуру [**points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3d895-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="3d895-119">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщения **WM \_ size** и **WM \_ Move** при обработке сообщения [**WM \_ виндовпосчанжед**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="3d895-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="3d895-120">Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="3d895-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d895-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3d895-121">Requirements</span></span>



| <span data-ttu-id="3d895-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3d895-122">Requirement</span></span> | <span data-ttu-id="3d895-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3d895-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d895-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d895-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d895-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d895-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d895-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d895-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d895-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d895-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d895-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d895-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d895-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d895-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d895-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d895-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d895-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3d895-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="3d895-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d895-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3d895-133">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d895-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3d895-134">**WM \_ виндовпосчанжед**</span><span class="sxs-lookup"><span data-stu-id="3d895-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="3d895-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3d895-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d895-136">Windows</span><span class="sxs-lookup"><span data-stu-id="3d895-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="3d895-137">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3d895-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3d895-138">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="3d895-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="3d895-139">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d895-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
