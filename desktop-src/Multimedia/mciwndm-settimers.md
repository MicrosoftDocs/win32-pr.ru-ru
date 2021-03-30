---
title: Сообщение MCIWNDM_SETTIMERS (VFW. h)
description: Сообщение МЦИВНДМ \_ сеттимерс задает периоды обновления, используемые мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении, отображаемых в строке заголовка окна, и отправки сообщений уведомления родительскому окну.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801325"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="24da7-104">\_Сообщение мЦивндм сеттимерс</span><span class="sxs-lookup"><span data-stu-id="24da7-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="24da7-105">Сообщение **мЦивндм \_ сеттимерс** задает периоды обновления, используемые мЦивнд для обновления TrackBar в окне мЦивнд, обновления сведений о положении, отображаемых в строке заголовка окна, и отправки сообщений уведомления родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="24da7-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="24da7-106">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсеттимерс**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="24da7-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="24da7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24da7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24da7-108"><span id="active"></span><span id="ACTIVE"></span>*Active*</span><span class="sxs-lookup"><span data-stu-id="24da7-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="24da7-109">Период обновления, используемый МЦивнд, если это активное окно.</span><span class="sxs-lookup"><span data-stu-id="24da7-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="24da7-110">Значение по умолчанию — 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="24da7-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="24da7-111">Размер хранилища для этого значения ограничен 16 битами.</span><span class="sxs-lookup"><span data-stu-id="24da7-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="24da7-112"><span id="inactive"></span><span id="INACTIVE"></span>*Активный*</span><span class="sxs-lookup"><span data-stu-id="24da7-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="24da7-113">Период обновления, используемый МЦивнд, если это неактивное окно.</span><span class="sxs-lookup"><span data-stu-id="24da7-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="24da7-114">Значение по умолчанию — 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="24da7-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="24da7-115">Размер хранилища для этого значения ограничен 16 битами.</span><span class="sxs-lookup"><span data-stu-id="24da7-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24da7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24da7-116">Return Value</span></span>

<span data-ttu-id="24da7-117">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="24da7-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24da7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="24da7-118">Requirements</span></span>



| <span data-ttu-id="24da7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="24da7-119">Requirement</span></span> | <span data-ttu-id="24da7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="24da7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="24da7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24da7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24da7-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24da7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24da7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24da7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24da7-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24da7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="24da7-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="24da7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24da7-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="24da7-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24da7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24da7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24da7-128">**мЦивндсеттимерс**</span><span class="sxs-lookup"><span data-stu-id="24da7-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





