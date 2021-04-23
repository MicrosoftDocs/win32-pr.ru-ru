---
title: Сообщение WM_POINTERDEVICEOUTOFRANGE
description: Отправляется в окно, когда устройство-указатель находится в диапазоне входного дигитайзера. Это сообщение содержит сведения об устройстве и его сходстве.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- WM_POINTERDEVICEOUTOFRANGE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135623"
---
# <a name="wm_pointerdeviceoutofrange-message"></a><span data-ttu-id="2563a-105">Сообщение WM_POINTERDEVICEOUTOFRANGE</span><span class="sxs-lookup"><span data-stu-id="2563a-105">WM_POINTERDEVICEOUTOFRANGE message</span></span>

<span data-ttu-id="2563a-106">Отправляется в окно, когда устройство-указатель находится в диапазоне входного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="2563a-106">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="2563a-107">Это сообщение содержит сведения об устройстве и его сходстве.</span><span class="sxs-lookup"><span data-stu-id="2563a-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="2563a-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="2563a-108">\[!Important\]</span></span>  
> <span data-ttu-id="2563a-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="2563a-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="2563a-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="2563a-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="2563a-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="2563a-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="2563a-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2563a-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a><span data-ttu-id="2563a-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="2563a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2563a-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2563a-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2563a-115">Дополнительные сведения, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="2563a-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="2563a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2563a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2563a-117">Дополнительные сведения, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="2563a-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2563a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2563a-118">Return value</span></span>

<span data-ttu-id="2563a-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="2563a-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="2563a-120">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="2563a-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="2563a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2563a-121">Requirements</span></span>



| <span data-ttu-id="2563a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2563a-122">Requirement</span></span> | <span data-ttu-id="2563a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2563a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2563a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2563a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2563a-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2563a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="2563a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2563a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2563a-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2563a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2563a-128">Header</span><span class="sxs-lookup"><span data-stu-id="2563a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2563a-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2563a-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2563a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2563a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2563a-131">Сообщения</span><span class="sxs-lookup"><span data-stu-id="2563a-131">Messages</span></span>](messages.md)
</dt> </dl>

 

