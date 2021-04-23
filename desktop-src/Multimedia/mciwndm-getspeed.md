---
title: Сообщение MCIWNDM_GETSPEED (VFW. h)
description: Сообщение МЦИВНДМ \_ Speed получает скорость воспроизведения устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивнджетспид.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492819"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="faf1b-105">\_Сообщение МЦИВНДМ Speed</span><span class="sxs-lookup"><span data-stu-id="faf1b-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="faf1b-106">Сообщение **МЦИВНДМ \_ Speed** получает скорость воспроизведения устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="faf1b-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="faf1b-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетспид**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="faf1b-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="faf1b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="faf1b-108">Return Value</span></span>

<span data-ttu-id="faf1b-109">При успешном выполнении возвращает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="faf1b-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="faf1b-110">Значение обычной скорости — 1000.</span><span class="sxs-lookup"><span data-stu-id="faf1b-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="faf1b-111">Большие значения указывают более быстрые скорости, а меньшие значения — медленные.</span><span class="sxs-lookup"><span data-stu-id="faf1b-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf1b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="faf1b-112">Requirements</span></span>



| <span data-ttu-id="faf1b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="faf1b-113">Requirement</span></span> | <span data-ttu-id="faf1b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="faf1b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="faf1b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="faf1b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="faf1b-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="faf1b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="faf1b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="faf1b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="faf1b-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="faf1b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="faf1b-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="faf1b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="faf1b-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="faf1b-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf1b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="faf1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf1b-122">**мЦивнджетспид**</span><span class="sxs-lookup"><span data-stu-id="faf1b-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





