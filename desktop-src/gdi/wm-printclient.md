---
description: Сообщение WM \_ принтклиент отправляется в окно для запроса на прорисовку клиентской области в указанном контексте устройства, чаще всего в контексте устройства печати.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Сообщение WM_PRINTCLIENT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985800"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="2f399-103">\_Сообщение ПРИНТКЛИЕНТ WM</span><span class="sxs-lookup"><span data-stu-id="2f399-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="2f399-104">Сообщение **WM \_ принтклиент** отправляется в окно для запроса на прорисовку клиентской области в указанном контексте устройства, чаще всего в контексте устройства печати.</span><span class="sxs-lookup"><span data-stu-id="2f399-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="2f399-105">В отличие [**от \_ Printing WM**](wm-print.md), **WM \_ принтклиент** не обрабатывается [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="2f399-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="2f399-106">Для правильного использования окно должно обрабатывать сообщение **WM \_ принтклиент** через определяемую приложением [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) функцию.</span><span class="sxs-lookup"><span data-stu-id="2f399-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="2f399-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f399-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f399-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f399-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f399-109">Маркер контекста устройства для рисования в.</span><span class="sxs-lookup"><span data-stu-id="2f399-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="2f399-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f399-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f399-111">Параметры рисования.</span><span class="sxs-lookup"><span data-stu-id="2f399-111">The drawing options.</span></span> <span data-ttu-id="2f399-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2f399-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2f399-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2f399-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="2f399-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2f399-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="2f399-115"><dt>**PRF \_ чекквисибле**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="2f399-116">Отображает окно только в том случае, если оно видимо.</span><span class="sxs-lookup"><span data-stu-id="2f399-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="2f399-117"><dt>**вложенные \_ элементы PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="2f399-118">Рисует все видимые дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="2f399-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="2f399-119"><dt>**PRF, \_ клиент**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="2f399-120">Рисует клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="2f399-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="2f399-121"><dt>**PRF \_ ерасебкгнд**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="2f399-122">Стирает фон перед рисованием окна.</span><span class="sxs-lookup"><span data-stu-id="2f399-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="2f399-123"><dt>**PRF не \_ клиент**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="2f399-124">Рисует неклиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="2f399-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="2f399-125"><dt>**\_владелец PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="2f399-126">Рисует все собственные окна.</span><span class="sxs-lookup"><span data-stu-id="2f399-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f399-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f399-127">Remarks</span></span>

<span data-ttu-id="2f399-128">Окно может обрабатывать это сообщение во многом так же, как [**WM \_ Paint**](./wm-paint.md), за исключением того, что [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) и [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) не нужно вызывать (предоставляется контекст устройства), и окно должно рисовать всю клиентскую область, а не только недействительную область.</span><span class="sxs-lookup"><span data-stu-id="2f399-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="2f399-129">Окна, которые могут использоваться в любом месте системы, например элементы управления, должны обрабатывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="2f399-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="2f399-130">В других окнах может быть целесообразно обработать это сообщение, так как оно относительно легко реализуется.</span><span class="sxs-lookup"><span data-stu-id="2f399-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="2f399-131">Функция [аниматевиндов](/windows/desktop/api/winuser/nf-winuser-animatewindow) требует, чтобы анимированное окно реализовало сообщение **WM \_ принтклиент** .</span><span class="sxs-lookup"><span data-stu-id="2f399-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f399-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2f399-132">Requirements</span></span>



| <span data-ttu-id="2f399-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2f399-133">Requirement</span></span> | <span data-ttu-id="2f399-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2f399-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f399-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f399-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f399-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f399-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f399-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f399-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f399-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f399-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f399-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2f399-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f399-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f399-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f399-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f399-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f399-142">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="2f399-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="2f399-143">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="2f399-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="2f399-144">**аниматевиндов**</span><span class="sxs-lookup"><span data-stu-id="2f399-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="2f399-145">**бегинпаинт**</span><span class="sxs-lookup"><span data-stu-id="2f399-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="2f399-146">**ендпаинт**</span><span class="sxs-lookup"><span data-stu-id="2f399-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="2f399-147">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="2f399-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
