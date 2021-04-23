---
title: Сообщение MM_MIM_LONGDATA (Ммсистем. h)
description: Сообщение MM \_ MIM \_ лонгдата отправляется в окно, когда получено сообщение об истечении времени ожидания системой MIDI или когда буфер заполнен данными, исключающие данные из системы.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137382"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="6f7e2-104">\_Сообщение о \_ лонгдатае mm MIM</span><span class="sxs-lookup"><span data-stu-id="6f7e2-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="6f7e2-105">Сообщение **mm \_ MIM \_ лонгдата** отправляется в окно, когда получено сообщение об истечении времени ожидания системой MIDI или когда буфер заполнен данными, исключающие данные из системы.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="6f7e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f7e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f7e2-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="6f7e2-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6f7e2-108">Обработчик для входного устройства MIDI, получившего данные.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e2-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="6f7e2-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="6f7e2-110">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую буфер.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f7e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f7e2-111">Return Value</span></span>

<span data-ttu-id="6f7e2-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f7e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f7e2-113">Remarks</span></span>

<span data-ttu-id="6f7e2-114">Возвращенный буфер может быть незаполненным.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-114">The returned buffer might not be full.</span></span> <span data-ttu-id="6f7e2-115">Чтобы определить число байтов, записанных в возвращенный буфер, используйте элемент **двбитесрекордед** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , на который указывает *лпмидихдр*.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="6f7e2-116">Нет отметки времени, доступной для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-116">No time stamp is available with this message.</span></span> <span data-ttu-id="6f7e2-117">Для входных данных с отметкой времени необходимо использовать сообщения, отправленные в функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6f7e2-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7e2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6f7e2-118">Requirements</span></span>



| <span data-ttu-id="6f7e2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6f7e2-119">Requirement</span></span> | <span data-ttu-id="6f7e2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6f7e2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7e2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f7e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7e2-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f7e2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6f7e2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f7e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7e2-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6f7e2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f7e2-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6f7e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f7e2-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e2-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f7e2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f7e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7e2-128">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="6f7e2-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6f7e2-129">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="6f7e2-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

