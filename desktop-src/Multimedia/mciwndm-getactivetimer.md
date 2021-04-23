---
title: Сообщение MCIWNDM_GETACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ жетактиветимер получает период обновления, используемый, когда окно мЦивнд является активным окном. Это сообщение можно отправить явно или с помощью макроса МЦивнджетактиветимер.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137799"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="7fd43-105">\_Сообщение мЦивндм жетактиветимер</span><span class="sxs-lookup"><span data-stu-id="7fd43-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="7fd43-106">Сообщение **мЦивндм \_ жетактиветимер** получает период обновления, используемый, когда окно мЦивнд является активным окном.</span><span class="sxs-lookup"><span data-stu-id="7fd43-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="7fd43-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="7fd43-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="7fd43-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fd43-108">Return Value</span></span>

<span data-ttu-id="7fd43-109">Возвращает период обновления в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="7fd43-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="7fd43-110">Значение по умолчанию — 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7fd43-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd43-111">Требования</span><span class="sxs-lookup"><span data-stu-id="7fd43-111">Requirements</span></span>



| <span data-ttu-id="7fd43-112">Требование</span><span class="sxs-lookup"><span data-stu-id="7fd43-112">Requirement</span></span> | <span data-ttu-id="7fd43-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7fd43-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fd43-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fd43-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd43-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7fd43-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fd43-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fd43-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd43-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7fd43-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fd43-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7fd43-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd43-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd43-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd43-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fd43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd43-121">**мЦивнджетактиветимер**</span><span class="sxs-lookup"><span data-stu-id="7fd43-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





