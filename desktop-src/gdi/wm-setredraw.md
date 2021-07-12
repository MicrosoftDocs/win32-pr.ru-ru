---
description: '**WM_SETREDRAW** сообщение отправляется в окно, чтобы разрешить перерисовку изменений в этом окне или предотвратить перерисовку изменений в этом окне.'
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Сообщение WM_SETREDRAW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593460"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="c81b7-103">Сообщение WM_SETREDRAW</span><span class="sxs-lookup"><span data-stu-id="c81b7-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="c81b7-104">Вы отправляете сообщение **WM \_ сетредрав** в окно, чтобы разрешить перерисовку изменений в этом окне или предотвратить перерисовку изменений в этом окне.</span><span class="sxs-lookup"><span data-stu-id="c81b7-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="c81b7-105">Чтобы отправить это сообщение, вызовите функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c81b7-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="c81b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c81b7-106">Parameters</span></span>

`wParam`

<span data-ttu-id="c81b7-107">Состояние перерисовки.</span><span class="sxs-lookup"><span data-stu-id="c81b7-107">The redraw state.</span></span> <span data-ttu-id="c81b7-108">Если этот параметр имеет **значение true**, то после изменения содержимое можно перерисовать.</span><span class="sxs-lookup"><span data-stu-id="c81b7-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="c81b7-109">Если этот параметр имеет **значение false**, то после изменения содержимое не может быть перерисовано.</span><span class="sxs-lookup"><span data-stu-id="c81b7-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="c81b7-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c81b7-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c81b7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c81b7-111">Return value</span></span>

<span data-ttu-id="c81b7-112">Приложение должно вернуть значение 0, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="c81b7-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c81b7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c81b7-113">Remarks</span></span>

<span data-ttu-id="c81b7-114">Это сообщение может быть полезно, если приложение должно добавить несколько элементов в список.</span><span class="sxs-lookup"><span data-stu-id="c81b7-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="c81b7-115">Приложение может вызвать это сообщение с параметром *wParam* , имеющим значение **false**, добавить элементы, а затем снова вызвать сообщение, указав для параметра *wParam* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c81b7-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="c81b7-116">Наконец, приложение может вызвать [**редраввиндов**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, РДВ \_ Erase \| РДВ \_ Frame \| РДВ \_ делает недействительным \| РДВ \_ аллчилдрен), чтобы перерисовать список.</span><span class="sxs-lookup"><span data-stu-id="c81b7-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="c81b7-117">Следует использовать [**редраввиндов**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) с заданными флагами вместо [**инвалидатерект**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), поскольку первый из них необходим для некоторых элементов управления, у которых есть неклиентская область, или иметь стили окна, которые приводят к тому, что они получают неклиентскую область (например, **WS_THICKFRAME**, **WS_BORDER** или **WS_EX_CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="c81b7-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="c81b7-118">Если у элемента управления нет области, неклиентской, то **редраввиндов** с этими флагами будет выполнять только столько же, сколько и **инвалидатерект** .</span><span class="sxs-lookup"><span data-stu-id="c81b7-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="c81b7-119">Передача **WM_SETREDRAW** сообщения в функцию **дефвиндовпрок** удаляет стиль **WS_VISIBLE** из окна, если параметр *wParam* имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c81b7-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="c81b7-120">Хотя содержимое окна остается видимым на экране, функция [**исвиндоввисибле**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) возвращает **значение false** при вызове в окне в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="c81b7-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="c81b7-121">Передача **WM_SETREDRAW** сообщения в функцию **дефвиндовпрок** добавляет к окну стиль **WS_VISIBLE** , если он не задан, если для параметра *wParam* задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c81b7-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="c81b7-122">Если приложение отправляет **WM_SETREDRAW** сообщение с параметром *wParam* , установленным в **значение true** , в скрытом окне, окно станет видимым.</span><span class="sxs-lookup"><span data-stu-id="c81b7-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="c81b7-123">**Windows 10 и более поздних версий; Windows Server 2016 и более поздних версий**.</span><span class="sxs-lookup"><span data-stu-id="c81b7-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="c81b7-124">Система устанавливает свойство с именем *сиссетредрав* в окне, в ходе которого оконная процедура передает **WM_SETREDRAW** сообщения **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="c81b7-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="c81b7-125">Чтобы получить значение свойства, если оно доступно, можно использовать функцию " [**предл**](/windows/win32/api/Winuser/nf-winuser-getpropa) ".</span><span class="sxs-lookup"><span data-stu-id="c81b7-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="c81b7-126">Функция **prop** возвращает ненулевое значение, если перерисовка отключена.</span><span class="sxs-lookup"><span data-stu-id="c81b7-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="c81b7-127">Свойство **prop** возвращает нуль, если перерисовка включена, или если не существует свойства окна.</span><span class="sxs-lookup"><span data-stu-id="c81b7-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="c81b7-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c81b7-128">Requirements</span></span>

| <span data-ttu-id="c81b7-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c81b7-129">Requirement</span></span> | <span data-ttu-id="c81b7-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c81b7-130">Value</span></span> |
|-|-|
| <span data-ttu-id="c81b7-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c81b7-131">Minimum supported client</span></span> | <span data-ttu-id="c81b7-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c81b7-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="c81b7-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c81b7-133">Minimum supported server</span></span> | <span data-ttu-id="c81b7-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c81b7-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="c81b7-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c81b7-135">Header</span></span> | <dl><span data-ttu-id="c81b7-136"><dt>Winuser. h (включает Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c81b7-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="c81b7-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c81b7-137">See also</span></span>

* [<span data-ttu-id="c81b7-138">Общие сведения о рисовании и рисовании</span><span class="sxs-lookup"><span data-stu-id="c81b7-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="c81b7-139">Рисование и рисование сообщений</span><span class="sxs-lookup"><span data-stu-id="c81b7-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="c81b7-140">редраввиндов</span><span class="sxs-lookup"><span data-stu-id="c81b7-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
