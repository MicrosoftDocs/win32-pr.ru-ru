---
title: Сообщение MM_MIM_DATA (Ммсистем. h)
description: Сообщение с данными типа "MM \_ MIM" \_ отправляется в окно, когда устройство ввода MIDI получает полное сообщение MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119699"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="38900-104">\_Сообщение данных MIM (мм) \_</span><span class="sxs-lookup"><span data-stu-id="38900-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="38900-105">Сообщение **с \_ \_ данными типа "mm MIM** " отправляется в окно, когда устройство ввода MIDI получает полное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="38900-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38900-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="38900-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="38900-108">Обработчик на устройстве ввода MIDI, которое получило сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="38900-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="38900-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="38900-110">Полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-110">MIDI message that was received.</span></span> <span data-ttu-id="38900-111">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="38900-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="38900-112">Требование</span><span class="sxs-lookup"><span data-stu-id="38900-112">Requirement</span></span> | <span data-ttu-id="38900-113">Значение</span><span class="sxs-lookup"><span data-stu-id="38900-113">Value</span></span> | <span data-ttu-id="38900-114">Описание</span><span class="sxs-lookup"><span data-stu-id="38900-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="38900-115">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="38900-115">High word</span></span> | <span data-ttu-id="38900-116">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="38900-116">High-order byte</span></span> | <span data-ttu-id="38900-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38900-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="38900-118">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="38900-118">Low-order byte</span></span>  | <span data-ttu-id="38900-119">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="38900-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="38900-120">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="38900-120">Low word</span></span>  | <span data-ttu-id="38900-121">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="38900-121">High-order byte</span></span> | <span data-ttu-id="38900-122">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="38900-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="38900-123">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="38900-123">Low-order byte</span></span>  | <span data-ttu-id="38900-124">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="38900-125">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38900-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38900-126">Return Value</span></span>

<span data-ttu-id="38900-127">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="38900-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38900-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="38900-128">Remarks</span></span>

<span data-ttu-id="38900-129">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="38900-130">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="38900-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="38900-131">Нет отметки времени, доступной для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="38900-131">No time stamp is available with this message.</span></span> <span data-ttu-id="38900-132">Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="38900-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="38900-133">Требования</span><span class="sxs-lookup"><span data-stu-id="38900-133">Requirements</span></span>



| <span data-ttu-id="38900-134">Требование</span><span class="sxs-lookup"><span data-stu-id="38900-134">Requirement</span></span> | <span data-ttu-id="38900-135">Значение</span><span class="sxs-lookup"><span data-stu-id="38900-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38900-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38900-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38900-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38900-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38900-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38900-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38900-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38900-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38900-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38900-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38900-141"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38900-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38900-142">См. также</span><span class="sxs-lookup"><span data-stu-id="38900-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38900-143">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="38900-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="38900-144">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="38900-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





