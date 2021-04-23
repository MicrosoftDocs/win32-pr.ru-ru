---
title: Сообщение WM_NCMBUTTONDOWN (Winuser. h)
description: Посылается, когда пользователь нажимает среднюю кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: 0aa86fc6-43e9-4356-a4c1-e3f687dc2884
keywords:
- WM_NCMBUTTONDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b7d6a0f43612b9a8877723fb62f87e7516529c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801948"
---
# <a name="wm_ncmbuttondown-message"></a><span data-ttu-id="d7397-106">\_Сообщение НКМБУТТОНДОВН WM</span><span class="sxs-lookup"><span data-stu-id="d7397-106">WM\_NCMBUTTONDOWN message</span></span>

<span data-ttu-id="d7397-107">Посылается, когда пользователь нажимает среднюю кнопку мыши, когда курсор находится внутри неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="d7397-107">Posted when the user presses the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="d7397-108">Это сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="d7397-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="d7397-109">Если окно захвачено мышью, это сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="d7397-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="d7397-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d7397-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONDOWN                0x00A7
```



## <a name="parameters"></a><span data-ttu-id="d7397-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7397-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7397-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7397-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7397-113">Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="d7397-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="d7397-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="d7397-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="d7397-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7397-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7397-116">Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="d7397-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="d7397-117">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="d7397-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7397-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7397-118">Return value</span></span>

<span data-ttu-id="d7397-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="d7397-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7397-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7397-120">Remarks</span></span>

<span data-ttu-id="d7397-121">Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="d7397-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="d7397-122">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="d7397-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="d7397-123">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="d7397-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="d7397-124">Если это уместно, система отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.</span><span class="sxs-lookup"><span data-stu-id="d7397-124">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7397-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d7397-125">Requirements</span></span>



| <span data-ttu-id="d7397-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d7397-126">Requirement</span></span> | <span data-ttu-id="d7397-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d7397-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7397-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7397-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d7397-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7397-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7397-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7397-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d7397-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7397-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7397-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7397-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7397-133"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7397-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7397-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7397-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7397-135">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d7397-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7397-136">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="d7397-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d7397-137">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="d7397-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="d7397-138">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="d7397-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="d7397-139">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="d7397-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="d7397-140">**WM \_ нкмбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="d7397-140">**WM\_NCMBUTTONDBLCLK**</span></span>](wm-ncmbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="d7397-141">**WM \_ нкмбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="d7397-141">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
</dt> <dt>

[<span data-ttu-id="d7397-142">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="d7397-142">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="d7397-143">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d7397-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7397-144">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="d7397-144">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="d7397-145">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="d7397-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d7397-146">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="d7397-146">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="d7397-147">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7397-147">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

