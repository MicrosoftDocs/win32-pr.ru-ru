---
title: Сообщение WM_NCLBUTTONDOWN (Winuser. h)
description: Посылается, когда пользователь нажимает на левую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: fca6d9ec-c549-4c82-9a80-15471481f876
keywords:
- WM_NCLBUTTONDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c31a6feded21d3a43d7b87c0de6a03724dcf2c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801954"
---
# <a name="wm_nclbuttondown-message"></a><span data-ttu-id="b2495-106">\_Сообщение НКЛБУТТОНДОВН WM</span><span class="sxs-lookup"><span data-stu-id="b2495-106">WM\_NCLBUTTONDOWN message</span></span>

<span data-ttu-id="b2495-107">Посылается, когда пользователь нажимает на левую кнопку мыши, когда курсор находится внутри неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="b2495-107">Posted when the user presses the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="b2495-108">Это сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="b2495-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="b2495-109">Если окно захвачено мышью, это сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="b2495-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="b2495-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b2495-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDOWN                0x00A1
```



## <a name="parameters"></a><span data-ttu-id="b2495-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2495-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2495-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2495-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2495-113">Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="b2495-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="b2495-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="b2495-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="b2495-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2495-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2495-116">Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="b2495-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="b2495-117">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="b2495-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2495-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2495-118">Return value</span></span>

<span data-ttu-id="b2495-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="b2495-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2495-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2495-120">Remarks</span></span>

<span data-ttu-id="b2495-121">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) проверяет указанную точку, чтобы найти расположение курсора и выполняет соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="b2495-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="b2495-122">При необходимости **дефвиндовпрок** отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.</span><span class="sxs-lookup"><span data-stu-id="b2495-122">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="b2495-123">Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b2495-123">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="b2495-124">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="b2495-124">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b2495-125">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="b2495-125">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2495-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b2495-126">Requirements</span></span>



| <span data-ttu-id="b2495-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b2495-127">Requirement</span></span> | <span data-ttu-id="b2495-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b2495-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2495-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2495-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2495-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2495-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2495-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2495-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2495-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2495-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2495-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2495-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2495-134"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2495-134"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2495-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2495-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2495-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b2495-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2495-137">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="b2495-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b2495-138">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b2495-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b2495-139">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="b2495-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b2495-140">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="b2495-140">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="b2495-141">**WM \_ нклбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="b2495-141">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="b2495-142">**WM \_ нклбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="b2495-142">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b2495-143">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="b2495-143">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="b2495-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b2495-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2495-145">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="b2495-145">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b2495-146">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b2495-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b2495-147">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="b2495-147">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b2495-148">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2495-148">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

