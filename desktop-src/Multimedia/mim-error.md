---
title: Сообщение MIM_ERROR (Ммсистем. h)
description: '\_Сообщение об ошибке MIM отправляется в функцию обратного вызова MIDI, когда получено недопустимое сообщение MIDI.'
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135278"
---
# <a name="mim_error-message"></a><span data-ttu-id="8c9a7-104">\_Сообщение об ошибке MIM</span><span class="sxs-lookup"><span data-stu-id="8c9a7-104">MIM\_ERROR message</span></span>

<span data-ttu-id="8c9a7-105">Сообщение **\_ об ошибке MIM** отправляется в функцию ОБРАТНОго вызова MIDI, когда получено недопустимое сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="8c9a7-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="8c9a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c9a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9a7-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="8c9a7-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="8c9a7-108">Получено недопустимое сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="8c9a7-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="8c9a7-109">Сообщение упаковывается в значение даублеворд с первым байтом сообщения в байте нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="8c9a7-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="8c9a7-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="8c9a7-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="8c9a7-111">Время получения сообщения драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="8c9a7-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="8c9a7-112">Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="8c9a7-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9a7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c9a7-113">Return Value</span></span>

<span data-ttu-id="8c9a7-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8c9a7-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9a7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8c9a7-115">Requirements</span></span>



| <span data-ttu-id="8c9a7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8c9a7-116">Requirement</span></span> | <span data-ttu-id="8c9a7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8c9a7-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9a7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c9a7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9a7-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c9a7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c9a7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c9a7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9a7-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c9a7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c9a7-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8c9a7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9a7-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c9a7-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9a7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c9a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9a7-125">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="8c9a7-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8c9a7-126">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="8c9a7-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

