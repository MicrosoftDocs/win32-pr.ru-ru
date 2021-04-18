---
Description: Посылается окну после изменения его размера.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Сообщение WM_SIZE (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649109"
---
# <a name="wm_size-message"></a><span data-ttu-id="77163-103">\_Сообщение о размере WM</span><span class="sxs-lookup"><span data-stu-id="77163-103">WM\_SIZE message</span></span>

<span data-ttu-id="77163-104">Посылается окну после изменения его размера.</span><span class="sxs-lookup"><span data-stu-id="77163-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="77163-105">Окно получает это сообщение через функцию [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="77163-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="77163-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77163-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77163-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77163-108">Тип запрошенного изменения размера.</span><span class="sxs-lookup"><span data-stu-id="77163-108">The type of resizing requested.</span></span> <span data-ttu-id="77163-109">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="77163-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="77163-110">Значение</span><span class="sxs-lookup"><span data-stu-id="77163-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="77163-111">Значение</span><span class="sxs-lookup"><span data-stu-id="77163-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="77163-112"><dt>**Размер \_ МАКСХИДЕ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="77163-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="77163-113">Сообщение отправляется во все всплывающие окна, когда какое-либо другое окно развернуто.</span><span class="sxs-lookup"><span data-stu-id="77163-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="77163-114"><dt>**Размер \_ РАЗВЕРНУТО**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="77163-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="77163-115">Окно развернуто.</span><span class="sxs-lookup"><span data-stu-id="77163-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="77163-116"><dt>**Размер \_ МАКСШОВ**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="77163-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="77163-117">Сообщение отправляется во все всплывающие окна при восстановлении какого-либо другого окна до своего прежнего размера.</span><span class="sxs-lookup"><span data-stu-id="77163-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="77163-118"><dt>**Размер \_ СВЕДЕНная**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="77163-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="77163-119">Окно было сведено к минимальному.</span><span class="sxs-lookup"><span data-stu-id="77163-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="77163-120"><dt>**Размер \_ ВОССТАНОВЛЕНо**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77163-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="77163-121">Размер окна был изменен, но не применяется ни **\_ уменьшенный размер** , ни **\_ развернутое значение размера** .</span><span class="sxs-lookup"><span data-stu-id="77163-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77163-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77163-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77163-123">Слово *lParam* в низком порядке задает новую ширину клиентской области.</span><span class="sxs-lookup"><span data-stu-id="77163-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="77163-124">Слово *lParam* в высоком порядке задает новую высоту клиентской области.</span><span class="sxs-lookup"><span data-stu-id="77163-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77163-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77163-125">Return value</span></span>

<span data-ttu-id="77163-126">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="77163-126">Type: **LRESULT**</span></span>

<span data-ttu-id="77163-127">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="77163-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="77163-128">Пример</span><span class="sxs-lookup"><span data-stu-id="77163-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="77163-129">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="77163-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="77163-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77163-130">Remarks</span></span>

<span data-ttu-id="77163-131">Если функция [**сетскроллпос**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) или [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) вызывается для дочернего окна в результате сообщения **\_ размера WM** , параметр *бредрав* или *брепаинт* должен быть ненулевым, чтобы перерисовать окно.</span><span class="sxs-lookup"><span data-stu-id="77163-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="77163-132">Хотя ширина и высота окна представляют собой 32-битные значения, параметр *lParam* содержит только 16 младших разрядов каждого из них.</span><span class="sxs-lookup"><span data-stu-id="77163-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="77163-133">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщения **WM \_ size** и **WM \_ Move** при обработке сообщения [**WM \_ виндовпосчанжед**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="77163-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="77163-134">Сообщения **WM \_ size** и **WM \_ Move** не отправляются, если приложение обрабатывает сообщение **WM \_ виндовпосчанжед** без вызова **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="77163-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="77163-135">Требования</span><span class="sxs-lookup"><span data-stu-id="77163-135">Requirements</span></span>



| <span data-ttu-id="77163-136">Требование</span><span class="sxs-lookup"><span data-stu-id="77163-136">Requirement</span></span> | <span data-ttu-id="77163-137">Значение</span><span class="sxs-lookup"><span data-stu-id="77163-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77163-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77163-138">Minimum supported client</span></span><br/> | <span data-ttu-id="77163-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77163-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="77163-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77163-140">Minimum supported server</span></span><br/> | <span data-ttu-id="77163-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="77163-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77163-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="77163-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="77163-143"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77163-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77163-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77163-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="77163-145">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="77163-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="77163-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77163-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="77163-147">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="77163-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="77163-148">**мовевиндов**</span><span class="sxs-lookup"><span data-stu-id="77163-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="77163-149">**WM \_ виндовпосчанжед**</span><span class="sxs-lookup"><span data-stu-id="77163-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="77163-150">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="77163-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="77163-151">Windows</span><span class="sxs-lookup"><span data-stu-id="77163-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="77163-152">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="77163-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="77163-153">[**сетскроллпос**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="77163-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
