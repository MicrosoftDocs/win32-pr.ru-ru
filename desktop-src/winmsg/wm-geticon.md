---
description: Отправляется окну для получения маркера на крупный или маленький значок, связанный с окном. Система отображает крупный значок в диалоговом окне ALT + TAB, а маленький значок в заголовке окна.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Сообщение WM_GETICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702573"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="ac30a-104">Сообщение WM с \_ значком</span><span class="sxs-lookup"><span data-stu-id="ac30a-104">WM\_GETICON message</span></span>

<span data-ttu-id="ac30a-105">Отправляется окну для получения маркера на крупный или маленький значок, связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="ac30a-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="ac30a-106">Система отображает крупный значок в диалоговом окне ALT + TAB, а маленький значок в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="ac30a-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="ac30a-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ac30a-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="ac30a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac30a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac30a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac30a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac30a-110">Тип извлекаемого значка.</span><span class="sxs-lookup"><span data-stu-id="ac30a-110">The type of icon being retrieved.</span></span> <span data-ttu-id="ac30a-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="ac30a-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ac30a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ac30a-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="ac30a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ac30a-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="ac30a-114"><dt>**Значок \_ БОЛЬШОЙ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ac30a-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="ac30a-115">Получение крупного значка для окна.</span><span class="sxs-lookup"><span data-stu-id="ac30a-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="ac30a-116"><dt>**Значок \_ Малый**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ac30a-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="ac30a-117">Получите маленький значок для окна.</span><span class="sxs-lookup"><span data-stu-id="ac30a-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="ac30a-118"><dt>**Значок \_ SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ac30a-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="ac30a-119">Извлекает маленький значок, предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="ac30a-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="ac30a-120">Если приложение не предоставляет его, система использует для этого окна значок, созданный системой.</span><span class="sxs-lookup"><span data-stu-id="ac30a-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ac30a-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac30a-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac30a-122">Значение DPI получаемого значка.</span><span class="sxs-lookup"><span data-stu-id="ac30a-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="ac30a-123">Он может использоваться для предоставления различных значков в зависимости от размера значка.</span><span class="sxs-lookup"><span data-stu-id="ac30a-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac30a-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac30a-124">Return value</span></span>

<span data-ttu-id="ac30a-125">Тип: **Хикон**</span><span class="sxs-lookup"><span data-stu-id="ac30a-125">Type: **HICON**</span></span>

<span data-ttu-id="ac30a-126">Возвращаемое значение является маркером для большого или маленького значка в зависимости от значения *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ac30a-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="ac30a-127">Когда приложение получает это сообщение, оно может вернуть маркер на большой или маленький значок или передать сообщение в функцию [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="ac30a-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac30a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac30a-128">Remarks</span></span>

<span data-ttu-id="ac30a-129">Когда приложение получает это сообщение, оно может вернуть маркер на большой или маленький значок или передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ac30a-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="ac30a-130">[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает маркер для большого или маленького значка, связанного с окном, в зависимости от значения *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ac30a-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="ac30a-131">Окно, не имеющее явно заданного значка (с **WM \_ сетикон**), использует значок для зарегистрированного класса окна, и в данном случае [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвратит 0 для сообщения **WM- \_ Icon** .</span><span class="sxs-lookup"><span data-stu-id="ac30a-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="ac30a-132">При отправке сообщения **WM- \_ Icon** в окно возвращается значение 0. Затем попробуйте вызвать функцию [**жеткласслонгптр**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) для окна.</span><span class="sxs-lookup"><span data-stu-id="ac30a-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="ac30a-133">Если возвращается значение 0, попробуйте использовать функцию [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona) .</span><span class="sxs-lookup"><span data-stu-id="ac30a-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac30a-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ac30a-134">Requirements</span></span>



| <span data-ttu-id="ac30a-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ac30a-135">Requirement</span></span> | <span data-ttu-id="ac30a-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ac30a-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac30a-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac30a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ac30a-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac30a-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ac30a-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac30a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ac30a-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac30a-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac30a-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ac30a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac30a-142"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac30a-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac30a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac30a-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="ac30a-144">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ac30a-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ac30a-145">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="ac30a-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ac30a-146">**WM \_ сетикон**</span><span class="sxs-lookup"><span data-stu-id="ac30a-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="ac30a-147">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ac30a-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ac30a-148">Windows</span><span class="sxs-lookup"><span data-stu-id="ac30a-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 
