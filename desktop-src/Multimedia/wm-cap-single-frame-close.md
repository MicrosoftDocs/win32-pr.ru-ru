---
title: Сообщение WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: Сообщение о \_ \_ закрытии одинарного кадра WM Cap \_ \_ закрывает файл записи, Открытый \_ \_ \_ \_ сообщением об открытом фрейме WM Cap. Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефрамеклосе.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803809"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="2d087-105">\_Сообщение о \_ \_ \_ закрытии одиночного кадра WM Cap</span><span class="sxs-lookup"><span data-stu-id="2d087-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="2d087-106">Сообщение **о \_ \_ \_ \_ закрытии одинарного кадра WM Cap** закрывает файл записи, Открытый сообщением об [**\_ \_ \_ \_ открытом фрейме WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="2d087-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="2d087-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресинглефрамеклосе**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .</span><span class="sxs-lookup"><span data-stu-id="2d087-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2d087-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d087-108">Return Value</span></span>

<span data-ttu-id="2d087-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2d087-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d087-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d087-110">Remarks</span></span>

<span data-ttu-id="2d087-111">Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="2d087-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d087-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2d087-112">Requirements</span></span>



| <span data-ttu-id="2d087-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2d087-113">Requirement</span></span> | <span data-ttu-id="2d087-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2d087-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d087-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d087-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2d087-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d087-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d087-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d087-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2d087-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2d087-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2d087-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2d087-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d087-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d087-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d087-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d087-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d087-122">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="2d087-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2d087-123">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2d087-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





