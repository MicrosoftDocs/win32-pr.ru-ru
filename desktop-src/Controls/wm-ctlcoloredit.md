---
title: Сообщение WM_CTLCOLOREDIT (Winuser. h)
description: Элемент управления "поле ввода", который не предназначен только для чтения или отключен, отправляет \_ сообщение WM ктлколоредит в его родительское окно, когда элемент управления собирается для рисования.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- Элементы управления Windows для WM_CTLCOLOREDIT сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489003"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="19cfe-104">\_Сообщение КТЛКОЛОРЕДИТ WM</span><span class="sxs-lookup"><span data-stu-id="19cfe-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="19cfe-105">Элемент управления "поле ввода", который не предназначен только для чтения или отключен, отправляет сообщение **WM \_ ктлколоредит** в его родительское окно, когда элемент управления собирается для рисования.</span><span class="sxs-lookup"><span data-stu-id="19cfe-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="19cfe-106">При ответе на это сообщение родительское окно может использовать указанный маркер контекста устройства, чтобы задать цвета текста и фона для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="19cfe-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="19cfe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="19cfe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cfe-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19cfe-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19cfe-109">Маркер контекста устройства для окна элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="19cfe-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="19cfe-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19cfe-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19cfe-111">Маркер для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="19cfe-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cfe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19cfe-112">Return value</span></span>

<span data-ttu-id="19cfe-113">Если приложение обрабатывает это сообщение, оно должно возвращать дескриптор кисти.</span><span class="sxs-lookup"><span data-stu-id="19cfe-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="19cfe-114">Система использует кисть для рисования фона элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="19cfe-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="19cfe-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19cfe-115">Remarks</span></span>

<span data-ttu-id="19cfe-116">Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть.</span><span class="sxs-lookup"><span data-stu-id="19cfe-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="19cfe-117">Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.</span><span class="sxs-lookup"><span data-stu-id="19cfe-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="19cfe-118">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="19cfe-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="19cfe-119">Элементы управления "изменение" только для чтения или "отключено" не отправляют сообщение **\_ ктлколоредит WM** ; вместо этого они отправляют сообщение [**WM \_ ктлколорстатик**](wm-ctlcolorstatic.md) .</span><span class="sxs-lookup"><span data-stu-id="19cfe-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="19cfe-120">Сообщение **WM \_ ктлколоредит** никогда не отправляется между потоками, оно отправляется только в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="19cfe-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="19cfe-121">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="19cfe-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="19cfe-122">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19cfe-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="19cfe-123">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="19cfe-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="19cfe-124">**Расширенное редактирование:** Это сообщение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="19cfe-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="19cfe-125">Чтобы задать цвет фона для элемента управления Rich Edit, используйте сообщение [**EM \_ сетбкгндколор**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="19cfe-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cfe-126">Требования</span><span class="sxs-lookup"><span data-stu-id="19cfe-126">Requirements</span></span>



| <span data-ttu-id="19cfe-127">Требование</span><span class="sxs-lookup"><span data-stu-id="19cfe-127">Requirement</span></span> | <span data-ttu-id="19cfe-128">Значение</span><span class="sxs-lookup"><span data-stu-id="19cfe-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cfe-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19cfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="19cfe-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19cfe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19cfe-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19cfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="19cfe-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19cfe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19cfe-133">Header</span><span class="sxs-lookup"><span data-stu-id="19cfe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="19cfe-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19cfe-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19cfe-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19cfe-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="19cfe-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="19cfe-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19cfe-137">**EM \_ сетбкгндколор**</span><span class="sxs-lookup"><span data-stu-id="19cfe-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="19cfe-138">**WM \_ ктлколорстатик**</span><span class="sxs-lookup"><span data-stu-id="19cfe-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="19cfe-139">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="19cfe-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="19cfe-140">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="19cfe-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="19cfe-141">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="19cfe-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="19cfe-142">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="19cfe-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

