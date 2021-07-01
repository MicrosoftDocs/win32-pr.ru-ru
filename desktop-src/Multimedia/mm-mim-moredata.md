---
title: Сообщение MM_MIM_MOREDATA (Ммсистем. h)
description: Сообщение MM \_ MIM \_ MOREDATA отправляется в окно обратного вызова, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает \_ сообщения данных MIM достаточно быстро, чтобы не допустить входного драйвера устройства.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120029"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="758e4-104">\_Сообщение о \_ MOREDATAе mm MIM</span><span class="sxs-lookup"><span data-stu-id="758e4-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="758e4-105">Сообщение **mm \_ MIM \_ MOREDATA** отправляется в окно обратного вызова, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает сообщения [**\_ данных MIM**](mim-data.md) достаточно быстро, чтобы не допустить входного драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="758e4-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="758e4-106">Окно получает это сообщение, только если приложение указывает \_ состояние ввода-вывода MIDI \_ в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="758e4-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="758e4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="758e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="758e4-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="758e4-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="758e4-109">Обработчик на устройстве ввода MIDI, которое получило сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="758e4-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="758e4-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="758e4-111">Указывает полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="758e4-112">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="758e4-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="758e4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="758e4-113">Requirement</span></span> | <span data-ttu-id="758e4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="758e4-114">Value</span></span> | <span data-ttu-id="758e4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="758e4-115">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="758e4-116">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="758e4-116">High word</span></span> | <span data-ttu-id="758e4-117">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="758e4-117">High-order byte</span></span> | <span data-ttu-id="758e4-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="758e4-118">Not used.</span></span>                                           |
|           | <span data-ttu-id="758e4-119">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="758e4-119">Low-order byte</span></span>  | <span data-ttu-id="758e4-120">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="758e4-120">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="758e4-121">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="758e4-121">Low word</span></span>  | <span data-ttu-id="758e4-122">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="758e4-122">High-order byte</span></span> | <span data-ttu-id="758e4-123">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="758e4-123">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="758e4-124">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="758e4-124">Low-order byte</span></span>  | <span data-ttu-id="758e4-125">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-125">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="758e4-126">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-126">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="758e4-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="758e4-127">Return Value</span></span>

<span data-ttu-id="758e4-128">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="758e4-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="758e4-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="758e4-129">Remarks</span></span>

<span data-ttu-id="758e4-130">Если приложение будет отправлять данные MIDI быстрее, чем оно может обработать, не следует использовать механизм обратного вызова окна.</span><span class="sxs-lookup"><span data-stu-id="758e4-130">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="758e4-131">Чтобы добиться максимальной скорости, используйте функцию обратного вызова и используйте [**сообщение \_ MOREDATA MIM**](mim-moredata.md) вместо mm \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="758e4-131">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="758e4-132">Приложение должно выполнять только минимальный объем обработки \_ сообщений mm MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="758e4-132">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="758e4-133">(В частности, приложения не должны вызывать функцию [посообщений](/windows/win32/api/winuser/nf-winuser-postmessagea) при обработке mm \_ MIM \_ MOREDATA.) Вместо этого приложение должно поместить данные события в буфер, а затем вернуть.</span><span class="sxs-lookup"><span data-stu-id="758e4-133">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="758e4-134">Когда приложение получает сообщение [**\_ \_ данных типа mm MIM**](mm-mim-data.md) после ряда MOREDATA сообщений размером mm \_ MIM \_ , оно было перехвачено с входящими событиями MIDI и может безопасно вызывать функции, потребляющие много времени.</span><span class="sxs-lookup"><span data-stu-id="758e4-134">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="758e4-135">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-135">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="758e4-136">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="758e4-136">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="758e4-137">Нет отметки времени, доступной для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="758e4-137">No time stamp is available with this message.</span></span> <span data-ttu-id="758e4-138">Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="758e4-138">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="758e4-139">Требования</span><span class="sxs-lookup"><span data-stu-id="758e4-139">Requirements</span></span>



| <span data-ttu-id="758e4-140">Требование</span><span class="sxs-lookup"><span data-stu-id="758e4-140">Requirement</span></span> | <span data-ttu-id="758e4-141">Значение</span><span class="sxs-lookup"><span data-stu-id="758e4-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758e4-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="758e4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="758e4-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="758e4-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="758e4-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="758e4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="758e4-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="758e4-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="758e4-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="758e4-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="758e4-147"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="758e4-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="758e4-148">См. также</span><span class="sxs-lookup"><span data-stu-id="758e4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758e4-149">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="758e4-149">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="758e4-150">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="758e4-150">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

