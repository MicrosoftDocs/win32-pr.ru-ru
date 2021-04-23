---
description: Отправляется приложением обучения на основе компьютеров (CBT) для разделения сообщений, вводимых пользователем, от других сообщений, отправленных с помощью \_ процедуры жаурналплайбакк.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Сообщение WM_QUEUESYNC (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647365"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="20fa1-103">\_Сообщение КУЕУЕСИНК WM</span><span class="sxs-lookup"><span data-stu-id="20fa1-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="20fa1-104">Отправляется приложением обучения на основе компьютеров (CBT) для разделения сообщений, вводимых пользователем, от других сообщений, отправленных с помощью процедуры [**\_ жаурналплайбакк**](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="20fa1-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="20fa1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="20fa1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fa1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20fa1-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20fa1-107">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="20fa1-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20fa1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20fa1-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20fa1-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="20fa1-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fa1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20fa1-110">Return value</span></span>

<span data-ttu-id="20fa1-111">Тип: **void**</span><span class="sxs-lookup"><span data-stu-id="20fa1-111">Type: **void**</span></span>

<span data-ttu-id="20fa1-112">Приложение CBT должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="20fa1-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="20fa1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20fa1-113">Remarks</span></span>

<span data-ttu-id="20fa1-114">Каждый раз, когда приложение CBT [**использует \_ жаурналплайбакк**](about-hooks.md) процедуру, первым и последним сообщением является **WM \_ куеуесинк**.</span><span class="sxs-lookup"><span data-stu-id="20fa1-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="20fa1-115">Это позволяет приложению CBT перехватывать и анализировать сообщения, инициированные пользователем, без необходимости делать это для отправляемых им событий.</span><span class="sxs-lookup"><span data-stu-id="20fa1-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="20fa1-116">Если в приложении задан **пустой** обработчик окна, сообщение отправляется в очередь сообщений активного окна.</span><span class="sxs-lookup"><span data-stu-id="20fa1-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="20fa1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="20fa1-117">Requirements</span></span>



| <span data-ttu-id="20fa1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="20fa1-118">Requirement</span></span> | <span data-ttu-id="20fa1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="20fa1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fa1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20fa1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="20fa1-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="20fa1-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20fa1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20fa1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="20fa1-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20fa1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20fa1-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20fa1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="20fa1-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fa1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fa1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20fa1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="20fa1-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="20fa1-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="20fa1-128">[*жаурналплайбаккпрок*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20fa1-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20fa1-129">**сетвиндовшукекс**</span><span class="sxs-lookup"><span data-stu-id="20fa1-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="20fa1-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="20fa1-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="20fa1-131">Обработчики</span><span class="sxs-lookup"><span data-stu-id="20fa1-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
