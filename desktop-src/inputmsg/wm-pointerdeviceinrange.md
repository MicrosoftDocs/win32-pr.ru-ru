---
title: Сообщение WM_POINTERDEVICEINRANGE
description: Отправляется в окно при обнаружении устройства-указателя в пределах диапазона входного дигитайзера. Это сообщение содержит сведения об устройстве и его сходстве.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535153"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="a9e00-105">Сообщение WM_POINTERDEVICEINRANGE</span><span class="sxs-lookup"><span data-stu-id="a9e00-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="a9e00-106">Отправляется в окно при обнаружении устройства-указателя в пределах диапазона входного дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="a9e00-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="a9e00-107">Это сообщение содержит сведения об устройстве и его сходстве.</span><span class="sxs-lookup"><span data-stu-id="a9e00-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="a9e00-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="a9e00-108">\[!Important\]</span></span>  
> <span data-ttu-id="a9e00-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="a9e00-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="a9e00-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="a9e00-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="a9e00-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="a9e00-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="a9e00-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9e00-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="a9e00-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9e00-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9e00-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9e00-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e00-115">Дополнительные сведения, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="a9e00-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="a9e00-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9e00-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9e00-117">Дополнительные сведения, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="a9e00-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9e00-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9e00-118">Return value</span></span>

<span data-ttu-id="a9e00-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a9e00-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="a9e00-120">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a9e00-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e00-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a9e00-121">Requirements</span></span>



| <span data-ttu-id="a9e00-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a9e00-122">Requirement</span></span> | <span data-ttu-id="a9e00-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a9e00-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e00-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9e00-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e00-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9e00-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a9e00-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9e00-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e00-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9e00-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9e00-128">Header</span><span class="sxs-lookup"><span data-stu-id="a9e00-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9e00-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9e00-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9e00-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9e00-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e00-131">Сообщения</span><span class="sxs-lookup"><span data-stu-id="a9e00-131">Messages</span></span>](messages.md)
</dt> </dl>

 

