---
title: Сообщение MM_MIM_ERROR (Ммсистем. h)
description: '\_ \_ При получении недопустимого сообщения MIDI в окно отправляется сообщение об ошибке в MIM.'
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135267"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="018ec-104">ММ \_ — \_ сообщение об ошибке MIM</span><span class="sxs-lookup"><span data-stu-id="018ec-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="018ec-105">При получении недопустимого сообщения MIDI в окно отправляется сообщение **\_ \_ об ошибке в MIM** .</span><span class="sxs-lookup"><span data-stu-id="018ec-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="018ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="018ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="018ec-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="018ec-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="018ec-108">Обрабатывает входное устройство MIDI, которое получило недопустимое сообщение.</span><span class="sxs-lookup"><span data-stu-id="018ec-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="018ec-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*лмидимессаже*</span><span class="sxs-lookup"><span data-stu-id="018ec-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="018ec-110">Недопустимое сообщение MIDI.</span><span class="sxs-lookup"><span data-stu-id="018ec-110">Invalid MIDI message.</span></span> <span data-ttu-id="018ec-111">Сообщение упаковывается в значение **DWORD** с первым байтом сообщения в байте нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="018ec-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="018ec-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="018ec-112">Return Value</span></span>

<span data-ttu-id="018ec-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="018ec-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="018ec-114">Требования</span><span class="sxs-lookup"><span data-stu-id="018ec-114">Requirements</span></span>



| <span data-ttu-id="018ec-115">Требование</span><span class="sxs-lookup"><span data-stu-id="018ec-115">Requirement</span></span> | <span data-ttu-id="018ec-116">Значение</span><span class="sxs-lookup"><span data-stu-id="018ec-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="018ec-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="018ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="018ec-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="018ec-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="018ec-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="018ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="018ec-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="018ec-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="018ec-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="018ec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="018ec-122"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="018ec-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="018ec-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="018ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018ec-124">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="018ec-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="018ec-125">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="018ec-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





