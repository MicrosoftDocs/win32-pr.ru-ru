---
title: Сообщение MIM_CLOSE (Ммсистем. h)
description: Сообщение о \_ закрытии MIM отправляется в функцию обратного вызова MIDI при закрытии входного устройства MIDI.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533794"
---
# <a name="mim_close-message"></a><span data-ttu-id="cf574-104">\_Сообщение о закрытии MIM</span><span class="sxs-lookup"><span data-stu-id="cf574-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="cf574-105">Сообщение **о \_ закрытии MIM** отправляется в функцию обратного вызова MIDI при закрытии входного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="cf574-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="cf574-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf574-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="cf574-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cf574-108">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="cf574-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="cf574-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="cf574-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cf574-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="cf574-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf574-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf574-111">Return Value</span></span>

<span data-ttu-id="cf574-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cf574-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf574-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf574-113">Remarks</span></span>

<span data-ttu-id="cf574-114">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="cf574-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf574-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cf574-115">Requirements</span></span>



| <span data-ttu-id="cf574-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cf574-116">Requirement</span></span> | <span data-ttu-id="cf574-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf574-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf574-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf574-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf574-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf574-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cf574-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf574-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf574-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf574-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cf574-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf574-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf574-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf574-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf574-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf574-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf574-125">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="cf574-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="cf574-126">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="cf574-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





