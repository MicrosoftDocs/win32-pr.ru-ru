---
title: Сообщение WIM_DATA (Ммсистем. h)
description: Сообщение с \_ данными WIM отправляется в указанную функцию обратного вызова аудио-звука, когда в входном буфере содержатся данные звуковой волны, а буфер возвращается приложению.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672813"
---
# <a name="wim_data-message"></a><span data-ttu-id="2ba78-104">\_Сообщение данных WIM</span><span class="sxs-lookup"><span data-stu-id="2ba78-104">WIM\_DATA message</span></span>

<span data-ttu-id="2ba78-105">Сообщение **с \_ данными WIM** отправляется в указанную функцию обратного вызова аудио-звука, когда в входном буфере содержатся данные звуковой волны, а буфер возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="2ba78-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="2ba78-106">Сообщение может быть отправлено, когда буфер полон или после вызова функции [**вавеинресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="2ba78-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="2ba78-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ba78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba78-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="2ba78-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2ba78-109">Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="2ba78-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="2ba78-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="2ba78-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2ba78-111">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2ba78-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba78-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ba78-112">Return Value</span></span>

<span data-ttu-id="2ba78-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2ba78-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba78-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ba78-114">Remarks</span></span>

<span data-ttu-id="2ba78-115">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="2ba78-115">The returned buffer might not be full.</span></span> <span data-ttu-id="2ba78-116">Используйте элемент **двбитесрекордед** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , заданную параметром *лпввхдр* , чтобы определить число байтов, записанных в возвращенный буфер.</span><span class="sxs-lookup"><span data-stu-id="2ba78-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba78-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2ba78-117">Requirements</span></span>



| <span data-ttu-id="2ba78-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2ba78-118">Requirement</span></span> | <span data-ttu-id="2ba78-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ba78-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba78-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ba78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba78-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ba78-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2ba78-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ba78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba78-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ba78-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2ba78-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2ba78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ba78-125"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ba78-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba78-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ba78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba78-127">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="2ba78-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="2ba78-128">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="2ba78-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

