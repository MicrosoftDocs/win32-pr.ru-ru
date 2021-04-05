---
description: Отправляется в окно, когда размер или расположение окна собирается измениться. Приложение может использовать это сообщение для переопределения стандартного размера и расположения окна по умолчанию, а также минимального или максимального размера отслеживания по умолчанию.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Сообщение WM_GETMINMAXINFO (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911376"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="23b71-104">\_Сообщение ЖЕТМИНМАКСИНФО WM</span><span class="sxs-lookup"><span data-stu-id="23b71-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="23b71-105">Отправляется в окно, когда размер или расположение окна собирается измениться.</span><span class="sxs-lookup"><span data-stu-id="23b71-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="23b71-106">Приложение может использовать это сообщение для переопределения стандартного размера и расположения окна по умолчанию, а также минимального или максимального размера отслеживания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23b71-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="23b71-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="23b71-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="23b71-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23b71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23b71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23b71-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="23b71-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23b71-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23b71-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23b71-112">Указатель на структуру [**минмаксинфо**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) , которая содержит развернутую по умолчанию расположение и размеры, а также минимальный и максимальный размер отслеживания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23b71-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="23b71-113">Приложение может переопределить значения по умолчанию, задав члены этой структуры.</span><span class="sxs-lookup"><span data-stu-id="23b71-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b71-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23b71-114">Return value</span></span>

<span data-ttu-id="23b71-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="23b71-115">Type: **LRESULT**</span></span>

<span data-ttu-id="23b71-116">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="23b71-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b71-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23b71-117">Remarks</span></span>

<span data-ttu-id="23b71-118">Максимальный размер отслеживания — это максимальный размер окна, который может быть создан с помощью границ для изменения размера окна.</span><span class="sxs-lookup"><span data-stu-id="23b71-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="23b71-119">Минимальный размер отслеживания — это наименьший размер окна, который может быть создан с помощью границ для изменения размера окна.</span><span class="sxs-lookup"><span data-stu-id="23b71-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b71-120">Требования</span><span class="sxs-lookup"><span data-stu-id="23b71-120">Requirements</span></span>



| <span data-ttu-id="23b71-121">Требование</span><span class="sxs-lookup"><span data-stu-id="23b71-121">Requirement</span></span> | <span data-ttu-id="23b71-122">Значение</span><span class="sxs-lookup"><span data-stu-id="23b71-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b71-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23b71-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23b71-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23b71-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="23b71-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23b71-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23b71-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23b71-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23b71-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="23b71-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b71-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23b71-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b71-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23b71-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="23b71-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="23b71-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23b71-131">**мовевиндов**</span><span class="sxs-lookup"><span data-stu-id="23b71-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="23b71-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="23b71-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="23b71-133">**минмаксинфо**</span><span class="sxs-lookup"><span data-stu-id="23b71-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="23b71-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="23b71-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23b71-135">Windows</span><span class="sxs-lookup"><span data-stu-id="23b71-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
