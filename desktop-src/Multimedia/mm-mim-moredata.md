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
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071597"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="4c698-104">\_Сообщение о \_ MOREDATAе mm MIM</span><span class="sxs-lookup"><span data-stu-id="4c698-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="4c698-105">Сообщение **mm \_ MIM \_ MOREDATA** отправляется в окно обратного вызова, когда устройство ввода MIDI получает сообщение MIDI, но приложение не обрабатывает сообщения [**\_ данных MIM**](mim-data.md) достаточно быстро, чтобы не допустить входного драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="4c698-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="4c698-106">Окно получает это сообщение, только если приложение указывает \_ состояние ввода-вывода MIDI \_ в вызове функции [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="4c698-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="4c698-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c698-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c698-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="4c698-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4c698-109">Обработчик на устройстве ввода MIDI, которое получило сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="4c698-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="4c698-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="4c698-111">Указывает полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="4c698-112">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c698-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="4c698-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4c698-113">Requirement</span></span> | <span data-ttu-id="4c698-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4c698-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="4c698-115">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="4c698-115">High word</span></span> | <span data-ttu-id="4c698-116">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="4c698-116">High-order byte</span></span> | <span data-ttu-id="4c698-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4c698-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="4c698-118">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="4c698-118">Low-order byte</span></span>  | <span data-ttu-id="4c698-119">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="4c698-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="4c698-120">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="4c698-120">Low word</span></span>  | <span data-ttu-id="4c698-121">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="4c698-121">High-order byte</span></span> | <span data-ttu-id="4c698-122">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="4c698-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="4c698-123">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="4c698-123">Low-order byte</span></span>  | <span data-ttu-id="4c698-124">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="4c698-125">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c698-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c698-126">Return Value</span></span>

<span data-ttu-id="4c698-127">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4c698-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c698-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c698-128">Remarks</span></span>

<span data-ttu-id="4c698-129">Если приложение будет отправлять данные MIDI быстрее, чем оно может обработать, не следует использовать механизм обратного вызова окна.</span><span class="sxs-lookup"><span data-stu-id="4c698-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="4c698-130">Чтобы добиться максимальной скорости, используйте функцию обратного вызова и используйте [**сообщение \_ MOREDATA MIM**](mim-moredata.md) вместо mm \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="4c698-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="4c698-131">Приложение должно выполнять только минимальный объем обработки \_ сообщений mm MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="4c698-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="4c698-132">(В частности, приложения не должны вызывать функцию [посообщений](/windows/win32/api/winuser/nf-winuser-postmessagea) при обработке mm \_ MIM \_ MOREDATA.) Вместо этого приложение должно поместить данные события в буфер, а затем вернуть.</span><span class="sxs-lookup"><span data-stu-id="4c698-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="4c698-133">Когда приложение получает сообщение [**\_ \_ данных типа mm MIM**](mm-mim-data.md) после ряда MOREDATA сообщений размером mm \_ MIM \_ , оно было перехвачено с входящими событиями MIDI и может безопасно вызывать функции, потребляющие много времени.</span><span class="sxs-lookup"><span data-stu-id="4c698-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="4c698-134">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="4c698-135">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="4c698-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="4c698-136">Нет отметки времени, доступной для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4c698-136">No time stamp is available with this message.</span></span> <span data-ttu-id="4c698-137">Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="4c698-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c698-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4c698-138">Requirements</span></span>



| <span data-ttu-id="4c698-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4c698-139">Requirement</span></span> | <span data-ttu-id="4c698-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4c698-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c698-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c698-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4c698-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c698-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4c698-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c698-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4c698-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c698-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4c698-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4c698-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c698-146"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c698-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c698-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c698-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c698-148">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4c698-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4c698-149">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="4c698-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

