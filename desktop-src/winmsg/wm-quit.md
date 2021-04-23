---
description: Обозначает запрос на завершение приложения и создается, когда приложение вызывает функцию Посткуитмессаже. Это сообщение приводит к тому, что функция передачи сообщений возвращает ноль.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Сообщение WM_QUIT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080817"
---
# <a name="wm_quit-message"></a><span data-ttu-id="ff530-104">\_Сообщение о выходе WM</span><span class="sxs-lookup"><span data-stu-id="ff530-104">WM\_QUIT message</span></span>

<span data-ttu-id="ff530-105">Обозначает запрос на завершение приложения и создается, когда приложение вызывает функцию [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="ff530-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="ff530-106">Это сообщение приводит к тому, что функция передачи [**сообщений**](/windows/win32/api/winuser/nf-winuser-getmessage) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ff530-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="ff530-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff530-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff530-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff530-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff530-109">Код выхода, заданный в функции [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="ff530-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="ff530-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff530-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff530-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ff530-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff530-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff530-112">Return value</span></span>

<span data-ttu-id="ff530-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="ff530-113">Type: **LRESULT**</span></span>

<span data-ttu-id="ff530-114">Это сообщение не имеет возвращаемого значения, так как оно приводит к завершению цикла обработки сообщений перед отправкой сообщения в процедуру окна приложения.</span><span class="sxs-lookup"><span data-stu-id="ff530-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff530-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff530-115">Remarks</span></span>

<span data-ttu-id="ff530-116">Сообщение **WM \_ Quit** не связано с окном и, следовательно, никогда не будет получено с помощью оконной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="ff530-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="ff530-117">Он извлекается только с помощью функций [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) или функции WITH [**Message**](/windows/win32/api/winuser/nf-winuser-getmessage) .</span><span class="sxs-lookup"><span data-stu-id="ff530-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="ff530-118">Не перемещайте сообщение **WM \_ Quit** с помощью функции [**onmessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; используйте [**посткуитмессаже**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="ff530-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff530-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ff530-119">Requirements</span></span>



| <span data-ttu-id="ff530-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ff530-120">Requirement</span></span> | <span data-ttu-id="ff530-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ff530-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff530-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff530-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ff530-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff530-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff530-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff530-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ff530-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff530-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff530-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff530-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff530-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff530-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff530-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff530-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff530-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ff530-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff530-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="ff530-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="ff530-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="ff530-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="ff530-132">**посткуитмессаже**</span><span class="sxs-lookup"><span data-stu-id="ff530-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="ff530-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ff530-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff530-134">Windows</span><span class="sxs-lookup"><span data-stu-id="ff530-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
