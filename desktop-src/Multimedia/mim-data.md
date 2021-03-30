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
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892754"
---
# <a name="mim_data-message"></a><span data-ttu-id="d9d14-104">\_Сообщение данных MIM</span><span class="sxs-lookup"><span data-stu-id="d9d14-104">MIM\_DATA message</span></span>

<span data-ttu-id="d9d14-105">Сообщение **\_ данных MIM** отправляется в функцию обратного вызова MIDI при получении сообщения MIDI входным устройством MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="d9d14-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9d14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9d14-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="d9d14-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="d9d14-108">Полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-108">MIDI message that was received.</span></span> <span data-ttu-id="d9d14-109">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d9d14-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="d9d14-110">Требование</span><span class="sxs-lookup"><span data-stu-id="d9d14-110">Requirement</span></span> | <span data-ttu-id="d9d14-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d9d14-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="d9d14-112">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="d9d14-112">High word</span></span> | <span data-ttu-id="d9d14-113">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="d9d14-113">High-order byte</span></span> | <span data-ttu-id="d9d14-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d9d14-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="d9d14-115">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="d9d14-115">Low-order byte</span></span>  | <span data-ttu-id="d9d14-116">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="d9d14-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="d9d14-117">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="d9d14-117">Low word</span></span>  | <span data-ttu-id="d9d14-118">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="d9d14-118">High-order byte</span></span> | <span data-ttu-id="d9d14-119">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="d9d14-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="d9d14-120">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="d9d14-120">Low-order byte</span></span>  | <span data-ttu-id="d9d14-121">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="d9d14-122">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="d9d14-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="d9d14-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="d9d14-124">Время получения сообщения драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="d9d14-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="d9d14-125">Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="d9d14-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9d14-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9d14-126">Return Value</span></span>

<span data-ttu-id="d9d14-127">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d9d14-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d14-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9d14-128">Remarks</span></span>

<span data-ttu-id="d9d14-129">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="d9d14-130">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="d9d14-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d14-131">Требования</span><span class="sxs-lookup"><span data-stu-id="d9d14-131">Requirements</span></span>



| <span data-ttu-id="d9d14-132">Требование</span><span class="sxs-lookup"><span data-stu-id="d9d14-132">Requirement</span></span> | <span data-ttu-id="d9d14-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d9d14-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d14-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9d14-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d14-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9d14-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d9d14-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9d14-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d14-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9d14-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d9d14-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9d14-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9d14-139"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9d14-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d14-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9d14-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d14-141">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="d9d14-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="d9d14-142">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="d9d14-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

