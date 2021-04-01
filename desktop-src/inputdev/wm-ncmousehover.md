---
title: Сообщение WM_NCMOUSEHOVER (Winuser. h)
description: Отправляется в окно при наведении курсора на неклиентскую область окна в течение периода времени, указанного в предыдущем вызове метода TrackMouseEven.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071938"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="2d555-104">\_Сообщение НКМАУСЕХОВЕР WM</span><span class="sxs-lookup"><span data-stu-id="2d555-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="2d555-105">Отправляется в окно при наведении курсора на неклиентскую область окна в течение периода времени, указанного в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="2d555-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="2d555-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2d555-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="2d555-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d555-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d555-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d555-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d555-109">Значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="2d555-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="2d555-110">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="2d555-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="2d555-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d555-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d555-112">Структура [**точек**](/previous-versions//dd162808(v=vs.85)) , содержащая координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="2d555-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="2d555-113">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="2d555-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d555-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d555-114">Return value</span></span>

<span data-ttu-id="2d555-115">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="2d555-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d555-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d555-116">Remarks</span></span>

<span data-ttu-id="2d555-117">Отслеживание наведения при наведении останавливается при создании сообщения.</span><span class="sxs-lookup"><span data-stu-id="2d555-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="2d555-118">Приложение должно вызвать [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) еще раз, если требуется дальнейшее отслеживание поведения при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="2d555-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="2d555-119">Можно также использовать макросы [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) и [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) для извлечения значений координат X и y из *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2d555-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="2d555-120">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="2d555-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="2d555-121">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="2d555-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d555-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2d555-122">Requirements</span></span>



| <span data-ttu-id="2d555-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2d555-123">Requirement</span></span> | <span data-ttu-id="2d555-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2d555-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d555-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d555-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d555-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d555-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d555-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d555-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d555-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d555-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d555-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2d555-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d555-130"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d555-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d555-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d555-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d555-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2d555-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d555-133">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="2d555-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2d555-134">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2d555-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2d555-135">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="2d555-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2d555-136">**TrackMouseEven**</span><span class="sxs-lookup"><span data-stu-id="2d555-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="2d555-137">**TRACKMOUSEEVEN**</span><span class="sxs-lookup"><span data-stu-id="2d555-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="2d555-138">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="2d555-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="2d555-139">**WM \_ маусеховер**</span><span class="sxs-lookup"><span data-stu-id="2d555-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="2d555-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2d555-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2d555-141">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="2d555-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="2d555-142">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="2d555-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2d555-143">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="2d555-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="2d555-144">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d555-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

