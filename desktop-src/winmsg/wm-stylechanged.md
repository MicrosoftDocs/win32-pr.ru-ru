---
description: Посылается окну после того, как функция SetWindowLong изменила один или несколько стилей окна.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Сообщение WM_STYLECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546471"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="7d4b7-103">\_Сообщение СТИЛЕЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="7d4b7-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="7d4b7-104">Посылается окну после того, как функция [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) изменила один или несколько стилей окна.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="7d4b7-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7d4b7-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="7d4b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d4b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d4b7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d4b7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4b7-108">Указывает, изменились ли стили окна или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="7d4b7-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="7d4b7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7d4b7-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="7d4b7-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7d4b7-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="7d4b7-112"><dt>**ГВЛ \_ ОПЕРАТОРЕ EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b7-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="7d4b7-113">Изменены стили расширенного окна.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="7d4b7-114"><dt>**ГВЛ \_ СТИЛЬ**</dt> <dt>— 16</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b7-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="7d4b7-115">Стили окна изменились.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="7d4b7-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d4b7-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4b7-117">Указатель на структуру [**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct) , содержащую новые стили для окна.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="7d4b7-118">Приложение может проверять стили, но не может их изменять.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d4b7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d4b7-119">Return value</span></span>

<span data-ttu-id="7d4b7-120">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-120">Type: **LRESULT**</span></span>

<span data-ttu-id="7d4b7-121">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="7d4b7-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4b7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7d4b7-122">Requirements</span></span>



| <span data-ttu-id="7d4b7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7d4b7-123">Requirement</span></span> | <span data-ttu-id="7d4b7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7d4b7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4b7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d4b7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7d4b7-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d4b7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7d4b7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d4b7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7d4b7-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d4b7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d4b7-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d4b7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d4b7-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d4b7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d4b7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d4b7-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d4b7-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="7d4b7-134">**стилеструкт**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="7d4b7-135">**WM \_ стилечангинг**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="7d4b7-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7d4b7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7d4b7-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7d4b7-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
