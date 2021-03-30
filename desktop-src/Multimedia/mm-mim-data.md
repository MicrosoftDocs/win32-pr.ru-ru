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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071229"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="f1255-104">\_Сообщение данных MIM (мм) \_</span><span class="sxs-lookup"><span data-stu-id="f1255-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="f1255-105">Сообщение **с \_ \_ данными типа "mm MIM** " отправляется в окно, когда устройство ввода MIDI получает полное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="f1255-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1255-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1255-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="f1255-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="f1255-108">Обработчик на устройстве ввода MIDI, которое получило сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="f1255-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="f1255-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="f1255-110">Полученное сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-110">MIDI message that was received.</span></span> <span data-ttu-id="f1255-111">Сообщение упаковывается в значение даублеворд следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1255-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="f1255-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f1255-112">Requirement</span></span> | <span data-ttu-id="f1255-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f1255-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="f1255-114">Высокое слово</span><span class="sxs-lookup"><span data-stu-id="f1255-114">High word</span></span> | <span data-ttu-id="f1255-115">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="f1255-115">High-order byte</span></span> | <span data-ttu-id="f1255-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f1255-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="f1255-117">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="f1255-117">Low-order byte</span></span>  | <span data-ttu-id="f1255-118">Содержит второй байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="f1255-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="f1255-119">Низкое слово</span><span class="sxs-lookup"><span data-stu-id="f1255-119">Low word</span></span>  | <span data-ttu-id="f1255-120">Байт высокого порядка</span><span class="sxs-lookup"><span data-stu-id="f1255-120">High-order byte</span></span> | <span data-ttu-id="f1255-121">Содержит первый байт данных MIDI (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="f1255-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="f1255-122">Байт низкого порядка</span><span class="sxs-lookup"><span data-stu-id="f1255-122">Low-order byte</span></span>  | <span data-ttu-id="f1255-123">Содержит состояние MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="f1255-124">Два байта данных MIDI являются необязательными в зависимости от байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1255-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1255-125">Return Value</span></span>

<span data-ttu-id="f1255-126">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f1255-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1255-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1255-127">Remarks</span></span>

<span data-ttu-id="f1255-128">Сообщения MIDI, полученные с порта ввода MIDI, имеют состояние "отключено". Каждое сообщение разворачивается для включения байта состояния MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="f1255-129">Это сообщение не отправляется, когда получено сообщение, исключающая систему MIDI.</span><span class="sxs-lookup"><span data-stu-id="f1255-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="f1255-130">Нет отметки времени, доступной для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1255-130">No time stamp is available with this message.</span></span> <span data-ttu-id="f1255-131">Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f1255-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1255-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f1255-132">Requirements</span></span>



| <span data-ttu-id="f1255-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f1255-133">Requirement</span></span> | <span data-ttu-id="f1255-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f1255-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1255-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1255-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f1255-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1255-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1255-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1255-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f1255-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1255-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1255-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f1255-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1255-140"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1255-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1255-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1255-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1255-142">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="f1255-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="f1255-143">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="f1255-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





