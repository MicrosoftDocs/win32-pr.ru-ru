---
title: Сообщение MCIWNDM_SETINACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ сетинактиветимер устанавливает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновляет сведения о положении в строке заголовка окна и отправляет сообщения уведомления родительскому окну, когда окно мЦивнд неактивно. Это сообщение можно отправить явно или с помощью макроса МЦивндсетинактиветимер.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- MCIWNDM_SETINACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534637"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="077bf-105">\_Сообщение мЦивндм сетинактиветимер</span><span class="sxs-lookup"><span data-stu-id="077bf-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="077bf-106">Сообщение **мЦивндм \_ сетинактиветимер** устанавливает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновляет сведения о положении в строке заголовка окна и отправляет сообщения уведомления родительскому окну, когда окно мЦивнд неактивно.</span><span class="sxs-lookup"><span data-stu-id="077bf-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="077bf-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="077bf-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="077bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="077bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077bf-109"><span id="inactive"></span><span id="INACTIVE"></span>*Активный*</span><span class="sxs-lookup"><span data-stu-id="077bf-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="077bf-110">Период обновления (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="077bf-110">Update period, in milliseconds.</span></span> <span data-ttu-id="077bf-111">Значение по умолчанию — 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="077bf-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077bf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="077bf-112">Return Value</span></span>

<span data-ttu-id="077bf-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="077bf-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="077bf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="077bf-114">Requirements</span></span>



| <span data-ttu-id="077bf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="077bf-115">Requirement</span></span> | <span data-ttu-id="077bf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="077bf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="077bf-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="077bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="077bf-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="077bf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="077bf-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="077bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="077bf-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="077bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="077bf-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="077bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="077bf-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="077bf-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="077bf-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="077bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077bf-124">**мЦивндсетинактиветимер**</span><span class="sxs-lookup"><span data-stu-id="077bf-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





