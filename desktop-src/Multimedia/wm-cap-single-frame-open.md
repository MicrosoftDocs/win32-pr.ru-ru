---
title: Сообщение WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: '\_ \_ \_ При открытии сообщения с одним кадром WM Cap \_ открывается файл записи для однокадровой записи. Все предыдущие сведения в файле записи перезаписываются. Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефрамеопен.'
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892634"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="ee916-106">\_ \_ \_ Сообщение об открытом одном кадре WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="ee916-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="ee916-107">При **открытии сообщения с \_ \_ одним \_ кадром \_ WM Cap** открывается файл записи для однокадровой записи.</span><span class="sxs-lookup"><span data-stu-id="ee916-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="ee916-108">Все предыдущие сведения в файле записи перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="ee916-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="ee916-109">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресинглефрамеопен**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .</span><span class="sxs-lookup"><span data-stu-id="ee916-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="ee916-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee916-110">Return Value</span></span>

<span data-ttu-id="ee916-111">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ee916-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee916-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee916-112">Remarks</span></span>

<span data-ttu-id="ee916-113">Дополнительные сведения об установке функций обратного вызова см. в разделе [**\_ \_ \_ \_ ошибка обратного вызова Set крепления WM**](wm-cap-set-callback-error.md) , а также сообщения [**\_ \_ \_ \_ кадра обратного вызова Set крепления WM**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="ee916-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee916-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ee916-114">Requirements</span></span>



| <span data-ttu-id="ee916-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ee916-115">Requirement</span></span> | <span data-ttu-id="ee916-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ee916-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ee916-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee916-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee916-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee916-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ee916-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee916-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee916-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee916-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ee916-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ee916-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee916-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee916-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee916-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee916-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee916-124">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="ee916-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ee916-125">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ee916-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





