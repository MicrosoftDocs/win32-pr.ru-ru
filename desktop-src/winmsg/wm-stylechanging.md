---
description: Отправляется в окно, когда функция SetWindowLong собирается изменить один или несколько стилей окна.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Сообщение WM_STYLECHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909852"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="a2561-103">\_Сообщение СТИЛЕЧАНГИНГ WM</span><span class="sxs-lookup"><span data-stu-id="a2561-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="a2561-104">Отправляется в окно, когда функция [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) собирается изменить один или несколько стилей окна.</span><span class="sxs-lookup"><span data-stu-id="a2561-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="a2561-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2561-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="a2561-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2561-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2561-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2561-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2561-108">Указывает, изменяются ли стили окна или расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="a2561-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="a2561-109">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a2561-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a2561-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a2561-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="a2561-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a2561-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="a2561-112"><dt>**ГВЛ \_ ОПЕРАТОРЕ EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="a2561-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="a2561-113">Изменяются расширенные стили окна.</span><span class="sxs-lookup"><span data-stu-id="a2561-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="a2561-114"><dt>**ГВЛ \_ СТИЛЬ**</dt> <dt>— 16</dt></span><span class="sxs-lookup"><span data-stu-id="a2561-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="a2561-115">Стили окна меняются.</span><span class="sxs-lookup"><span data-stu-id="a2561-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="a2561-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2561-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2561-117">Указатель на структуру [**стилеструкт**](/windows/win32/api/winuser/ns-winuser-stylestruct) , которая содержит предложенные новые стили для окна.</span><span class="sxs-lookup"><span data-stu-id="a2561-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="a2561-118">Приложение может проверить стили и при необходимости изменить их.</span><span class="sxs-lookup"><span data-stu-id="a2561-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2561-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2561-119">Return value</span></span>

<span data-ttu-id="a2561-120">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="a2561-120">Type: **LRESULT**</span></span>

<span data-ttu-id="a2561-121">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a2561-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2561-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a2561-122">Requirements</span></span>



| <span data-ttu-id="a2561-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a2561-123">Requirement</span></span> | <span data-ttu-id="a2561-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a2561-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2561-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2561-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a2561-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2561-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2561-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2561-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a2561-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2561-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2561-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2561-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2561-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2561-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2561-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2561-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2561-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a2561-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a2561-133">**стилеструкт**</span><span class="sxs-lookup"><span data-stu-id="a2561-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="a2561-134">**WM \_ стилечанжед**</span><span class="sxs-lookup"><span data-stu-id="a2561-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="a2561-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a2561-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a2561-136">Windows</span><span class="sxs-lookup"><span data-stu-id="a2561-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
