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
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804097"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="fa905-104">\_Сообщение MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="fa905-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="fa905-105">Сообщение **\_ MOREDATA MIM** отправляется в функцию ОБРАТНОго вызова MIDI, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает сообщения [**\_ данных MIM**](mim-data.md) достаточно быстро, чтобы не допустить входного драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="fa905-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="fa905-106">Функция обратного вызова получает это сообщение, только если приложение указывает \_ состояние ввода-вывода MIDI \_ в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="fa905-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="fa905-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa905-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa905-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*двмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="fa905-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="fa905-109">Указывает полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="fa905-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="fa905-110">Сообщение упаковывается в значение **DWORD** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fa905-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="fa905-111">Требование</span><span class="sxs-lookup"><span data-stu-id="fa905-111">Requirement</span></span> | <span data-ttu-id="fa905-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fa905-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="fa905-113">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="fa905-113">High word</span></span> | <span data-ttu-id="fa905-114">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="fa905-114">High-order byte</span></span> | <span data-ttu-id="fa905-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fa905-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="fa905-116">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="fa905-116">Low-order byte</span></span>  | <span data-ttu-id="fa905-117">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="fa905-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="fa905-118">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="fa905-118">Low word</span></span>  | <span data-ttu-id="fa905-119">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="fa905-119">High-order byte</span></span> | <span data-ttu-id="fa905-120">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="fa905-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="fa905-121">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="fa905-121">Low-order byte</span></span>  | <span data-ttu-id="fa905-122">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="fa905-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="fa905-123">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="fa905-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="fa905-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="fa905-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="fa905-125">Указывает время получения сообщения драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="fa905-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="fa905-126">Метка времени указывается в миллисекундах, начиная с 0 при вызове функции [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="fa905-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa905-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa905-127">Return Value</span></span>

<span data-ttu-id="fa905-128">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fa905-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa905-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa905-129">Remarks</span></span>

<span data-ttu-id="fa905-130">Приложение должно выполнять только минимальный объем обработки \_ сообщений MOREDATA MIM.</span><span class="sxs-lookup"><span data-stu-id="fa905-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="fa905-131">(В частности, приложения не должны вызывать функцию [посообщений](/windows/win32/api/winuser/nf-winuser-postmessagea) при обработке MIM \_ . MOREDATA.) Вместо этого приложение должно поместить данные события в буфер, а затем вернуть.</span><span class="sxs-lookup"><span data-stu-id="fa905-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="fa905-132">Когда приложение получает сообщение [**\_ данных MIM**](mim-data.md) после ряда \_ сообщений MOREDATA MIM, оно захватывается входящими событиями MIDI и может безопасно вызывать функции, требующие много времени.</span><span class="sxs-lookup"><span data-stu-id="fa905-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="fa905-133">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="fa905-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="fa905-134">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="fa905-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa905-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fa905-135">Requirements</span></span>



| <span data-ttu-id="fa905-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fa905-136">Requirement</span></span> | <span data-ttu-id="fa905-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fa905-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa905-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa905-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fa905-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa905-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa905-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa905-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fa905-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa905-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa905-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fa905-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa905-143"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa905-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa905-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa905-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa905-145">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="fa905-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="fa905-146">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="fa905-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

