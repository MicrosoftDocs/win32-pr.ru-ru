---
title: Сообщение WIM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии WIM отправляется в указанную функцию обратного вызова звукового сигнала аудио при закрытии устройства ввода аудио-сигнала. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492609"
---
# <a name="wim_close-message"></a><span data-ttu-id="dbda8-105">\_Сообщение о закрытии WIM</span><span class="sxs-lookup"><span data-stu-id="dbda8-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="dbda8-106">Сообщение **о \_ закрытии WIM** отправляется в указанную функцию обратного вызова звукового сигнала аудио при закрытии устройства ввода аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="dbda8-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="dbda8-107">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="dbda8-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="dbda8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbda8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbda8-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="dbda8-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dbda8-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dbda8-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbda8-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="dbda8-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dbda8-112">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dbda8-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbda8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbda8-113">Return Value</span></span>

<span data-ttu-id="dbda8-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dbda8-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbda8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="dbda8-115">Requirements</span></span>



| <span data-ttu-id="dbda8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="dbda8-116">Requirement</span></span> | <span data-ttu-id="dbda8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dbda8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbda8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbda8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbda8-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbda8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dbda8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbda8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbda8-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dbda8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dbda8-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dbda8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbda8-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbda8-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbda8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbda8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbda8-125">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="dbda8-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="dbda8-126">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="dbda8-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





