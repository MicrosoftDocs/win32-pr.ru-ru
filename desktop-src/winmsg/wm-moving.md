---
description: Отправляется в окно, которое перемещает пользователь. Обрабатывая это сообщение, приложение может отслеживать расположение прямоугольника перетаскивания и, при необходимости, изменять его расположение.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Сообщение WM_MOVING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673267"
---
# <a name="wm_moving-message"></a><span data-ttu-id="71e9e-104">\_Перемещение сообщения WM</span><span class="sxs-lookup"><span data-stu-id="71e9e-104">WM\_MOVING message</span></span>

<span data-ttu-id="71e9e-105">Отправляется в окно, которое перемещает пользователь.</span><span class="sxs-lookup"><span data-stu-id="71e9e-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="71e9e-106">Обрабатывая это сообщение, приложение может отслеживать расположение прямоугольника перетаскивания и, при необходимости, изменять его расположение.</span><span class="sxs-lookup"><span data-stu-id="71e9e-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="71e9e-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="71e9e-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="71e9e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="71e9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e9e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71e9e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e9e-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="71e9e-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="71e9e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71e9e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e9e-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) с текущей позицией окна в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="71e9e-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="71e9e-113">Чтобы изменить расположение прямоугольника перетаскивания, приложение должно изменить члены этой структуры.</span><span class="sxs-lookup"><span data-stu-id="71e9e-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e9e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71e9e-114">Return value</span></span>

<span data-ttu-id="71e9e-115">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="71e9e-115">Type: **LRESULT**</span></span>

<span data-ttu-id="71e9e-116">Приложение должно возвращать **значение true** , если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="71e9e-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e9e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="71e9e-117">Requirements</span></span>



| <span data-ttu-id="71e9e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="71e9e-118">Requirement</span></span> | <span data-ttu-id="71e9e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="71e9e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e9e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71e9e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71e9e-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71e9e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="71e9e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71e9e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71e9e-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71e9e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71e9e-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="71e9e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e9e-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71e9e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e9e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71e9e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="71e9e-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="71e9e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71e9e-128">**\_Перемещение WM**</span><span class="sxs-lookup"><span data-stu-id="71e9e-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="71e9e-129">**\_изменение размера WM**</span><span class="sxs-lookup"><span data-stu-id="71e9e-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="71e9e-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="71e9e-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71e9e-131">Windows</span><span class="sxs-lookup"><span data-stu-id="71e9e-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="71e9e-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="71e9e-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="71e9e-133">[**ПЕРЕТАСКИВАЕМЫЕ**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71e9e-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
