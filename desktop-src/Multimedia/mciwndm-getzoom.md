---
title: Сообщение MCIWNDM_GETZOOM (VFW. h)
description: Сообщение МЦИВНДМ \_ Zoom получает текущее значение масштаба, используемое устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетзум.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490119"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="7c9ad-105">\_Сообщение МЦИВНДМ Zoom</span><span class="sxs-lookup"><span data-stu-id="7c9ad-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="7c9ad-106">Сообщение **МЦИВНДМ \_ Zoom** получает текущее значение масштаба, используемое устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="7c9ad-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="7c9ad-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="7c9ad-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7c9ad-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c9ad-108">Return Value</span></span>

<span data-ttu-id="7c9ad-109">Возвращает последние значения, используемые с [**мЦивндм \_ сетзум**](mciwndm-setzoom.md).</span><span class="sxs-lookup"><span data-stu-id="7c9ad-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9ad-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c9ad-110">Remarks</span></span>

<span data-ttu-id="7c9ad-111">Возвращаемое значение 100 означает, что изображение не масштабируется.</span><span class="sxs-lookup"><span data-stu-id="7c9ad-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="7c9ad-112">Значение 200 указывает, что изображение увеличивается вдвое в два раза.</span><span class="sxs-lookup"><span data-stu-id="7c9ad-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="7c9ad-113">Значение 50 указывает, что изображение уменьшается до половины исходного размера.</span><span class="sxs-lookup"><span data-stu-id="7c9ad-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9ad-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7c9ad-114">Requirements</span></span>



| <span data-ttu-id="7c9ad-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7c9ad-115">Requirement</span></span> | <span data-ttu-id="7c9ad-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c9ad-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7c9ad-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c9ad-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9ad-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c9ad-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7c9ad-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c9ad-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9ad-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7c9ad-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c9ad-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7c9ad-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9ad-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9ad-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9ad-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c9ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9ad-124">**мЦивнджетзум**</span><span class="sxs-lookup"><span data-stu-id="7c9ad-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="7c9ad-125">**МЦИВНДМ \_ сетзум**</span><span class="sxs-lookup"><span data-stu-id="7c9ad-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





