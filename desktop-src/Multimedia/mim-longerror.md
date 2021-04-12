---
title: Сообщение MIM_LONGERROR (Ммсистем. h)
description: '\_Сообщение ЛОНЖЕРРОР MIM отправляется в функцию обратного вызова MIDI, если получено недопустимое или неполное сообщение, исключающие MIDI.'
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- MIM_LONGERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489402"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="26d4b-104">\_Сообщение ЛОНЖЕРРОР MIM</span><span class="sxs-lookup"><span data-stu-id="26d4b-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="26d4b-105">Сообщение **\_ лонжеррор MIM** отправляется в функцию ОБРАТНОго вызова MIDI, если получено недопустимое или неполное сообщение, исключающие MIDI.</span><span class="sxs-lookup"><span data-stu-id="26d4b-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="26d4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d4b-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="26d4b-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="26d4b-108">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер, содержащий недопустимое сообщение.</span><span class="sxs-lookup"><span data-stu-id="26d4b-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="26d4b-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="26d4b-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="26d4b-110">Время получения данных драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="26d4b-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="26d4b-111">Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="26d4b-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d4b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26d4b-112">Return Value</span></span>

<span data-ttu-id="26d4b-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="26d4b-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d4b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26d4b-114">Remarks</span></span>

<span data-ttu-id="26d4b-115">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="26d4b-115">The returned buffer might not be full.</span></span> <span data-ttu-id="26d4b-116">Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , заданную параметром *лпмидихдр*.</span><span class="sxs-lookup"><span data-stu-id="26d4b-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d4b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="26d4b-117">Requirements</span></span>



| <span data-ttu-id="26d4b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="26d4b-118">Requirement</span></span> | <span data-ttu-id="26d4b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="26d4b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d4b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26d4b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26d4b-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26d4b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26d4b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26d4b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26d4b-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26d4b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26d4b-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26d4b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d4b-125"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26d4b-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d4b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26d4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d4b-127">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="26d4b-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="26d4b-128">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="26d4b-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

