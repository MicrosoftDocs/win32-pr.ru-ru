---
title: Сообщение WM_CTLCOLORSTATIC (Winuser. h)
description: Статический элемент управления или элемент управления "поле ввода", который доступен только для чтения или отключен, отправляет \_ сообщение WM ктлколорстатик в свое родительское окно при прорисовке элемента управления.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- Элементы управления Windows для WM_CTLCOLORSTATIC сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802176"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="cf4e4-104">\_Сообщение КТЛКОЛОРСТАТИК WM</span><span class="sxs-lookup"><span data-stu-id="cf4e4-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="cf4e4-105">Статический элемент управления или элемент управления "поле ввода", который доступен только для чтения или отключен, отправляет сообщение **WM \_ ктлколорстатик** в свое родительское окно при прорисовке элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="cf4e4-106">При ответе на это сообщение родительское окно может использовать указанный маркер контекста устройства, чтобы задать цвет переднего плана текста и фона статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="cf4e4-107">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cf4e4-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cf4e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf4e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf4e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf4e4-110">Обработайте контекст устройства для окна статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="cf4e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf4e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf4e4-112">Обработчик статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4e4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf4e4-113">Return value</span></span>

<span data-ttu-id="cf4e4-114">Если приложение обрабатывает это сообщение, возвращаемое значение является дескриптором кисти, используемой системой для рисования фона статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4e4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf4e4-115">Remarks</span></span>

<span data-ttu-id="cf4e4-116">Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="cf4e4-117">Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="cf4e4-118">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="cf4e4-119">Можно задать цвет фона текста отключенного элемента управления "поле ввода", но нельзя задать цвет переднего плана текста.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="cf4e4-120">Система всегда использует цвет \_ грайтекст.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="cf4e4-121">Изменение элементов управления, которые не предназначены только для чтения или отключены, не отправляют сообщение **\_ ктлколорстатик WM** ; вместо этого они отправляют сообщение [**WM \_ ктлколоредит**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4e4-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="cf4e4-122">Сообщение **WM \_ ктлколорстатик** никогда не отправляется между потоками; оно отправляется только в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="cf4e4-123">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="cf4e4-124">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="cf4e4-125">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="cf4e4-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="cf4e4-126">Examples</span></span>

<span data-ttu-id="cf4e4-127">В следующем примере C++ показано, как задать цвет переднего плана и фона текста статического элемента управления в ответ на сообщение **\_ ктлколорстатик WM** .</span><span class="sxs-lookup"><span data-stu-id="cf4e4-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="cf4e4-128">`hbrBkgnd`Переменная является статической переменной **хбруш** , которая инициализируется значением NULL, и сохраняет кисть фона между вызовами **WM \_ ктлколорстатик**.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="cf4e4-129">Эта кисть должна быть уничтожена вызовом функции [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) , когда она больше не нужна, как правило, при уничтожении связанного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="cf4e4-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="cf4e4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cf4e4-130">Requirements</span></span>



| <span data-ttu-id="cf4e4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cf4e4-131">Requirement</span></span> | <span data-ttu-id="cf4e4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cf4e4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4e4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf4e4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4e4-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf4e4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf4e4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf4e4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4e4-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf4e4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf4e4-137">Header</span><span class="sxs-lookup"><span data-stu-id="cf4e4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf4e4-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf4e4-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4e4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf4e4-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf4e4-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf4e4-141">**WM \_ ктлколорбтн**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="cf4e4-142">**WM \_ ктлколоредит**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="cf4e4-143">**WM \_ ктлколорлистбокс**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="cf4e4-144">**WM \_ ктлколорскроллбар**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="cf4e4-145">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cf4e4-146">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cf4e4-147">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="cf4e4-148">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="cf4e4-149">**WM \_ ктлколордлг**</span><span class="sxs-lookup"><span data-stu-id="cf4e4-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

