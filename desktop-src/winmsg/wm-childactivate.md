---
description: Посылается в дочернее окно, когда пользователь щелкает заголовок окна или при активации, перемещении или изменении размера окна.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: Сообщение WM_CHILDACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815464"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="615e3-103">\_Сообщение ЧИЛДАКТИВАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="615e3-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="615e3-104">Посылается в дочернее окно, когда пользователь щелкает заголовок окна или при активации, перемещении или изменении размера окна.</span><span class="sxs-lookup"><span data-stu-id="615e3-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="615e3-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="615e3-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="615e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="615e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="615e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="615e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="615e3-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="615e3-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="615e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="615e3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="615e3-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="615e3-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="615e3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="615e3-111">Return value</span></span>

<span data-ttu-id="615e3-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="615e3-112">Type: **LRESULT**</span></span>

<span data-ttu-id="615e3-113">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="615e3-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="615e3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="615e3-114">Requirements</span></span>



| <span data-ttu-id="615e3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="615e3-115">Requirement</span></span> | <span data-ttu-id="615e3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="615e3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="615e3-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="615e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="615e3-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="615e3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="615e3-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="615e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="615e3-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="615e3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="615e3-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="615e3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="615e3-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="615e3-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615e3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="615e3-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="615e3-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="615e3-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="615e3-125">**мовевиндов**</span><span class="sxs-lookup"><span data-stu-id="615e3-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="615e3-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="615e3-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="615e3-127">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="615e3-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="615e3-128">Windows</span><span class="sxs-lookup"><span data-stu-id="615e3-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 
