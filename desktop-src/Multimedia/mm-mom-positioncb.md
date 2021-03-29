---
title: Сообщение MM_MOM_POSITIONCB (Ммсистем. h)
description: '\_ \_ При \_ \_ достижении события обратного вызова мевт F в потоке вывода MIDI в окно отправляется сообщение поситионкб MOM.'
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988258"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="ec1bb-104">\_ \_ Сообщение поситионкб MOM</span><span class="sxs-lookup"><span data-stu-id="ec1bb-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="ec1bb-105">При **\_ \_** \_ \_ достижении события обратного вызова МЕВТ F в потоке вывода MIDI в окно отправляется сообщение поситионкб MOM.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ec1bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec1bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1bb-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*лпмидихдр*</span><span class="sxs-lookup"><span data-stu-id="ec1bb-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="ec1bb-108">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , которая идентифицирует событие, вызвавшее обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="ec1bb-109">Элемент **двоффсет** дает смещение события.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="ec1bb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec1bb-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ec1bb-111">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec1bb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec1bb-112">Return Value</span></span>

<span data-ttu-id="ec1bb-113">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1bb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec1bb-114">Remarks</span></span>

<span data-ttu-id="ec1bb-115">Воспроизведение буфера потока сохраняется даже во время выполнения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="ec1bb-116">Все события после \_ \_ события обратного вызова мевт F в буфере будут планироваться и отправляться вовремя независимо от того, сколько времени тратится на функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="ec1bb-117">Если обратные вызовы размещения создаются быстрее, чем приложение может их обработать, элемент **двоффсет** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) может ссылаться на событие, которое еще не обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="ec1bb-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ec1bb-118">Requirements</span></span>



| <span data-ttu-id="ec1bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ec1bb-119">Requirement</span></span> | <span data-ttu-id="ec1bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ec1bb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1bb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec1bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1bb-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec1bb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ec1bb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec1bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1bb-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec1bb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec1bb-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ec1bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec1bb-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec1bb-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec1bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec1bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1bb-128">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="ec1bb-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

