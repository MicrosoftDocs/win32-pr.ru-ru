---
title: Сообщение WM_RENDERALLFORMATS (Winuser. h)
description: Отправляется владельцу буфера обмена до его уничтожения, если владелец буфера обмена откладывает отложенную отрисовку одного или нескольких форматов буфера обмена.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- Обмен данными с сообщениями WM_RENDERALLFORMATS
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534940"
---
# <a name="wm_renderallformats-message"></a><span data-ttu-id="feaae-104">\_Сообщение РЕНДЕРАЛЛФОРМАТС WM</span><span class="sxs-lookup"><span data-stu-id="feaae-104">WM\_RENDERALLFORMATS message</span></span>

<span data-ttu-id="feaae-105">Отправляется владельцу буфера обмена до его уничтожения, если владелец буфера обмена откладывает отложенную отрисовку одного или нескольких форматов буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="feaae-105">Sent to the clipboard owner before it is destroyed, if the clipboard owner has delayed rendering one or more clipboard formats.</span></span> <span data-ttu-id="feaae-106">Чтобы содержимое буфера обмена оставалось доступным для других приложений, владелец буфера обмена должен визуализировать данные во всех форматах, которые он способен создать, и поместить данные в буфер обмена, вызвав функцию [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="feaae-106">For the content of the clipboard to remain available to other applications, the clipboard owner must render data in all the formats it is capable of generating, and place the data on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>

<span data-ttu-id="feaae-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="feaae-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a><span data-ttu-id="feaae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="feaae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feaae-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="feaae-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feaae-110">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="feaae-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="feaae-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="feaae-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feaae-112">Этот параметр не используется и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="feaae-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feaae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feaae-113">Return value</span></span>

<span data-ttu-id="feaae-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="feaae-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="feaae-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feaae-115">Remarks</span></span>

<span data-ttu-id="feaae-116">При ответе на **сообщение WM \_ рендераллформатс** приложение должно вызвать функцию [**опенклипбоард**](/windows/win32/api/winuser/nf-winuser-openclipboard) , а затем проверить, что он по-прежнему является владельцем буфера обмена, вызвав функцию [**жетклипбоардовнер**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="feaae-116">When responding to a **WM\_RENDERALLFORMATS** message, the application must call the [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) function and then check that it is still the clipboard owner by calling the [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span>

<span data-ttu-id="feaae-117">Приложение должно проверить, что он по-прежнему является владельцем буфера обмена после открытия буфера обмена, так как после того, как он получит сообщение **WM \_ рендераллформатс** , но до того, как он откроет буфер обмена, другое приложение могло открыться и стать владельцем буфера обмена, и данные этого приложения не должны перезаписываться.</span><span class="sxs-lookup"><span data-stu-id="feaae-117">The application needs to check that it is still the clipboard owner after opening the clipboard because after it receives the **WM\_RENDERALLFORMATS** message, but before it opens the clipboard, another application may have opened and taken ownership of the clipboard, and that application's data should not be overwritten.</span></span>

<span data-ttu-id="feaae-118">В большинстве случаев приложение не должно вызывать функцию [**емптиклипбоард**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) перед вызовом [**сетклипбоарддата**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), так как это приведет к удалению форматов буфера обмена, которые приложение уже отрисовывает.</span><span class="sxs-lookup"><span data-stu-id="feaae-118">In most cases, the application should not call the [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) function before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), since doing so will erase the clipboard formats that the application has already rendered.</span></span>

<span data-ttu-id="feaae-119">При возвращении приложения система удаляет все неотображенные форматы из списка доступных форматов буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="feaae-119">When the application returns, the system removes any unrendered formats from the list of available clipboard formats.</span></span> <span data-ttu-id="feaae-120">Дополнительные сведения о отложенной отрисовке см. в разделе [отложенная визуализация](clipboard-operations.md#delayed-rendering).</span><span class="sxs-lookup"><span data-stu-id="feaae-120">For information about delayed rendering, see [Delayed Rendering](clipboard-operations.md#delayed-rendering).</span></span>

## <a name="requirements"></a><span data-ttu-id="feaae-121">Требования</span><span class="sxs-lookup"><span data-stu-id="feaae-121">Requirements</span></span>



| <span data-ttu-id="feaae-122">Требование</span><span class="sxs-lookup"><span data-stu-id="feaae-122">Requirement</span></span> | <span data-ttu-id="feaae-123">Значение</span><span class="sxs-lookup"><span data-stu-id="feaae-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feaae-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="feaae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="feaae-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="feaae-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="feaae-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="feaae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="feaae-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="feaae-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="feaae-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="feaae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="feaae-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="feaae-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feaae-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feaae-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="feaae-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="feaae-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="feaae-132">**емптиклипбоард**</span><span class="sxs-lookup"><span data-stu-id="feaae-132">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[<span data-ttu-id="feaae-133">**опенклипбоард**</span><span class="sxs-lookup"><span data-stu-id="feaae-133">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[<span data-ttu-id="feaae-134">**сетклипбоарддата**</span><span class="sxs-lookup"><span data-stu-id="feaae-134">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="feaae-135">**WM \_ RENDERFORMAT**</span><span class="sxs-lookup"><span data-stu-id="feaae-135">**WM\_RENDERFORMAT**</span></span>](wm-renderformat.md)
</dt> <dt>

<span data-ttu-id="feaae-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="feaae-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="feaae-137">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="feaae-137">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

