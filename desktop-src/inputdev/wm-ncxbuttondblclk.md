---
title: Сообщение WM_NCXBUTTONDBLCLK (Winuser. h)
description: Публикуется, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в неклиентской области окна. Это сообщение отправляется в окно, содержащее курсор. Если окно захвачено мышью, это сообщение не отправляется.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- WM_NCXBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710531"
---
# <a name="wm_ncxbuttondblclk-message"></a><span data-ttu-id="54920-106">\_Сообщение НККСБУТТОНДБЛКЛК WM</span><span class="sxs-lookup"><span data-stu-id="54920-106">WM\_NCXBUTTONDBLCLK message</span></span>

<span data-ttu-id="54920-107">Публикуется, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в неклиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="54920-107">Posted when the user double-clicks the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="54920-108">Это сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="54920-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="54920-109">Если окно захвачено мышью, это сообщение не отправляется.</span><span class="sxs-lookup"><span data-stu-id="54920-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="54920-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54920-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a><span data-ttu-id="54920-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="54920-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54920-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54920-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54920-113">Слово нижнего порядка указывает значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , из обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="54920-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="54920-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="54920-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="54920-115">Слово в высоком порядке указывает на то, какая кнопка была двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="54920-115">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="54920-116">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="54920-116">It can be one of the following values.</span></span>



| <span data-ttu-id="54920-117">Значение</span><span class="sxs-lookup"><span data-stu-id="54920-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="54920-118">Значение</span><span class="sxs-lookup"><span data-stu-id="54920-118">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="54920-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="54920-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="54920-120">Первая кнопка X была двойным щелчком...</span><span class="sxs-lookup"><span data-stu-id="54920-120">The first X button was double-clicked..</span></span><br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="54920-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="54920-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="54920-122">Вторая кнопка X была двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="54920-122">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54920-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54920-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54920-124">Указатель на структуру [**точек**](/previous-versions//dd162808(v=vs.85)) , которая содержит координаты x и y курсора.</span><span class="sxs-lookup"><span data-stu-id="54920-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="54920-125">Координаты задаются относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="54920-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54920-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54920-126">Return value</span></span>

<span data-ttu-id="54920-127">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="54920-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="54920-128">Дополнительные сведения об обработке возвращаемого значения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="54920-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="54920-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54920-129">Remarks</span></span>

<span data-ttu-id="54920-130">Используйте следующий код, чтобы получить сведения в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="54920-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="54920-131">Для получения координат x и y из *lParam* можно также использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="54920-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="54920-132">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="54920-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="54920-133">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="54920-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="54920-134">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) проверяет указанную точку на получение позиции курсора и выполняет соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="54920-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="54920-135">При необходимости оно отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно.</span><span class="sxs-lookup"><span data-stu-id="54920-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="54920-136">Для получения сообщений **\_ нкксбуттондблклк WM** в окне не требуется стиль **CS \_ дблклкс** .</span><span class="sxs-lookup"><span data-stu-id="54920-136">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCXBUTTONDBLCLK** messages.</span></span> <span data-ttu-id="54920-137">Система создает сообщение **WM \_ нкксбуттондблклк** , когда пользователь нажимает, отпускает и снова нажимает кнопку X в пределах предельного времени двойного щелчка системы.</span><span class="sxs-lookup"><span data-stu-id="54920-137">The system generates a **WM\_NCXBUTTONDBLCLK** message when the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="54920-138">Двойной щелчок одной из этих кнопок на самом деле приводит к созданию четырех сообщений: [**WM \_ нкксбуттондовн**](wm-ncxbuttondown.md), [**WM \_ Нкксбуттонуп**](wm-ncxbuttonup.md), **WM \_ нкксбуттондблклк** и **WM \_ нкксбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="54920-138">Double-clicking one of these buttons actually generates four messages: [**WM\_NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM\_NCXBUTTONUP**](wm-ncxbuttonup.md), **WM\_NCXBUTTONDBLCLK**, and **WM\_NCXBUTTONUP** again.</span></span>

<span data-ttu-id="54920-139">В отличие от [**сообщений \_ WM нклбуттондблклк**](wm-nclbuttondblclk.md), [**WM \_ нкмбуттондблклк**](wm-ncmbuttondblclk.md)и [**WM \_ нкрбуттондблклк**](wm-ncrbuttondblclk.md) , приложение должно вернуть **значение true** из этого сообщения, если оно обрабатывает его.</span><span class="sxs-lookup"><span data-stu-id="54920-139">Unlike the [**WM\_NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM\_NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md), and [**WM\_NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="54920-140">Это позволит программному обеспечению имитировать это сообщение в системах Windows более ранних, чем Windows 2000, чтобы определить, обрабатывало ли это сообщение процедура окна или вызываемая [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для его обработки.</span><span class="sxs-lookup"><span data-stu-id="54920-140">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="54920-141">Требования</span><span class="sxs-lookup"><span data-stu-id="54920-141">Requirements</span></span>



| <span data-ttu-id="54920-142">Требование</span><span class="sxs-lookup"><span data-stu-id="54920-142">Requirement</span></span> | <span data-ttu-id="54920-143">Значение</span><span class="sxs-lookup"><span data-stu-id="54920-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54920-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54920-144">Minimum supported client</span></span><br/> | <span data-ttu-id="54920-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="54920-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54920-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54920-146">Minimum supported server</span></span><br/> | <span data-ttu-id="54920-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="54920-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54920-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="54920-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="54920-149"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54920-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54920-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54920-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="54920-151">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="54920-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54920-152">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="54920-152">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="54920-153">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="54920-153">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="54920-154">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="54920-154">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="54920-155">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="54920-155">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="54920-156">**WM \_ нкксбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="54920-156">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="54920-157">**WM \_ нкксбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="54920-157">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="54920-158">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="54920-158">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="54920-159">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="54920-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54920-160">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="54920-160">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="54920-161">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="54920-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="54920-162">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="54920-162">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="54920-163">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54920-163">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

