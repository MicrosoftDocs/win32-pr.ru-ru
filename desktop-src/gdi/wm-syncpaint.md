---
description: Сообщение WM \_ синкпаинт используется для синхронизации рисования и предотвращения связывания независимых потоков графического пользовательского интерфейса.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Сообщение WM_SYNCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997642"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="b6ea4-103">\_Сообщение СИНКПАИНТ WM</span><span class="sxs-lookup"><span data-stu-id="b6ea4-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="b6ea4-104">Сообщение **WM \_ синкпаинт** используется для синхронизации рисования и предотвращения связывания независимых потоков графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="b6ea4-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b6ea4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="b6ea4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6ea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ea4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6ea4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ea4-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6ea4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6ea4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6ea4-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6ea4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6ea4-111">Return value</span></span>

<span data-ttu-id="b6ea4-112">Приложение возвращает нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ea4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6ea4-113">Remarks</span></span>

<span data-ttu-id="b6ea4-114">При скрытии, отображении, перемещении или изменении размера окна система может определить, что необходимо отправить сообщение **\_ синкпаинт WM** в окна верхнего уровня других потоков.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="b6ea4-115">Приложения должны передавать **WM \_ Синкпаинт** в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  для обработки.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="b6ea4-116">Функция **дефвиндовпрок** отправит сообщение [**WM \_ нкпаинт**](wm-ncpaint.md) в оконную процедуру, если фрейм окна необходимо зарисовывать и отправить сообщение [**WM \_ ерасебкгнд**](../winmsg/wm-erasebkgnd.md) , если фон окна необходимо стереть.</span><span class="sxs-lookup"><span data-stu-id="b6ea4-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ea4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b6ea4-117">Requirements</span></span>



| <span data-ttu-id="b6ea4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b6ea4-118">Requirement</span></span> | <span data-ttu-id="b6ea4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b6ea4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ea4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6ea4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ea4-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6ea4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b6ea4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6ea4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ea4-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6ea4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6ea4-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6ea4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6ea4-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6ea4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ea4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6ea4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ea4-127">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="b6ea4-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="b6ea4-128">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="b6ea4-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="b6ea4-129">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="b6ea4-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b6ea4-130">**жетдцекс**</span><span class="sxs-lookup"><span data-stu-id="b6ea4-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="b6ea4-131">**жетвиндовдк**</span><span class="sxs-lookup"><span data-stu-id="b6ea4-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="b6ea4-132">**WM \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="b6ea4-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
