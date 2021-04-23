---
description: Приложение отправляет \_ сообщение WM сетредрав в окно, чтобы разрешить перерисовку изменений в этом окне или предотвратить перерисовку изменений в этом окне.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Сообщение WM_SETREDRAW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265518"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="bdc9b-103">\_Сообщение СЕТРЕДРАВ WM</span><span class="sxs-lookup"><span data-stu-id="bdc9b-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="bdc9b-104">Приложение отправляет сообщение **WM \_ сетредрав** в окно, чтобы разрешить перерисовку изменений в этом окне или предотвратить перерисовку изменений в этом окне.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="bdc9b-105">Чтобы отправить это сообщение, вызовите функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="bdc9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdc9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc9b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdc9b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc9b-108">Состояние перерисовки.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-108">The redraw state.</span></span> <span data-ttu-id="bdc9b-109">Если этот параметр имеет **значение true**, содержимое можно перерисовать после изменения.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="bdc9b-110">Если этот параметр имеет **значение false**, то после изменения содержимое не может быть перерисовано.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="bdc9b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdc9b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdc9b-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc9b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdc9b-113">Return value</span></span>

<span data-ttu-id="bdc9b-114">Приложение возвращает нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc9b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="bdc9b-115">Remarks</span></span>

<span data-ttu-id="bdc9b-116">Это сообщение может быть полезно, если приложение должно добавить несколько элементов в список.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="bdc9b-117">Приложение может вызвать это сообщение с параметром *wParam* , имеющим значение **false**, добавить элементы, а затем снова вызвать сообщение, указав для параметра *wParam* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="bdc9b-118">Наконец, приложение может вызвать [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, РДВ \_ Erase \| РДВ \_ Frame \| РДВ \_ делает недействительным \| РДВ \_ аллчилдрен), чтобы перерисовать список.</span><span class="sxs-lookup"><span data-stu-id="bdc9b-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="bdc9b-119">[**Редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) с заданными флагами используется вместо [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , так как первый необходим для некоторых элементов управления, которые имеют неклиентскую область, или имеют стили окна, которые приводят к тому, что им предоставляется неклиентская область (например, **WS \_ сиккфраме**, **WS \_ border** или **WS \_ ex \_ клиентедже**).</span><span class="sxs-lookup"><span data-stu-id="bdc9b-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="bdc9b-120">Если у элемента управления нет неклиентской области, **редраввиндов** с этими флагами будет выполнять только столько же, сколько и **инвалидатерект** .</span><span class="sxs-lookup"><span data-stu-id="bdc9b-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="bdc9b-121">Если приложение отправляет сообщение **WM \_ сетредрав** в скрытое окно, окно становится видимым (т. е. операционная система добавляет в окно стиль **, \_ видимый WS** ).</span><span class="sxs-lookup"><span data-stu-id="bdc9b-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc9b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bdc9b-122">Requirements</span></span>



| <span data-ttu-id="bdc9b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bdc9b-123">Requirement</span></span> | <span data-ttu-id="bdc9b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bdc9b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc9b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdc9b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc9b-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bdc9b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bdc9b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdc9b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc9b-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bdc9b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdc9b-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bdc9b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc9b-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdc9b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc9b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdc9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc9b-132">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="bdc9b-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="bdc9b-133">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="bdc9b-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="bdc9b-134">**редраввиндов**</span><span class="sxs-lookup"><span data-stu-id="bdc9b-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
