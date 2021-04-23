---
description: Сообщение WM \_ Print отправляется в окно, чтобы запрашивать, что оно рисуется в указанном контексте устройства, чаще всего в контексте устройства печати.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Сообщение WM_PRINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080645"
---
# <a name="wm_print-message"></a><span data-ttu-id="a8375-103">\_Сообщение для печати WM</span><span class="sxs-lookup"><span data-stu-id="a8375-103">WM\_PRINT message</span></span>

<span data-ttu-id="a8375-104">Сообщение **WM \_ Print** отправляется в окно, чтобы запрашивать, что оно рисуется в указанном контексте устройства, чаще всего в контексте устройства печати.</span><span class="sxs-lookup"><span data-stu-id="a8375-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="a8375-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a8375-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="a8375-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8375-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8375-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8375-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8375-108">Маркер контекста устройства для рисования в.</span><span class="sxs-lookup"><span data-stu-id="a8375-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="a8375-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8375-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8375-110">Параметры рисования.</span><span class="sxs-lookup"><span data-stu-id="a8375-110">The drawing options.</span></span> <span data-ttu-id="a8375-111">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a8375-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a8375-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a8375-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="a8375-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a8375-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="a8375-114"><dt>**PRF \_ чекквисибле**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="a8375-115">Отображает окно только в том случае, если оно видимо.</span><span class="sxs-lookup"><span data-stu-id="a8375-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="a8375-116"><dt>**вложенные \_ элементы PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="a8375-117">Рисует все видимые дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="a8375-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="a8375-118"><dt>**PRF, \_ клиент**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="a8375-119">Рисует клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="a8375-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="a8375-120"><dt>**PRF \_ ерасебкгнд**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="a8375-121">Стирает фон перед рисованием окна.</span><span class="sxs-lookup"><span data-stu-id="a8375-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="a8375-122"><dt>**PRF не \_ клиент**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="a8375-123">Рисует неклиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="a8375-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="a8375-124"><dt>**\_владелец PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="a8375-125">Рисует все собственные окна.</span><span class="sxs-lookup"><span data-stu-id="a8375-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8375-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8375-126">Remarks</span></span>

<span data-ttu-id="a8375-127">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) обрабатывает это сообщение в зависимости от того, какой параметр рисования указан: Если \_ указано PRF чекквисибле, а окно не отображается, ничего не делать, если \_ указан PRF-неклиент, нарисуйте неклиентскую область в указанном контексте устройства, если \_ указан PRF-ерасебкгнд, отправите окну сообщение [**\_ ерасебкгнд WM**](../winmsg/wm-erasebkgnd.md) , если \_ указан PRF-клиент, отправьте окно в [**сообщение \_ принтклиент WM**](wm-printclient.md) , если \_ заданы потомки PRF, отправьте каждое видимое дочернее окно в сообщение WM Print Message, если **\_** \_ задано значение "владеет" **. \_**</span><span class="sxs-lookup"><span data-stu-id="a8375-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8375-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a8375-128">Requirements</span></span>



| <span data-ttu-id="a8375-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a8375-129">Requirement</span></span> | <span data-ttu-id="a8375-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a8375-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8375-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8375-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8375-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8375-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8375-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8375-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8375-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a8375-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8375-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a8375-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8375-136"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8375-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8375-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8375-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8375-138">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="a8375-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="a8375-139">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="a8375-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="a8375-140">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="a8375-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a8375-141">**WM \_ ерасебкгнд**</span><span class="sxs-lookup"><span data-stu-id="a8375-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="a8375-142">**WM \_ принтклиент**</span><span class="sxs-lookup"><span data-stu-id="a8375-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
