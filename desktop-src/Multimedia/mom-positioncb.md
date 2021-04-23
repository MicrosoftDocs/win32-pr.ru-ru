---
title: Сообщение MOM_POSITIONCB (Ммсистем. h)
description: Сообщение о \_ должности MOM отправляется при \_ \_ достижении события обратного вызова мевт F в потоке вывода MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803665"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="ac12a-104">\_Сообщение MOM поситионкб</span><span class="sxs-lookup"><span data-stu-id="ac12a-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="ac12a-105">Сообщение **о \_ должности MOM** отправляется при достижении события **\_ \_ обратного вызова МЕВТ F** в потоке вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="ac12a-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac12a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac12a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac12a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ac12a-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ac12a-108">Указатель на структуру [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , определяющую входной буфер.</span><span class="sxs-lookup"><span data-stu-id="ac12a-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ac12a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ac12a-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ac12a-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ac12a-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac12a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac12a-111">Return Value</span></span>

<span data-ttu-id="ac12a-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac12a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac12a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac12a-113">Remarks</span></span>

<span data-ttu-id="ac12a-114">Воспроизведение буфера потока сохраняется даже во время выполнения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ac12a-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="ac12a-115">Все события после события **\_ \_ обратного вызова мевт F** в буфере будут планироваться и отправляться вовремя независимо от того, сколько времени тратится на функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ac12a-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="ac12a-116">Если обратные вызовы размещения создаются быстрее, чем приложение может их обработать, элемент **двоффсет** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) может ссылаться на событие, которое еще не обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="ac12a-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac12a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ac12a-117">Requirements</span></span>



| <span data-ttu-id="ac12a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ac12a-118">Requirement</span></span> | <span data-ttu-id="ac12a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ac12a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac12a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac12a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac12a-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac12a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac12a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac12a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac12a-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac12a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac12a-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ac12a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac12a-125"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac12a-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac12a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac12a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac12a-127">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="ac12a-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

