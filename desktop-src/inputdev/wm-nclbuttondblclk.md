---
title: Сообщение WM_NCLBUTTONDBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды щелкает левую кнопку мыши, когда курсор находится внутри неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- WM_NCLBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135631"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="3b746-106">\_Сообщение НКЛБУТТОНДБЛКЛК WM</span><span class="sxs-lookup"><span data-stu-id="3b746-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="3b746-107">Посылается, когда пользователь дважды щелкает левую кнопку мыши, когда курсор находится внутри неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="3b746-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="3b746-108">Это сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="3b746-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="3b746-109">Если окно захвачено мышью, это сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="3b746-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="3b746-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b746-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="3b746-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b746-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b746-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b746-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b746-113">Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="3b746-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="3b746-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="3b746-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="3b746-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b746-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b746-116">Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="3b746-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="3b746-117">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="3b746-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b746-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b746-118">Return value</span></span>

<span data-ttu-id="3b746-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3b746-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b746-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b746-120">Remarks</span></span>

<span data-ttu-id="3b746-121">Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="3b746-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="3b746-122">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="3b746-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="3b746-123">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="3b746-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="3b746-124">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) проверяет указанную точку для определения расположения курсора и выполняет соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="3b746-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="3b746-125">При необходимости **дефвиндовпрок** отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.</span><span class="sxs-lookup"><span data-stu-id="3b746-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="3b746-126">Для получения сообщений **\_ нклбуттондблклк WM** в окне не требуется стиль **CS \_ дблклкс** .</span><span class="sxs-lookup"><span data-stu-id="3b746-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="3b746-127">Система создает сообщение **WM \_ нклбуттондблклк** , когда пользователь нажимает, отпускает и снова нажимает левую кнопку мыши в пределах предельного времени двойного щелчка системы.</span><span class="sxs-lookup"><span data-stu-id="3b746-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="3b746-128">Двойной щелчок левой кнопки мыши на самом деле приводит к созданию четырех сообщений: [**WM \_ нклбуттондовн**](wm-nclbuttondown.md), [**WM \_ Нклбуттонуп**](wm-nclbuttonup.md), **WM \_ нклбуттондблклк** и **WM \_ нклбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="3b746-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b746-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3b746-129">Requirements</span></span>



| <span data-ttu-id="3b746-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3b746-130">Requirement</span></span> | <span data-ttu-id="3b746-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3b746-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b746-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b746-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3b746-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b746-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3b746-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b746-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3b746-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b746-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3b746-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b746-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b746-137"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b746-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b746-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b746-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b746-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3b746-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b746-140">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="3b746-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="3b746-141">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="3b746-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="3b746-142">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="3b746-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="3b746-143">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="3b746-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="3b746-144">**WM \_ нклбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="3b746-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="3b746-145">**WM \_ нклбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="3b746-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="3b746-146">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="3b746-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="3b746-147">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3b746-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3b746-148">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="3b746-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="3b746-149">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3b746-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3b746-150">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="3b746-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="3b746-151">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b746-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

