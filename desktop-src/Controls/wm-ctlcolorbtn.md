---
title: Сообщение WM_CTLCOLORBTN (Winuser. h)
description: Сообщение WM \_ ктлколорбтн отправляется в родительское окно кнопки перед рисованием кнопки. Родительское окно может изменять цвета текста и фона кнопки. Однако только рисуемые владельцем кнопки реагируют на родительское окно, обрабатывающее это сообщение.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- Элементы управления Windows для WM_CTLCOLORBTN сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988184"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="3c2c7-106">\_Сообщение КТЛКОЛОРБТН WM</span><span class="sxs-lookup"><span data-stu-id="3c2c7-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="3c2c7-107">Сообщение **WM \_ ктлколорбтн** отправляется в родительское окно кнопки перед рисованием кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="3c2c7-108">Родительское окно может изменять цвета текста и фона кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="3c2c7-109">Однако только рисуемые владельцем кнопки реагируют на родительское окно, обрабатывающее это сообщение.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3c2c7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c2c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2c7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c2c7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c2c7-112">Контекст **HDC** , задающий маркер для контекста вывода кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="3c2c7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c2c7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c2c7-114">**HWND** , указывающий дескриптор кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c2c7-115">Return value</span></span>

<span data-ttu-id="3c2c7-116">Если приложение обрабатывает это сообщение, оно должно возвращать маркер кисти.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="3c2c7-117">Система использует кисть для рисования фона кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c2c7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c2c7-118">Remarks</span></span>

<span data-ttu-id="3c2c7-119">Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="3c2c7-120">Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="3c2c7-121">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="3c2c7-122">Кнопки с [**\_ кнопками BS**](button-styles.md), [**\_ дефпушбуттон**](button-styles.md)или [**BS \_ пушлике**](button-styles.md) не используют возвращенную кисть.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="3c2c7-123">Кнопки с этими стилями всегда отображаются с системными цветами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="3c2c7-124">Для нажатия кнопок рисования требуется несколько различных кистей, выделения и тени, но сообщение **WM \_ ктлколорбтн** позволяет вернуть только одну кисть.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="3c2c7-125">Чтобы предоставить пользовательский внешний вид для кнопок, используйте рисуемые владельцем кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="3c2c7-126">Дополнительные сведения см. в разделе [Создание элементов управления Owner-Drawn](user-controls-intro.md).</span><span class="sxs-lookup"><span data-stu-id="3c2c7-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="3c2c7-127">Сообщение **WM \_ ктлколорбтн** никогда не передается между потоками.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="3c2c7-128">Он отправляется только в пределах одного потока.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-128">It is sent only within one thread.</span></span>

<span data-ttu-id="3c2c7-129">Цвет текста флажка или переключателя применяется к полю или кнопке, его галочке и тексту.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="3c2c7-130">Прямоугольник фокуса для этих кнопок остается цветом системы по умолчанию (обычно черным).</span><span class="sxs-lookup"><span data-stu-id="3c2c7-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="3c2c7-131">Цвет текста поля группы применяется к тексту, но не к линии, определяющей поле.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="3c2c7-132">Цвет текста кнопки «кнопка» применяется только к прямоугольнику фокуса; Он не влияет на цвет текста.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="3c2c7-133">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="3c2c7-134">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="3c2c7-135">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3c2c7-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2c7-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3c2c7-136">Requirements</span></span>



| <span data-ttu-id="3c2c7-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3c2c7-137">Requirement</span></span> | <span data-ttu-id="3c2c7-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3c2c7-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2c7-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c2c7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2c7-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c2c7-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c2c7-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c2c7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2c7-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c2c7-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3c2c7-143">Header</span><span class="sxs-lookup"><span data-stu-id="3c2c7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2c7-144"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c7-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2c7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c2c7-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c2c7-146">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3c2c7-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3c2c7-147">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="3c2c7-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="3c2c7-148">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="3c2c7-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

