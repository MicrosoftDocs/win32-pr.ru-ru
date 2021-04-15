---
title: Сообщение MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Сообщение МЦИВНДМ \_ жетинактиветимер получает период обновления, используемый, когда окно мЦивнд является неактивным окном. Это сообщение можно отправить явно или с помощью макроса МЦивнджетинактиветимер.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672497"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="b3042-105">\_Сообщение мЦивндм жетинактиветимер</span><span class="sxs-lookup"><span data-stu-id="b3042-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="b3042-106">Сообщение **мЦивндм \_ жетинактиветимер** получает период обновления, используемый, когда окно мЦивнд является неактивным окном.</span><span class="sxs-lookup"><span data-stu-id="b3042-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="b3042-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="b3042-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b3042-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3042-108">Return Value</span></span>

<span data-ttu-id="b3042-109">Возвращает период обновления в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="b3042-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="b3042-110">Значение по умолчанию — 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="b3042-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3042-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b3042-111">Requirements</span></span>



| <span data-ttu-id="b3042-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b3042-112">Requirement</span></span> | <span data-ttu-id="b3042-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b3042-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3042-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3042-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b3042-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3042-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3042-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3042-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b3042-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3042-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b3042-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b3042-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3042-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3042-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3042-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3042-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3042-121">**мЦивнджетинактиветимер**</span><span class="sxs-lookup"><span data-stu-id="b3042-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





