---
title: Сообщение WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Сообщение о \_ \_ \_ неостановкой кадра захвата для WM \_ замещает буфер кадров одним несжатым кадром с устройства записи и отображает его.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892417"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="8b83c-104">\_Сообщение о \_ \_ \_ неостановкой кадра захвата WM Cap</span><span class="sxs-lookup"><span data-stu-id="8b83c-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="8b83c-105">Сообщение **о \_ \_ \_ \_ Неостановкой кадра захвата для WM** замещает буфер кадров одним несжатым кадром с устройства записи и отображает его.</span><span class="sxs-lookup"><span data-stu-id="8b83c-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="8b83c-106">В отличие от сообщения [**с \_ закреплением \_ \_ WM**](wm-cap-grab-frame.md) , состояние наложения или предварительного просмотра не изменяется этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="8b83c-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="8b83c-107">Это сообщение можно отправить явно или с помощью макроса [**капграбфраменостоп**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .</span><span class="sxs-lookup"><span data-stu-id="8b83c-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="8b83c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b83c-108">Return Value</span></span>

<span data-ttu-id="8b83c-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8b83c-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b83c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b83c-110">Remarks</span></span>

<span data-ttu-id="8b83c-111">Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="8b83c-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b83c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8b83c-112">Requirements</span></span>



| <span data-ttu-id="8b83c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8b83c-113">Requirement</span></span> | <span data-ttu-id="8b83c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8b83c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8b83c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b83c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8b83c-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b83c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8b83c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b83c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8b83c-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b83c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b83c-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8b83c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b83c-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b83c-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b83c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b83c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b83c-122">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="8b83c-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8b83c-123">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="8b83c-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





