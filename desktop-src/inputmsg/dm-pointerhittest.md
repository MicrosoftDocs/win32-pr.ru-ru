---
title: Сообщение DM_POINTERHITTEST
description: Отправляется в окно при первом обнаружении входных указателей для определения наиболее вероятного целевого объекта ввода для непосредственной манипуляции.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136687"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="711d9-104">Сообщение DM_POINTERHITTEST</span><span class="sxs-lookup"><span data-stu-id="711d9-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="711d9-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="711d9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="711d9-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="711d9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="711d9-107">Отправляется в окно при первом обнаружении входных указателей для определения наиболее вероятного целевого объекта ввода для [непосредственной манипуляции](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span><span class="sxs-lookup"><span data-stu-id="711d9-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="711d9-108">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="711d9-108">\[!Important\]</span></span>  
> <span data-ttu-id="711d9-109">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="711d9-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="711d9-110">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="711d9-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="711d9-111">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="711d9-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="711d9-112">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="711d9-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="711d9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="711d9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d9-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="711d9-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d9-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="711d9-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="711d9-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="711d9-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="711d9-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="711d9-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="711d9-118">Return value</span></span>

<span data-ttu-id="711d9-119">NULL</span><span class="sxs-lookup"><span data-stu-id="711d9-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="711d9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="711d9-120">Requirements</span></span>



| <span data-ttu-id="711d9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="711d9-121">Requirement</span></span> | <span data-ttu-id="711d9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="711d9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711d9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="711d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="711d9-124">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="711d9-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="711d9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="711d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="711d9-126">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="711d9-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="711d9-127">Header</span><span class="sxs-lookup"><span data-stu-id="711d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="711d9-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="711d9-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711d9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="711d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711d9-130">Сообщения</span><span class="sxs-lookup"><span data-stu-id="711d9-130">Messages</span></span>](messages.md)
</dt> </dl>

 

