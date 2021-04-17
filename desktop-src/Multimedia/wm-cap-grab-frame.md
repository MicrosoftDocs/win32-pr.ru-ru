---
title: Сообщение WM_CAP_GRAB_FRAME (VFW. h)
description: Сообщение о \_ \_ кадре захвата WM Cap \_ извлекает и отображает один кадр из драйвера записи. После записи перекрытие и предварительный просмотр отключены. Это сообщение можно отправить явно или с помощью макроса Капграбфраме.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491145"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="7869b-106">\_Сообщение о \_ блоке захвата крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="7869b-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="7869b-107">Сообщение **о \_ \_ \_ кадре захвата WM Cap** извлекает и отображает один кадр из драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="7869b-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="7869b-108">После записи перекрытие и предварительный просмотр отключены.</span><span class="sxs-lookup"><span data-stu-id="7869b-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="7869b-109">Это сообщение можно отправить явно или с помощью макроса [**капграбфраме**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .</span><span class="sxs-lookup"><span data-stu-id="7869b-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="7869b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7869b-110">Return Value</span></span>

<span data-ttu-id="7869b-111">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7869b-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7869b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7869b-112">Remarks</span></span>

<span data-ttu-id="7869b-113">Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="7869b-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7869b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7869b-114">Requirements</span></span>



| <span data-ttu-id="7869b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7869b-115">Requirement</span></span> | <span data-ttu-id="7869b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7869b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7869b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7869b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7869b-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7869b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7869b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7869b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7869b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7869b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7869b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7869b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7869b-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7869b-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7869b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7869b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7869b-124">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="7869b-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7869b-125">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="7869b-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





