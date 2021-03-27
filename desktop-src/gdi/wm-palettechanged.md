---
description: Сообщение WM \_ палеттечанжед отправляется во все окна верхнего уровня и перекрывающихся окон после того, как окно с фокусом клавиатуры реализовало логическую палитру, тем самым изменяя системную палитру.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Сообщение WM_PALETTECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813018"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="36dba-103">\_Сообщение ПАЛЕТТЕЧАНЖЕД WM</span><span class="sxs-lookup"><span data-stu-id="36dba-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="36dba-104">Сообщение **WM \_ палеттечанжед** отправляется во все окна верхнего уровня и перекрывающихся окон после того, как окно с фокусом клавиатуры реализовало логическую палитру, тем самым изменяя системную палитру.</span><span class="sxs-lookup"><span data-stu-id="36dba-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="36dba-105">Это сообщение активирует окно, использующее цветовую палитру, но не имеющее фокуса клавиатуры, чтобы реализовать логическую палитру и обновить ее клиентскую область.</span><span class="sxs-lookup"><span data-stu-id="36dba-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="36dba-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36dba-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="36dba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36dba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36dba-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36dba-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dba-109">Маркер окна, вызвавшего изменение системной палитры.</span><span class="sxs-lookup"><span data-stu-id="36dba-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="36dba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36dba-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dba-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="36dba-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36dba-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="36dba-112">Remarks</span></span>

<span data-ttu-id="36dba-113">Это сообщение должно быть отправлено всем окнам верхнего уровня и перекрывающихся окон, включая те, которые изменили системную палитру.</span><span class="sxs-lookup"><span data-stu-id="36dba-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="36dba-114">Если любые дочерние окна используют цветовую палитру, это сообщение также должно быть передано в них.</span><span class="sxs-lookup"><span data-stu-id="36dba-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="36dba-115">Чтобы избежать создания бесконечного цикла, окно, которое получает это сообщение, не должно знать его палитру, если только не определит, что *wParam* не содержит собственного обработчика окна.</span><span class="sxs-lookup"><span data-stu-id="36dba-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="36dba-116">Требования</span><span class="sxs-lookup"><span data-stu-id="36dba-116">Requirements</span></span>



| <span data-ttu-id="36dba-117">Требование</span><span class="sxs-lookup"><span data-stu-id="36dba-117">Requirement</span></span> | <span data-ttu-id="36dba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="36dba-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dba-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36dba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="36dba-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36dba-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="36dba-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36dba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="36dba-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36dba-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36dba-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36dba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dba-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36dba-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36dba-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36dba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36dba-126">Общие сведения о цветах</span><span class="sxs-lookup"><span data-stu-id="36dba-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="36dba-127">Цветные сообщения</span><span class="sxs-lookup"><span data-stu-id="36dba-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="36dba-128">**WM \_ палеттеисчангинг**</span><span class="sxs-lookup"><span data-stu-id="36dba-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="36dba-129">**WM \_ куериневпалетте**</span><span class="sxs-lookup"><span data-stu-id="36dba-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
