---
title: Сообщение MM_WIM_CLOSE (Ммсистем. h)
description: Сообщение о закрытии \_ WIM-файла mm \_ отправляется в окно при закрытии входного устройства звуковой волны. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071088"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="8c17f-105">MM \_ . \_ сообщение о закрытии WIM</span><span class="sxs-lookup"><span data-stu-id="8c17f-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="8c17f-106">Сообщение о закрытии **\_ WIM \_** -файла mm отправляется в окно при закрытии входного устройства звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="8c17f-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="8c17f-107">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="8c17f-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="8c17f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c17f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c17f-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*хинпутдев*</span><span class="sxs-lookup"><span data-stu-id="8c17f-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="8c17f-110">Обработано выходное устройство ввода аудио-сигнала, которое было закрыто.</span><span class="sxs-lookup"><span data-stu-id="8c17f-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="8c17f-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c17f-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8c17f-112">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8c17f-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c17f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c17f-113">Return Value</span></span>

<span data-ttu-id="8c17f-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8c17f-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c17f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8c17f-115">Requirements</span></span>



| <span data-ttu-id="8c17f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8c17f-116">Requirement</span></span> | <span data-ttu-id="8c17f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8c17f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c17f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c17f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c17f-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c17f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c17f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c17f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c17f-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c17f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c17f-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8c17f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c17f-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c17f-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c17f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c17f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c17f-125">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="8c17f-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="8c17f-126">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="8c17f-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





