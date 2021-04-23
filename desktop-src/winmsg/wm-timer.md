---
description: Отправляется в очередь сообщений установки потока по истечении времени ожидания. Сообщение отправляется функцией PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Сообщение WM_TIMER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265991"
---
# <a name="wm_timer-message"></a><span data-ttu-id="20bac-104">\_Сообщение таймера WM</span><span class="sxs-lookup"><span data-stu-id="20bac-104">WM\_TIMER message</span></span>

<span data-ttu-id="20bac-105">Отправляется в очередь сообщений установки потока по истечении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="20bac-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="20bac-106">Сообщение отправляется функцией [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . [](/windows/win32/api/winuser/nf-winuser-getmessage)</span><span class="sxs-lookup"><span data-stu-id="20bac-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="20bac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20bac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bac-108">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20bac-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bac-109">Идентификатор таймера.</span><span class="sxs-lookup"><span data-stu-id="20bac-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="20bac-110">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20bac-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bac-111">Указатель на определяемую приложением функцию обратного вызова, которая была передана функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) при установке таймера.</span><span class="sxs-lookup"><span data-stu-id="20bac-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bac-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20bac-112">Return value</span></span>

<span data-ttu-id="20bac-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="20bac-113">Type: **LRESULT**</span></span>

<span data-ttu-id="20bac-114">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="20bac-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="20bac-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20bac-115">Remarks</span></span>

<span data-ttu-id="20bac-116">Вы можете обработать сообщение, указав в процедуре Windows регистр **\_ таймера WM** .</span><span class="sxs-lookup"><span data-stu-id="20bac-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="20bac-117">В противном случае [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) будет вызывать функцию обратного вызова [*тимерпрок*](/windows/win32/api/winuser/nc-winuser-timerproc) , указанную в вызове функции [**сеттимер**](/windows/win32/api/winuser/nf-winuser-settimer) , используемой для установки таймера.</span><span class="sxs-lookup"><span data-stu-id="20bac-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="20bac-118">Сообщение **\_ таймера WM** является сообщением с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="20bac-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="20bac-119">Функции [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) и [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) помещаются в это сообщение только в том случае, если в очереди сообщений потока отсутствуют другие сообщения с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="20bac-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="20bac-120">Requirements</span></span>



| <span data-ttu-id="20bac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="20bac-121">Requirement</span></span> | <span data-ttu-id="20bac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="20bac-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bac-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20bac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="20bac-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20bac-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="20bac-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20bac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="20bac-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20bac-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20bac-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20bac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="20bac-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20bac-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bac-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20bac-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="20bac-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="20bac-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="20bac-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="20bac-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="20bac-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="20bac-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="20bac-133">**сеттимер**</span><span class="sxs-lookup"><span data-stu-id="20bac-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="20bac-134">**тимерпрок**</span><span class="sxs-lookup"><span data-stu-id="20bac-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="20bac-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="20bac-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="20bac-136">Таймеры</span><span class="sxs-lookup"><span data-stu-id="20bac-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 
