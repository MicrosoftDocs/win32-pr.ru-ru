---
title: Сообщение WM_CONTEXTMENU (Winuser. h)
description: Уведомляет окно, что пользователь щелкнул правой кнопкой мыши в окне.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710479"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="06ba0-104">\_Сообщение WM CONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="06ba0-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="06ba0-105">Уведомляет окно о том, что пользователь хочет отобразить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="06ba0-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="06ba0-106">Пользователь мог щелкнуть правой кнопкой мыши в окне, нажать Shift + F10 или нажал клавишу приложения (раздел контекстного меню) на некоторых клавиатурах.</span><span class="sxs-lookup"><span data-stu-id="06ba0-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="06ba0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06ba0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ba0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06ba0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06ba0-109">Указатель на окно, в котором пользователь щелкнул правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="06ba0-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="06ba0-110">Это может быть дочернее окно окна, получающего сообщение.</span><span class="sxs-lookup"><span data-stu-id="06ba0-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="06ba0-111">Дополнительные сведения об обработке этого сообщения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="06ba0-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="06ba0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06ba0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06ba0-113">Слово нижнего порядка задает горизонтальное расположение курсора в экранных координатах во время щелчка мышью.</span><span class="sxs-lookup"><span data-stu-id="06ba0-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="06ba0-114">Слово в высоком порядке задает вертикальное расположение курсора в экранных координатах во время щелчка мышью.</span><span class="sxs-lookup"><span data-stu-id="06ba0-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06ba0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06ba0-115">Return value</span></span>

<span data-ttu-id="06ba0-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="06ba0-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ba0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06ba0-117">Remarks</span></span>

<span data-ttu-id="06ba0-118">Окно может обработать это сообщение, отображая контекстное меню с помощью функций [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) или [**траккпопупменуекс**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="06ba0-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="06ba0-119">Чтобы получить горизонтальные и вертикальные позиции, используйте следующий код.</span><span class="sxs-lookup"><span data-stu-id="06ba0-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="06ba0-120">Если окно не отображает контекстное меню, оно должно передать это сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="06ba0-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="06ba0-121">Если окно является дочерним, **дефвиндовпрок** отправляет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="06ba0-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="06ba0-122">В противном случае **дефвиндовпрок** отображает контекстное меню по умолчанию, если указанное расположение находится в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="06ba0-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="06ba0-123">[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) создает сообщение **WM \_ CONTEXTMENU** при обработке сообщения [**WM \_ рбуттонуп**](/windows/desktop/inputdev/wm-rbuttonup) или [**WM \_ нкрбуттонуп**](/windows/desktop/inputdev/wm-ncrbuttonup) или когда пользователь вводит Shift + F10.</span><span class="sxs-lookup"><span data-stu-id="06ba0-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="06ba0-124">Сообщение **WM \_ CONTEXTMENU** также создается, когда пользователь нажимает и отпускает ключ [**VK \_ Apps**](/windows/desktop/inputdev/virtual-key-codes) .</span><span class="sxs-lookup"><span data-stu-id="06ba0-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="06ba0-125">Если контекстное меню создается на основе клавиатуры, например, если пользователь вводит SHIFT + F10, координаты x и y равны-1, и приложение должно отобразить контекстное меню в месте текущего выделения, а не в (Кспос, ИПОС).</span><span class="sxs-lookup"><span data-stu-id="06ba0-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="06ba0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="06ba0-126">Requirements</span></span>



| <span data-ttu-id="06ba0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="06ba0-127">Requirement</span></span> | <span data-ttu-id="06ba0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="06ba0-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ba0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06ba0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06ba0-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="06ba0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06ba0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06ba0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06ba0-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="06ba0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06ba0-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="06ba0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06ba0-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06ba0-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06ba0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06ba0-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="06ba0-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="06ba0-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06ba0-137">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="06ba0-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="06ba0-138">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="06ba0-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="06ba0-139">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="06ba0-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="06ba0-140">**Метод TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="06ba0-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="06ba0-141">**траккпопупменуекс**</span><span class="sxs-lookup"><span data-stu-id="06ba0-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="06ba0-142">**WM \_ нкрбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="06ba0-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="06ba0-143">**WM \_ рбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="06ba0-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="06ba0-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="06ba0-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06ba0-145">Меню</span><span class="sxs-lookup"><span data-stu-id="06ba0-145">Menus</span></span>](menus.md)
</dt> </dl>

 

