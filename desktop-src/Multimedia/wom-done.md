---
title: Сообщение WOM_DONE (Ммсистем. h)
description: Сообщение вом \_ done отправляется в функцию выходного обратного вызова звуковой волны, когда заданный выходной буфер возвращается приложению.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135259"
---
# <a name="wom_done-message"></a><span data-ttu-id="5b8da-104">\_Сообщение о завершении ВОМ</span><span class="sxs-lookup"><span data-stu-id="5b8da-104">WOM\_DONE message</span></span>

<span data-ttu-id="5b8da-105">Сообщение **вом \_ done** отправляется в функцию выходного обратного вызова звуковой волны, когда заданный выходной буфер возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="5b8da-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="5b8da-106">Буферы возвращаются в приложение, когда они воспроизводятся, или в результате вызова функции [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="5b8da-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="5b8da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b8da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b8da-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5b8da-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5b8da-109">Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер.</span><span class="sxs-lookup"><span data-stu-id="5b8da-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b8da-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5b8da-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5b8da-111">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5b8da-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b8da-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b8da-112">Return Value</span></span>

<span data-ttu-id="5b8da-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5b8da-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b8da-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5b8da-114">Requirements</span></span>



| <span data-ttu-id="5b8da-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5b8da-115">Requirement</span></span> | <span data-ttu-id="5b8da-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5b8da-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8da-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b8da-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8da-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b8da-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5b8da-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b8da-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8da-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b8da-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5b8da-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5b8da-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b8da-122"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b8da-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b8da-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b8da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8da-124">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="5b8da-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="5b8da-125">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="5b8da-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

