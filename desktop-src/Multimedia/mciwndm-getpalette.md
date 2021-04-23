---
title: Сообщение MCIWNDM_GETPALETTE (VFW. h)
description: Сообщение МЦИВНДМ \_ -Palette получает маркер палитры, используемый устройством MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетпалетте.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071232"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="66731-105">\_Сообщение мЦивндм</span><span class="sxs-lookup"><span data-stu-id="66731-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="66731-106">Сообщение **мЦивндм- \_ Palette** получает маркер палитры, используемый устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="66731-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="66731-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетпалетте**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="66731-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="66731-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66731-108">Return Value</span></span>

<span data-ttu-id="66731-109">Возвращает маркер палитры в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="66731-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="66731-110">Требования</span><span class="sxs-lookup"><span data-stu-id="66731-110">Requirements</span></span>



| <span data-ttu-id="66731-111">Требование</span><span class="sxs-lookup"><span data-stu-id="66731-111">Requirement</span></span> | <span data-ttu-id="66731-112">Значение</span><span class="sxs-lookup"><span data-stu-id="66731-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66731-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66731-113">Minimum supported client</span></span><br/> | <span data-ttu-id="66731-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66731-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66731-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66731-115">Minimum supported server</span></span><br/> | <span data-ttu-id="66731-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66731-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66731-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="66731-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="66731-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="66731-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66731-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66731-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66731-120">**мЦивнджетпалетте**</span><span class="sxs-lookup"><span data-stu-id="66731-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





