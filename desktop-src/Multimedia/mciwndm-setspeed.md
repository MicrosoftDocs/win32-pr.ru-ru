---
title: Сообщение MCIWNDM_SETSPEED (VFW. h)
description: Сообщение МЦИВНДМ \_ сетспид задает скорость воспроизведения устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивндсетспид.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988960"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="5f84e-105">\_Сообщение мЦивндм сетспид</span><span class="sxs-lookup"><span data-stu-id="5f84e-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="5f84e-106">Сообщение **мЦивндм \_ сетспид** задает скорость воспроизведения устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="5f84e-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="5f84e-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетспид**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="5f84e-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="5f84e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f84e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f84e-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*испид*</span><span class="sxs-lookup"><span data-stu-id="5f84e-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="5f84e-110">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5f84e-110">Playback speed.</span></span> <span data-ttu-id="5f84e-111">Укажите 1000 для обычной скорости, более высокие значения для более быстрых скоростей и меньшие значения для медленных скоростей.</span><span class="sxs-lookup"><span data-stu-id="5f84e-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f84e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f84e-112">Return Value</span></span>

<span data-ttu-id="5f84e-113">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5f84e-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f84e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5f84e-114">Requirements</span></span>



| <span data-ttu-id="5f84e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5f84e-115">Requirement</span></span> | <span data-ttu-id="5f84e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5f84e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f84e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f84e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f84e-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f84e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5f84e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f84e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f84e-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5f84e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f84e-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5f84e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f84e-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f84e-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f84e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f84e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f84e-124">**мЦивндсетспид**</span><span class="sxs-lookup"><span data-stu-id="5f84e-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





