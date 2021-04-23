---
title: Сообщение MCIWNDM_SETACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ сетактиветимер задает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении в строке заголовка окна и отправки сообщений уведомления родительскому окну, когда окно мЦивнд активно. Это сообщение можно отправить явно или с помощью макроса МЦивндсетактиветимер.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- MCIWNDM_SETACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136587"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="9303d-105">\_Сообщение мЦивндм сетактиветимер</span><span class="sxs-lookup"><span data-stu-id="9303d-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="9303d-106">Сообщение **мЦивндм \_ сетактиветимер** задает период обновления, используемый мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении в строке заголовка окна и отправки сообщений уведомления родительскому окну, когда окно мЦивнд активно.</span><span class="sxs-lookup"><span data-stu-id="9303d-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="9303d-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="9303d-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="9303d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9303d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9303d-109"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="9303d-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="9303d-110">Период обновления (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="9303d-110">Update period, in milliseconds.</span></span> <span data-ttu-id="9303d-111">Значение по умолчанию — 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="9303d-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9303d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9303d-112">Return Value</span></span>

<span data-ttu-id="9303d-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9303d-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9303d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9303d-114">Requirements</span></span>



| <span data-ttu-id="9303d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9303d-115">Requirement</span></span> | <span data-ttu-id="9303d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9303d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9303d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9303d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9303d-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9303d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9303d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9303d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9303d-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9303d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9303d-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9303d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9303d-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9303d-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9303d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9303d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9303d-124">**мЦивндсетактиветимер**</span><span class="sxs-lookup"><span data-stu-id="9303d-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





