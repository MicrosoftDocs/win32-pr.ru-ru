---
description: Посылается, когда приложение запрашивает создание окна с помощью вызова функции CreateWindowEx или CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Сообщение WM_CREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702578"
---
# <a name="wm_create-message"></a><span data-ttu-id="de71a-103">\_Создание сообщения WM</span><span class="sxs-lookup"><span data-stu-id="de71a-103">WM\_CREATE message</span></span>

<span data-ttu-id="de71a-104">Посылается, когда приложение запрашивает создание окна с помощью вызова функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) или [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="de71a-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="de71a-105">(Сообщение отправляется перед возвратом функции.) Процедура окна нового окна получает это сообщение после создания окна, но до того, как окно становится видимым.</span><span class="sxs-lookup"><span data-stu-id="de71a-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="de71a-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="de71a-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="de71a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="de71a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de71a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de71a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de71a-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="de71a-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="de71a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de71a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de71a-111">Указатель на структуру [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) , содержащую сведения о создаваемом окне.</span><span class="sxs-lookup"><span data-stu-id="de71a-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de71a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de71a-112">Return value</span></span>

<span data-ttu-id="de71a-113">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="de71a-113">Type: **LRESULT**</span></span>

<span data-ttu-id="de71a-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль, чтобы продолжить создание окна.</span><span class="sxs-lookup"><span data-stu-id="de71a-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="de71a-115">Если приложение возвращает значение – 1, окно уничтожается, а функция [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) или [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) возвращает **нулевой** маркер.</span><span class="sxs-lookup"><span data-stu-id="de71a-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="de71a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="de71a-116">Requirements</span></span>



| <span data-ttu-id="de71a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="de71a-117">Requirement</span></span> | <span data-ttu-id="de71a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="de71a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de71a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de71a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de71a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de71a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="de71a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de71a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de71a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de71a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de71a-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="de71a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de71a-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de71a-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de71a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de71a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="de71a-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="de71a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de71a-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="de71a-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="de71a-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="de71a-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="de71a-129">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="de71a-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="de71a-130">**WM \_ нккреате**</span><span class="sxs-lookup"><span data-stu-id="de71a-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="de71a-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="de71a-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de71a-132">Windows</span><span class="sxs-lookup"><span data-stu-id="de71a-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
