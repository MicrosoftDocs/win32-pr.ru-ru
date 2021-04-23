---
title: Сообщение MM_WIM_DATA (Ммсистем. h)
description: Сообщение с \_ данными WIM в \_ формате mm отправляется в окно, когда в входном буфере содержатся аудиоданные-аудиозаписи и буфер возвращается приложению. Сообщение может быть отправлено либо при заполнении буфера, либо после вызова функции Вавеинресет.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682103"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="14b81-105">MM \_ , \_ сообщение с данными WIM</span><span class="sxs-lookup"><span data-stu-id="14b81-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="14b81-106">Сообщение **с \_ \_ данными WIM** в формате mm отправляется в окно, когда в входном буфере содержатся аудиоданные-аудиозаписи и буфер возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="14b81-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="14b81-107">Сообщение может быть отправлено либо при заполнении буфера, либо после вызова функции [**вавеинресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="14b81-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="14b81-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14b81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b81-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*хинпутдев*</span><span class="sxs-lookup"><span data-stu-id="14b81-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="14b81-110">Обработано устройство ввода аудио-сигнала, которое получило данные.</span><span class="sxs-lookup"><span data-stu-id="14b81-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="14b81-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*лпввхдр*</span><span class="sxs-lookup"><span data-stu-id="14b81-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="14b81-112">Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="14b81-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b81-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b81-113">Return Value</span></span>

<span data-ttu-id="14b81-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14b81-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b81-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14b81-115">Remarks</span></span>

<span data-ttu-id="14b81-116">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="14b81-116">The returned buffer might not be full.</span></span> <span data-ttu-id="14b81-117">Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , заданную параметром *lParam* .</span><span class="sxs-lookup"><span data-stu-id="14b81-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b81-118">Требования</span><span class="sxs-lookup"><span data-stu-id="14b81-118">Requirements</span></span>



| <span data-ttu-id="14b81-119">Требование</span><span class="sxs-lookup"><span data-stu-id="14b81-119">Requirement</span></span> | <span data-ttu-id="14b81-120">Значение</span><span class="sxs-lookup"><span data-stu-id="14b81-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b81-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14b81-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14b81-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14b81-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14b81-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14b81-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14b81-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14b81-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14b81-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14b81-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b81-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14b81-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b81-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14b81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b81-128">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="14b81-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="14b81-129">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="14b81-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

