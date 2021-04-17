---
title: Сообщение WOM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии вом отправляется в функцию выходного обратного вызова звуковой волны при закрытии выходного устройства аудио аудио. После отправки этого сообщения маркер устройства больше не действителен.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672605"
---
# <a name="wom_close-message"></a><span data-ttu-id="b1623-105">\_Сообщение о закрытии ВОМ</span><span class="sxs-lookup"><span data-stu-id="b1623-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="b1623-106">Сообщение **о \_ закрытии вом** отправляется в функцию выходного обратного вызова звуковой волны при закрытии выходного устройства аудио аудио.</span><span class="sxs-lookup"><span data-stu-id="b1623-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="b1623-107">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="b1623-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b1623-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1623-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1623-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b1623-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b1623-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b1623-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b1623-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b1623-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b1623-112">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b1623-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1623-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1623-113">Return Value</span></span>

<span data-ttu-id="b1623-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b1623-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1623-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b1623-115">Requirements</span></span>



| <span data-ttu-id="b1623-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b1623-116">Requirement</span></span> | <span data-ttu-id="b1623-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b1623-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1623-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1623-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1623-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1623-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1623-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1623-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1623-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1623-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1623-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b1623-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1623-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1623-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1623-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1623-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1623-125">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="b1623-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="b1623-126">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="b1623-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





