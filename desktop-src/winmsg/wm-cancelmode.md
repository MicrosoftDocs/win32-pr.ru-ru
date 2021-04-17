---
description: Отправляется для отмены определенных режимов, таких как захват мыши.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Сообщение WM_CANCELMODE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702580"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="94d55-103">\_Сообщение КАНЦЕЛМОДЕ WM</span><span class="sxs-lookup"><span data-stu-id="94d55-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="94d55-104">Отправляется для отмены определенных режимов, таких как захват мыши.</span><span class="sxs-lookup"><span data-stu-id="94d55-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="94d55-105">Например, система отправляет это сообщение в активное окно, когда отображается диалоговое окно или поле сообщения.</span><span class="sxs-lookup"><span data-stu-id="94d55-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="94d55-106">Некоторые функции также отправляют это сообщение явно в указанное окно, независимо от того, является ли оно активным.</span><span class="sxs-lookup"><span data-stu-id="94d55-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="94d55-107">Например, функция [**енаблевиндов**](/windows/win32/api/winuser/nf-winuser-enablewindow) отправляет это сообщение при отключении указанного окна.</span><span class="sxs-lookup"><span data-stu-id="94d55-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="94d55-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="94d55-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="94d55-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="94d55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d55-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94d55-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d55-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="94d55-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94d55-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94d55-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94d55-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="94d55-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d55-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94d55-114">Return value</span></span>

<span data-ttu-id="94d55-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="94d55-115">Type: **LRESULT**</span></span>

<span data-ttu-id="94d55-116">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="94d55-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94d55-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94d55-117">Remarks</span></span>

<span data-ttu-id="94d55-118">При отправке сообщения **WM \_ Канцелмоде** функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отменяет внутреннюю обработку стандартного ввода полосы прокрутки, отменяет внутреннюю обработку меню и освобождает захват мыши.</span><span class="sxs-lookup"><span data-stu-id="94d55-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d55-119">Требования</span><span class="sxs-lookup"><span data-stu-id="94d55-119">Requirements</span></span>



| <span data-ttu-id="94d55-120">Требование</span><span class="sxs-lookup"><span data-stu-id="94d55-120">Requirement</span></span> | <span data-ttu-id="94d55-121">Значение</span><span class="sxs-lookup"><span data-stu-id="94d55-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d55-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94d55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94d55-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94d55-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94d55-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94d55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94d55-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94d55-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94d55-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="94d55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d55-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94d55-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d55-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94d55-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="94d55-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="94d55-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="94d55-130">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="94d55-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="94d55-131">**енаблевиндов**</span><span class="sxs-lookup"><span data-stu-id="94d55-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="94d55-132">**релеасекаптуре**</span><span class="sxs-lookup"><span data-stu-id="94d55-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="94d55-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="94d55-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94d55-134">Windows</span><span class="sxs-lookup"><span data-stu-id="94d55-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
