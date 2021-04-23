---
title: Сообщение MM_MIM_LONGERROR (Ммсистем. h)
description: Сообщение MM \_ MIM \_ лонжеррор отправляется в окно, когда получено недопустимое или неполное сообщение, исключающие MIDI.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- MM_MIM_LONGERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682052"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="8fe7d-104">\_Сообщение о \_ лонжерроре mm MIM</span><span class="sxs-lookup"><span data-stu-id="8fe7d-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="8fe7d-105">Сообщение **mm \_ MIM \_ лонжеррор** отправляется в окно, когда получено недопустимое или неполное сообщение, исключающие MIDI.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="8fe7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fe7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe7d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="8fe7d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="8fe7d-108">Обрабатывает входное устройство MIDI, которое получило недопустимое сообщение.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="8fe7d-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="8fe7d-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="8fe7d-110">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер, содержащий недопустимое сообщение.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fe7d-111">Return Value</span></span>

<span data-ttu-id="8fe7d-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fe7d-113">Remarks</span></span>

<span data-ttu-id="8fe7d-114">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-114">The returned buffer might not be full.</span></span> <span data-ttu-id="8fe7d-115">Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , заданную параметром *лпмидихдр*.</span><span class="sxs-lookup"><span data-stu-id="8fe7d-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe7d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8fe7d-116">Requirements</span></span>



| <span data-ttu-id="8fe7d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8fe7d-117">Requirement</span></span> | <span data-ttu-id="8fe7d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe7d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe7d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fe7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe7d-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8fe7d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8fe7d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fe7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe7d-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8fe7d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8fe7d-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8fe7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe7d-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fe7d-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe7d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fe7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe7d-126">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="8fe7d-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="8fe7d-127">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="8fe7d-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

