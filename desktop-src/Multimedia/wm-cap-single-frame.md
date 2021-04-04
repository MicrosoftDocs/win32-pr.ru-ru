---
title: Сообщение WM_CAP_SINGLE_FRAME (VFW. h)
description: Сообщение с \_ \_ одним \_ кадром WM Cap добавляет один кадр в файл записи, Открытый с помощью \_ \_ \_ сообщения об открытом фрейме WM Cap \_ . Это сообщение можно отправить явно или с помощью макроса Капкаптуресинглефраме.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137511"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="2096d-105">\_ \_ \_ Сообщение об одном кадре WM Cap</span><span class="sxs-lookup"><span data-stu-id="2096d-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="2096d-106">Сообщение **с \_ \_ одним \_ кадром WM Cap** добавляет один кадр в файл записи, Открытый с помощью сообщения об [**\_ \_ \_ \_ открытом фрейме WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="2096d-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="2096d-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресинглефраме**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .</span><span class="sxs-lookup"><span data-stu-id="2096d-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2096d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2096d-108">Return Value</span></span>

<span data-ttu-id="2096d-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2096d-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2096d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2096d-110">Requirements</span></span>



| <span data-ttu-id="2096d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="2096d-111">Requirement</span></span> | <span data-ttu-id="2096d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2096d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2096d-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2096d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2096d-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2096d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2096d-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2096d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2096d-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2096d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2096d-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2096d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2096d-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2096d-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2096d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2096d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2096d-120">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="2096d-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2096d-121">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="2096d-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





