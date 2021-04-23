---
description: Отправляется в окно с уменьшенным (значком).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Сообщение WM_QUERYDRAGICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345582"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="2a5e1-103">\_Сообщение КУЕРИДРАГИКОН WM</span><span class="sxs-lookup"><span data-stu-id="2a5e1-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="2a5e1-104">Отправляется в окно с уменьшенным (значком).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="2a5e1-105">Окно будет перенесено пользователем, но не имеет значка, определенного для его класса.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="2a5e1-106">Приложение может вернуть маркер к значку или курсору.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="2a5e1-107">Система отображает этот курсор или значок, пока пользователь перетаскивает значок.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="2a5e1-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a5e1-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="2a5e1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a5e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a5e1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a5e1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a5e1-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2a5e1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a5e1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a5e1-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a5e1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a5e1-114">Return value</span></span>

<span data-ttu-id="2a5e1-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="2a5e1-115">Type: **LRESULT**</span></span>

<span data-ttu-id="2a5e1-116">Приложение должно возвращать маркер курсора или значка, который система будет отображать, когда пользователь перетаскивает значок.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="2a5e1-117">Курсор или значок должен быть совместим с разрешением видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="2a5e1-118">Если приложение возвращает **значение NULL**, система отображает курсор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a5e1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a5e1-119">Remarks</span></span>

<span data-ttu-id="2a5e1-120">Когда пользователь перетаскивает значок окна без значка класса, система заменяет значок на курсор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="2a5e1-121">Если приложению требуется, чтобы во время перетаскивания отображался другой курсор, он должен вернуть указатель или значок, совместимый с разрешением видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="2a5e1-122">Если приложение возвращает маркер цветного курсора или значка, система преобразует курсор или значок в черный и белый.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="2a5e1-123">Приложение может вызвать функцию [**лоадкурсор**](/windows/win32/api/winuser/nf-winuser-loadcursora) или [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona) для загрузки курсора или значка из ресурсов в исполняемом файле (exe) и получения этого маркера.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="2a5e1-124">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к **логическому** типу и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="2a5e1-125">Значение **\_ мсгресулт DWL** , заданное функцией [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5e1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2a5e1-126">Requirements</span></span>



| <span data-ttu-id="2a5e1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2a5e1-127">Requirement</span></span> | <span data-ttu-id="2a5e1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2a5e1-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5e1-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a5e1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5e1-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a5e1-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a5e1-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a5e1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5e1-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a5e1-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a5e1-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2a5e1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a5e1-134"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e1-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a5e1-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a5e1-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a5e1-136">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2a5e1-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a5e1-137">**лоадкурсор**</span><span class="sxs-lookup"><span data-stu-id="2a5e1-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="2a5e1-138">**лоадикон**</span><span class="sxs-lookup"><span data-stu-id="2a5e1-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="2a5e1-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2a5e1-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a5e1-140">Windows</span><span class="sxs-lookup"><span data-stu-id="2a5e1-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
