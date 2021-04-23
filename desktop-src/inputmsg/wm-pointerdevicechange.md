---
title: Сообщение WM_POINTERDEVICECHANGE
description: Отправляется в окно при изменении параметров монитора, к которому присоединен дигитайзер. Это сообщение содержит сведения о масштабировании режима экрана.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719197"
---
# <a name="wm_pointerdevicechange-message"></a><span data-ttu-id="fe2f2-105">Сообщение WM_POINTERDEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="fe2f2-105">WM_POINTERDEVICECHANGE message</span></span>

<span data-ttu-id="fe2f2-106">Отправляется в окно при изменении параметров монитора, к которому присоединен дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-106">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="fe2f2-107">Это сообщение содержит сведения о масштабировании режима экрана.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-107">This message contains information regarding the scaling of the display mode.</span></span>

> <span data-ttu-id="fe2f2-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="fe2f2-108">\[!Important\]</span></span>  
> <span data-ttu-id="fe2f2-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="fe2f2-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="fe2f2-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="fe2f2-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="fe2f2-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe2f2-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a><span data-ttu-id="fe2f2-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe2f2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2f2-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe2f2-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2f2-115">Содержит значение от [**констант изменения указателя на устройство**](pointer-device-change-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fe2f2-115">Contains a value from [**Pointer Device Change Constants**](pointer-device-change-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe2f2-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe2f2-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2f2-117">Дополнительные сведения, относящиеся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2f2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe2f2-118">Return value</span></span>

<span data-ttu-id="fe2f2-119">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="fe2f2-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="fe2f2-120">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="fe2f2-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2f2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fe2f2-121">Requirements</span></span>



| <span data-ttu-id="fe2f2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fe2f2-122">Requirement</span></span> | <span data-ttu-id="fe2f2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fe2f2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2f2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe2f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2f2-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe2f2-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="fe2f2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe2f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2f2-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe2f2-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe2f2-128">Header</span><span class="sxs-lookup"><span data-stu-id="fe2f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe2f2-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe2f2-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2f2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe2f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2f2-131">Сообщения</span><span class="sxs-lookup"><span data-stu-id="fe2f2-131">Messages</span></span>](messages.md)
</dt> </dl>

 

