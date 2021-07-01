---
title: Сообщение MIM_MOREDATA (Ммсистем. h)
description: '\_Сообщение MOREDATA MIM отправляется в функцию обратного вызова MIDI, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает \_ сообщения данных MIM достаточно быстро, чтобы не допустить входного драйвера устройства.'
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119410"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="c4ec4-104">\_Сообщение MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="c4ec4-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="c4ec4-105">Сообщение **\_ MOREDATA MIM** отправляется в функцию ОБРАТНОго вызова MIDI, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает сообщения [**\_ данных MIM**](mim-data.md) достаточно быстро, чтобы не допустить входного драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="c4ec4-106">Функция обратного вызова получает это сообщение, только если приложение указывает \_ состояние ввода-вывода MIDI \_ в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="c4ec4-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="c4ec4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4ec4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ec4-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="c4ec4-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="c4ec4-109">Указывает полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="c4ec4-110">Сообщение упаковывается в значение **DWORD** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c4ec4-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="c4ec4-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c4ec4-111">Requirement</span></span> | <span data-ttu-id="c4ec4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c4ec4-112">Value</span></span> | <span data-ttu-id="c4ec4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c4ec4-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="c4ec4-114">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="c4ec4-114">High word</span></span> | <span data-ttu-id="c4ec4-115">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="c4ec4-115">High-order byte</span></span> | <span data-ttu-id="c4ec4-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="c4ec4-117">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="c4ec4-117">Low-order byte</span></span>  | <span data-ttu-id="c4ec4-118">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="c4ec4-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="c4ec4-119">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="c4ec4-119">Low word</span></span>  | <span data-ttu-id="c4ec4-120">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="c4ec4-120">High-order byte</span></span> | <span data-ttu-id="c4ec4-121">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="c4ec4-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="c4ec4-122">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="c4ec4-122">Low-order byte</span></span>  | <span data-ttu-id="c4ec4-123">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="c4ec4-124">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="c4ec4-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="c4ec4-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="c4ec4-126">Указывает время получения сообщения драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="c4ec4-127">Метка времени указывается в миллисекундах, начиная с 0 при вызове функции [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="c4ec4-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ec4-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4ec4-128">Return Value</span></span>

<span data-ttu-id="c4ec4-129">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ec4-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="c4ec4-130">Remarks</span></span>

<span data-ttu-id="c4ec4-131">Приложение должно выполнять только минимальный объем обработки \_ сообщений MOREDATA MIM.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="c4ec4-132">(В частности, приложения не должны вызывать функцию [посообщений](/windows/win32/api/winuser/nf-winuser-postmessagea) при обработке MIM \_ . MOREDATA.) Вместо этого приложение должно поместить данные события в буфер, а затем вернуть.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="c4ec4-133">Когда приложение получает сообщение [**\_ данных MIM**](mim-data.md) после ряда \_ сообщений MOREDATA MIM, оно захватывается входящими событиями MIDI и может безопасно вызывать функции, требующие много времени.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="c4ec4-134">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="c4ec4-135">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="c4ec4-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ec4-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c4ec4-136">Requirements</span></span>



| <span data-ttu-id="c4ec4-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c4ec4-137">Requirement</span></span> | <span data-ttu-id="c4ec4-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c4ec4-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ec4-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4ec4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ec4-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4ec4-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4ec4-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4ec4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ec4-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4ec4-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4ec4-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c4ec4-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ec4-144"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4ec4-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ec4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="c4ec4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ec4-146">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="c4ec4-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="c4ec4-147">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="c4ec4-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

