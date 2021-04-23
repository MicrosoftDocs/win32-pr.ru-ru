---
title: Сообщение MM_WOM_DONE (Ммсистем. h)
description: Сообщение о \_ \_ завершении вом mm отправляется в окно, когда заданный выходной буфер возвращается приложению. Буферы возвращаются в приложение, когда они воспроизводятся, или в результате вызова функции Вавеаутресет.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804085"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="a0735-105">\_Сообщение о \_ завершении вом mm</span><span class="sxs-lookup"><span data-stu-id="a0735-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="a0735-106">Сообщение **о \_ \_ завершении вом mm** отправляется в окно, когда заданный выходной буфер возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="a0735-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="a0735-107">Буферы возвращаются в приложение, когда они воспроизводятся, или в результате вызова функции [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="a0735-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="a0735-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0735-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*хаутпутдев*</span><span class="sxs-lookup"><span data-stu-id="a0735-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="a0735-110">Маркер устройства вывода аудио аудио, который воспроизводил буфер.</span><span class="sxs-lookup"><span data-stu-id="a0735-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a0735-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*лпввхдр*</span><span class="sxs-lookup"><span data-stu-id="a0735-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="a0735-112">Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер.</span><span class="sxs-lookup"><span data-stu-id="a0735-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0735-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0735-113">Return Value</span></span>

<span data-ttu-id="a0735-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0735-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0735-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a0735-115">Requirements</span></span>



| <span data-ttu-id="a0735-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a0735-116">Requirement</span></span> | <span data-ttu-id="a0735-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a0735-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0735-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0735-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a0735-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0735-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a0735-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0735-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a0735-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a0735-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a0735-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a0735-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0735-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0735-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0735-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0735-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0735-125">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="a0735-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="a0735-126">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="a0735-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

