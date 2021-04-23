---
description: Сообщение WM \_ куериневпалетте информирует окно о том, что он собирается получить фокус клавиатуры, давая окну возможность реализовать логическую палитру при получении фокуса.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Сообщение WM_QUERYNEWPALETTE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985337"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="e6bb9-103">\_Сообщение КУЕРИНЕВПАЛЕТТЕ WM</span><span class="sxs-lookup"><span data-stu-id="e6bb9-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="e6bb9-104">Сообщение **WM \_ куериневпалетте** информирует окно о том, что он собирается получить фокус клавиатуры, давая окну возможность реализовать логическую палитру при получении фокуса.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="e6bb9-105">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6bb9-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="e6bb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6bb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6bb9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6bb9-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6bb9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6bb9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6bb9-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6bb9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6bb9-111">Return value</span></span>

<span data-ttu-id="e6bb9-112">Если окно реализует логическую палитру, оно должно возвращать **значение true**. в противном случае он должен вернуть **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6bb9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e6bb9-113">Requirements</span></span>



| <span data-ttu-id="e6bb9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e6bb9-114">Requirement</span></span> | <span data-ttu-id="e6bb9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e6bb9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bb9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6bb9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e6bb9-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6bb9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6bb9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6bb9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e6bb9-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6bb9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6bb9-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e6bb9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6bb9-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6bb9-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6bb9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6bb9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6bb9-123">Общие сведения о цветах</span><span class="sxs-lookup"><span data-stu-id="e6bb9-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="e6bb9-124">Цветные сообщения</span><span class="sxs-lookup"><span data-stu-id="e6bb9-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="e6bb9-125">**WM \_ палеттечанжед**</span><span class="sxs-lookup"><span data-stu-id="e6bb9-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="e6bb9-126">**WM \_ палеттеисчангинг**</span><span class="sxs-lookup"><span data-stu-id="e6bb9-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 
