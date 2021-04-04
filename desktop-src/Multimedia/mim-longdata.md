---
title: Сообщение MIM_LONGDATA (Ммсистем. h)
description: '\_Сообщение ЛОНГДАТА MIM отправляется в функцию обратного вызова MIDI, когда системный буфер заполняется данными и возвращается приложению.'
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137798"
---
# <a name="mim_longdata-message"></a><span data-ttu-id="336a0-104">\_Сообщение ЛОНГДАТА MIM</span><span class="sxs-lookup"><span data-stu-id="336a0-104">MIM\_LONGDATA message</span></span>

<span data-ttu-id="336a0-105">Сообщение **\_ лонгдата MIM** отправляется в функцию ОБРАТНОго вызова MIDI, когда системный буфер заполняется данными и возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="336a0-105">The **MIM\_LONGDATA** message is sent to a MIDI input callback function when a system-exclusive buffer has been filled with data and is being returned to the application.</span></span>


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="336a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="336a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="336a0-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="336a0-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="336a0-108">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую входной буфер.</span><span class="sxs-lookup"><span data-stu-id="336a0-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="336a0-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*двтиместамп*</span><span class="sxs-lookup"><span data-stu-id="336a0-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="336a0-110">Время получения данных драйвером устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="336a0-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="336a0-111">Метка времени указывается в миллисекундах, начиная с нуля, когда была вызвана функция [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="336a0-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="336a0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="336a0-112">Return Value</span></span>

<span data-ttu-id="336a0-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="336a0-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="336a0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="336a0-114">Remarks</span></span>

<span data-ttu-id="336a0-115">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="336a0-115">The returned buffer might not be full.</span></span> <span data-ttu-id="336a0-116">Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , заданную параметром *лпмидихдр*.</span><span class="sxs-lookup"><span data-stu-id="336a0-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="336a0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="336a0-117">Requirements</span></span>



| <span data-ttu-id="336a0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="336a0-118">Requirement</span></span> | <span data-ttu-id="336a0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="336a0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="336a0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="336a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="336a0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="336a0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="336a0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="336a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="336a0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="336a0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="336a0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="336a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="336a0-125"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="336a0-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="336a0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="336a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336a0-127">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="336a0-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="336a0-128">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="336a0-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

