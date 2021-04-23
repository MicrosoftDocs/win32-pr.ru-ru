---
title: Сообщение WM_DPICHANGED (WinUser. h)
description: Посылается при изменении эффективных точек на дюйм для окна.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED высокое разрешение для сообщения
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802525"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="6c8e9-104">\_Сообщение DPICHANGED WM</span><span class="sxs-lookup"><span data-stu-id="6c8e9-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="6c8e9-105">Посылается при изменении эффективных точек на дюйм для окна.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="6c8e9-106">Значение DPI является коэффициентом масштабирования для окна.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="6c8e9-107">Существует несколько событий, которые могут привести к изменению DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="6c8e9-108">В следующем списке указаны возможные причины изменения DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="6c8e9-109">Окно перемещается на новый монитор с разными DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="6c8e9-110">Значение DPI монитора, размещающего окно, изменяется.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="6c8e9-111">Текущее значение DPI для окна всегда равно последнему значению DPI, отправленному **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="6c8e9-112">Это коэффициент масштабирования, в течение которого окно должно масштабироваться для потоков, которые знают об изменениях DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="6c8e9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c8e9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8e9-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c8e9-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8e9-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) параметра *wParam* содержит значение оси Y нового значения DPI окна.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="6c8e9-116">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) параметра *wParam* содержит значение оси X нового значения DPI окна.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="6c8e9-117">Например, 96, 120, 144 или 192.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="6c8e9-118">Значения оси X и оси Y идентичны для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="6c8e9-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c8e9-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8e9-120">Указатель на структуру [**Rect**](/windows/desktop/api/windef/ns-windef-rect) , которая предоставляет предлагаемый размер и расположение текущего окна, масштабированного для новых точек на дюйм.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="6c8e9-121">Ожидание заключается в том, что приложения будут перемещать окна и изменять их размер в зависимости от предложений, предоставляемых параметром *lParam* при обработке этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8e9-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c8e9-122">Return value</span></span>

<span data-ttu-id="6c8e9-123">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8e9-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c8e9-124">Remarks</span></span>

<span data-ttu-id="6c8e9-125">Это сообщение относится только к **процессам \_ с \_ отслеживанием \_ dpi \_** на уровне монитора или по dpi для потоков, **\_ \_ \_ \_ поддерживающих мониторинг** .</span><span class="sxs-lookup"><span data-stu-id="6c8e9-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="6c8e9-126">Оно может быть получено при определенных изменениях DPI, если окно или процесс верхнего уровня выполняется как неточное **разрешение dpi** или **учитывается dpi системы**, но в таких ситуациях его можно спокойно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="6c8e9-127">Дополнительные сведения о различных типах осведомленности см. в разделе [**Обработка \_ dpi \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) и отслеживание [**dpi \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="6c8e9-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="6c8e9-128">Более старые версии Windows должны соответствовать требованиям к DPI на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="6c8e9-129">Эти приложения используют сведения о **\_ dpi \_ процесса**.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="6c8e9-130">В настоящее время отслеживание DPI привязано к потокам и отдельным окнам, а не ко всему приложению.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="6c8e9-131">Эти приложения используют **\_ Распознавание dpi**.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="6c8e9-132">При масштабировании приложения необходимо использовать либо ось X, либо значение по оси Y, так как они совпадают.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="6c8e9-133">Чтобы правильно обрабатывалось это сообщение, необходимо изменить размер и расположение окна на основе предложений *lParam* и [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="6c8e9-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="6c8e9-134">Если этого не сделать, окно будет увеличиваться или уменьшаться относительно всех остальных элементов на новом мониторе.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="6c8e9-135">Например, если пользователь использует несколько мониторов и перетащилт окно с монитора 96 DPI на монитор 192, размер окна будет вдвое выше, чем у других элементов монитора 192 DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="6c8e9-136">Базовое значение DPI определяется как **пользовательское \_ по умолчанию \_ \_ dpi** , значение которого равно 96.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="6c8e9-137">Чтобы определить коэффициент масштабирования для монитора, Возьмите значение DPI и разделите его по значению **\_ \_ \_ DPI по умолчанию на экране пользователя**.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="6c8e9-138">В следующей таблице приведены некоторые примеры значений DPI и связанные коэффициенты масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="6c8e9-139">Значение DPI</span><span class="sxs-lookup"><span data-stu-id="6c8e9-139">DPI value</span></span> | <span data-ttu-id="6c8e9-140">Процент масштабирования</span><span class="sxs-lookup"><span data-stu-id="6c8e9-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="6c8e9-141">96</span><span class="sxs-lookup"><span data-stu-id="6c8e9-141">96</span></span>        | <span data-ttu-id="6c8e9-142">100 %</span><span class="sxs-lookup"><span data-stu-id="6c8e9-142">100%</span></span>               |
| <span data-ttu-id="6c8e9-143">120</span><span class="sxs-lookup"><span data-stu-id="6c8e9-143">120</span></span>       | <span data-ttu-id="6c8e9-144">125%</span><span class="sxs-lookup"><span data-stu-id="6c8e9-144">125%</span></span>               |
| <span data-ttu-id="6c8e9-145">144</span><span class="sxs-lookup"><span data-stu-id="6c8e9-145">144</span></span>       | <span data-ttu-id="6c8e9-146">150%</span><span class="sxs-lookup"><span data-stu-id="6c8e9-146">150%</span></span>               |
| <span data-ttu-id="6c8e9-147">192</span><span class="sxs-lookup"><span data-stu-id="6c8e9-147">192</span></span>       | <span data-ttu-id="6c8e9-148">200 %</span><span class="sxs-lookup"><span data-stu-id="6c8e9-148">200%</span></span>               |



 

<span data-ttu-id="6c8e9-149">В следующем примере показан пример обработчика изменений DPI.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="6c8e9-150">Следующий код линейно масштабирует значение с 100% (96 точек на дюйм) до произвольного DPI, определенного в *g \_ dpi*.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="6c8e9-151">Альтернативный способ масштабирования значения — преобразование значения DPI в коэффициент масштабирования и его использование.</span><span class="sxs-lookup"><span data-stu-id="6c8e9-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="6c8e9-152">Требования</span><span class="sxs-lookup"><span data-stu-id="6c8e9-152">Requirements</span></span>



| <span data-ttu-id="6c8e9-153">Требование</span><span class="sxs-lookup"><span data-stu-id="6c8e9-153">Requirement</span></span> | <span data-ttu-id="6c8e9-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6c8e9-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8e9-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c8e9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8e9-156">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c8e9-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c8e9-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c8e9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8e9-158">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c8e9-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6c8e9-159">Header</span><span class="sxs-lookup"><span data-stu-id="6c8e9-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8e9-160"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8e9-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8e9-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c8e9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8e9-162">**\_Поддержка dpi**</span><span class="sxs-lookup"><span data-stu-id="6c8e9-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="6c8e9-163">**\_поддержка обработки dpi \_**</span><span class="sxs-lookup"><span data-stu-id="6c8e9-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

