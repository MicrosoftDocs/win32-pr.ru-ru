---
title: Сообщение MIM_DATA (Ммсистем. h)
description: '\_Сообщение данных MIM отправляется в функцию обратного вызова MIDI при получении сообщения MIDI входным устройством MIDI.'
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118409"
---
# <a name="mim_data-message"></a><span data-ttu-id="cd743-104">\_Сообщение данных MIM</span><span class="sxs-lookup"><span data-stu-id="cd743-104">MIM\_DATA message</span></span>

<span data-ttu-id="cd743-105">Сообщение **\_ данных MIM** отправляется в функцию обратного вызова MIDI при получении сообщения MIDI входным устройством MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="cd743-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd743-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="cd743-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="cd743-108">Полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-108">MIDI message that was received.</span></span> <span data-ttu-id="cd743-109">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd743-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="cd743-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cd743-110">Requirement</span></span> | <span data-ttu-id="cd743-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cd743-111">Value</span></span> | <span data-ttu-id="cd743-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cd743-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="cd743-113">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="cd743-113">High word</span></span> | <span data-ttu-id="cd743-114">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="cd743-114">High-order byte</span></span> | <span data-ttu-id="cd743-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cd743-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="cd743-116">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="cd743-116">Low-order byte</span></span>  | <span data-ttu-id="cd743-117">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="cd743-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="cd743-118">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="cd743-118">Low word</span></span>  | <span data-ttu-id="cd743-119">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="cd743-119">High-order byte</span></span> | <span data-ttu-id="cd743-120">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="cd743-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="cd743-121">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="cd743-121">Low-order byte</span></span>  | <span data-ttu-id="cd743-122">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="cd743-123">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="cd743-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="cd743-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="cd743-125">Время получения сообщения драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="cd743-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="cd743-126">Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="cd743-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd743-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd743-127">Return Value</span></span>

<span data-ttu-id="cd743-128">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cd743-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd743-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="cd743-129">Remarks</span></span>

<span data-ttu-id="cd743-130">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="cd743-131">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="cd743-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd743-132">Требования</span><span class="sxs-lookup"><span data-stu-id="cd743-132">Requirements</span></span>



| <span data-ttu-id="cd743-133">Требование</span><span class="sxs-lookup"><span data-stu-id="cd743-133">Requirement</span></span> | <span data-ttu-id="cd743-134">Значение</span><span class="sxs-lookup"><span data-stu-id="cd743-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd743-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd743-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cd743-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd743-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd743-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd743-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cd743-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd743-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd743-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cd743-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd743-140"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd743-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd743-141">См. также</span><span class="sxs-lookup"><span data-stu-id="cd743-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd743-142">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="cd743-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="cd743-143">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="cd743-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

