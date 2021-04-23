---
description: Не выполняет никаких операций. Приложение отправляет \_ сообщение WM null, если ему нужно отправить сообщение о том, что окно получателя будет игнорироваться.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Сообщение WM_NULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264522"
---
# <a name="wm_null-message"></a><span data-ttu-id="5ca51-104">\_Сообщение NULL WM</span><span class="sxs-lookup"><span data-stu-id="5ca51-104">WM\_NULL message</span></span>

<span data-ttu-id="5ca51-105">Не выполняет никаких операций.</span><span class="sxs-lookup"><span data-stu-id="5ca51-105">Performs no operation.</span></span> <span data-ttu-id="5ca51-106">Приложение отправляет сообщение **WM \_ null** , если ему нужно отправить сообщение о том, что окно получателя будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="5ca51-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="5ca51-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ca51-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="5ca51-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ca51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca51-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ca51-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ca51-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="5ca51-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ca51-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ca51-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ca51-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="5ca51-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca51-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca51-113">Return value</span></span>

<span data-ttu-id="5ca51-114">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="5ca51-114">Type: **LRESULT**</span></span>

<span data-ttu-id="5ca51-115">Приложение возвращает нуль, если обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="5ca51-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca51-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ca51-116">Remarks</span></span>

<span data-ttu-id="5ca51-117">Например, если приложение установило какой-либо **обработчик \_ сообщений** и желает предотвратить обработку сообщения, функция обратного вызова [**жетмсгпрок**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) может изменить номер сообщения на **WM \_ null** , чтобы получатель игнорировал его.</span><span class="sxs-lookup"><span data-stu-id="5ca51-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="5ca51-118">В качестве другого примера приложение может проверить, отвечает ли окно на сообщения, отправив сообщение **WM \_ null** с помощью функции [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="5ca51-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca51-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca51-119">Requirements</span></span>



| <span data-ttu-id="5ca51-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca51-120">Requirement</span></span> | <span data-ttu-id="5ca51-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca51-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca51-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ca51-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca51-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ca51-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ca51-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ca51-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca51-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ca51-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ca51-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5ca51-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca51-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca51-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca51-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ca51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca51-129">Обзор Windows</span><span class="sxs-lookup"><span data-stu-id="5ca51-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
