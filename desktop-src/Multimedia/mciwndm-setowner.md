---
title: Сообщение MCIWNDM_SETOWNER (VFW. h)
description: Сообщение МЦИВНДМ \_ сетовнер указывает, что окно будет принимать сообщения уведомления, связанные с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсетовнер.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136591"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="59925-105">\_Сообщение мЦивндм сетовнер</span><span class="sxs-lookup"><span data-stu-id="59925-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="59925-106">Сообщение **мЦивндм \_ сетовнер** указывает, что окно будет принимать сообщения уведомления, связанные с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="59925-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="59925-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетовнер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="59925-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="59925-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="59925-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59925-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*хвндп*</span><span class="sxs-lookup"><span data-stu-id="59925-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="59925-110">Обработчик для окна, получающего сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="59925-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59925-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59925-111">Return Value</span></span>

<span data-ttu-id="59925-112">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="59925-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="59925-113">Требования</span><span class="sxs-lookup"><span data-stu-id="59925-113">Requirements</span></span>



| <span data-ttu-id="59925-114">Требование</span><span class="sxs-lookup"><span data-stu-id="59925-114">Requirement</span></span> | <span data-ttu-id="59925-115">Значение</span><span class="sxs-lookup"><span data-stu-id="59925-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="59925-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59925-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59925-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59925-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="59925-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59925-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59925-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="59925-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="59925-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="59925-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="59925-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="59925-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59925-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59925-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59925-123">**мЦивндсетовнер**</span><span class="sxs-lookup"><span data-stu-id="59925-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





