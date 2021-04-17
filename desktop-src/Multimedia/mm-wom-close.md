---
title: Сообщение MM_WOM_CLOSE (Ммсистем. h)
description: '\_ \_ При закрытии выходного устройства аудио-аудио в окно отправляется сообщение о закрытии вом mm. После отправки этого сообщения маркер устройства больше не действителен.'
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682160"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="d9a6d-105">MM \_ ВОМ, \_ сообщение о закрытии</span><span class="sxs-lookup"><span data-stu-id="d9a6d-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="d9a6d-106">При закрытии выходного устройства аудио-аудио в окно отправляется сообщение о **\_ \_ закрытии вом mm** .</span><span class="sxs-lookup"><span data-stu-id="d9a6d-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="d9a6d-107">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="d9a6d-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d9a6d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9a6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a6d-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*хаутпутдев*</span><span class="sxs-lookup"><span data-stu-id="d9a6d-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="d9a6d-110">Обработчик для закрытого устройства.</span><span class="sxs-lookup"><span data-stu-id="d9a6d-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="d9a6d-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9a6d-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d9a6d-112">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d9a6d-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a6d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9a6d-113">Return Value</span></span>

<span data-ttu-id="d9a6d-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d9a6d-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a6d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d9a6d-115">Requirements</span></span>



| <span data-ttu-id="d9a6d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d9a6d-116">Requirement</span></span> | <span data-ttu-id="d9a6d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a6d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9a6d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a6d-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9a6d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d9a6d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9a6d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a6d-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9a6d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9a6d-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9a6d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9a6d-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9a6d-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a6d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9a6d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a6d-125">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="d9a6d-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="d9a6d-126">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="d9a6d-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





