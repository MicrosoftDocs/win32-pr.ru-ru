---
title: Сообщение WM_CAP_EDIT_COPY (VFW. h)
description: '\_ \_ Сообщение об изменении копии с креплениями WM \_ копирует содержимое буфера кадров видео и связанной с ним палитры в буфер обмена. Это сообщение можно отправить явно или с помощью макроса Капедиткопи.'
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136579"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="159ca-105">\_ \_ Сообщение об изменении копии с КРЕПЛЕНИЯми WM \_</span><span class="sxs-lookup"><span data-stu-id="159ca-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="159ca-106">Сообщение **об \_ \_ изменении \_ копии с креплениями WM** копирует содержимое буфера кадров видео и связанной с ним палитры в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="159ca-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="159ca-107">Это сообщение можно отправить явно или с помощью макроса [**капедиткопи**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .</span><span class="sxs-lookup"><span data-stu-id="159ca-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="159ca-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="159ca-108">Return Value</span></span>

<span data-ttu-id="159ca-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="159ca-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="159ca-110">Требования</span><span class="sxs-lookup"><span data-stu-id="159ca-110">Requirements</span></span>



| <span data-ttu-id="159ca-111">Требование</span><span class="sxs-lookup"><span data-stu-id="159ca-111">Requirement</span></span> | <span data-ttu-id="159ca-112">Значение</span><span class="sxs-lookup"><span data-stu-id="159ca-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="159ca-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="159ca-113">Minimum supported client</span></span><br/> | <span data-ttu-id="159ca-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="159ca-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="159ca-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="159ca-115">Minimum supported server</span></span><br/> | <span data-ttu-id="159ca-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="159ca-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="159ca-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="159ca-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="159ca-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="159ca-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159ca-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="159ca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159ca-120">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="159ca-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="159ca-121">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="159ca-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





