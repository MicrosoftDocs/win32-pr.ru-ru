---
title: Сообщение WM_NCMBUTTONDBLCLK (Winuser. h)
description: Размещается, когда пользователь дважды щелкает среднюю кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- WM_NCMBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801949"
---
# <a name="wm_ncmbuttondblclk-message"></a><span data-ttu-id="15abe-106">\_Сообщение НКМБУТТОНДБЛКЛК WM</span><span class="sxs-lookup"><span data-stu-id="15abe-106">WM\_NCMBUTTONDBLCLK message</span></span>

<span data-ttu-id="15abe-107">Размещается, когда пользователь дважды щелкает среднюю кнопку мыши, когда курсор находится внутри неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="15abe-107">Posted when the user double-clicks the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="15abe-108">Это сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="15abe-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="15abe-109">Если окно захвачено мышью, это сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="15abe-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="15abe-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="15abe-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a><span data-ttu-id="15abe-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="15abe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15abe-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15abe-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15abe-113">Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="15abe-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="15abe-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="15abe-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="15abe-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15abe-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15abe-116">Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="15abe-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="15abe-117">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="15abe-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15abe-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15abe-118">Return value</span></span>

<span data-ttu-id="15abe-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="15abe-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="15abe-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15abe-120">Remarks</span></span>

<span data-ttu-id="15abe-121">Для получения сообщений **\_ нкмбуттондблклк WM** в окне не требуется стиль **CS \_ дблклкс** .</span><span class="sxs-lookup"><span data-stu-id="15abe-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCMBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="15abe-122">Система создает сообщение **WM \_ нкмбуттондблклк** , когда пользователь нажимает, отпускает и снова нажимает среднюю кнопку мыши в пределах предельного времени двойного щелчка системы.</span><span class="sxs-lookup"><span data-stu-id="15abe-122">The system generates a **WM\_NCMBUTTONDBLCLK** message when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="15abe-123">Двойной щелчок средней кнопки мыши на самом деле приводит к созданию четырех сообщений: [**WM \_ нкмбуттондовн**](wm-ncmbuttondown.md), [**WM \_ Нкмбуттонуп**](wm-ncmbuttonup.md), **WM \_ нкмбуттондблклк** и **WM \_ нкмбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="15abe-123">Double-clicking the middle mouse button actually generates four messages: [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), **WM\_NCMBUTTONDBLCLK**, and **WM\_NCMBUTTONUP** again.</span></span>

<span data-ttu-id="15abe-124">Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="15abe-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="15abe-125">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="15abe-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="15abe-126">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="15abe-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="15abe-127">Если это уместно, система отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.</span><span class="sxs-lookup"><span data-stu-id="15abe-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="15abe-128">Требования</span><span class="sxs-lookup"><span data-stu-id="15abe-128">Requirements</span></span>



| <span data-ttu-id="15abe-129">Требование</span><span class="sxs-lookup"><span data-stu-id="15abe-129">Requirement</span></span> | <span data-ttu-id="15abe-130">Значение</span><span class="sxs-lookup"><span data-stu-id="15abe-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15abe-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15abe-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15abe-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15abe-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15abe-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15abe-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15abe-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15abe-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15abe-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15abe-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="15abe-136"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15abe-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15abe-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15abe-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="15abe-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="15abe-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15abe-139">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="15abe-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="15abe-140">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="15abe-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="15abe-141">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="15abe-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="15abe-142">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="15abe-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="15abe-143">**WM \_ нкмбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="15abe-143">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="15abe-144">**WM \_ нкмбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="15abe-144">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
</dt> <dt>

[<span data-ttu-id="15abe-145">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="15abe-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="15abe-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="15abe-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15abe-147">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="15abe-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="15abe-148">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="15abe-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="15abe-149">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="15abe-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="15abe-150">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15abe-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

