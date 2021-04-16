---
title: Сообщение MIM_OPEN (Ммсистем. h)
description: '\_При открытии входного устройства MIDI в функции обратного вызова MIDI отправляется сообщение Open.'
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414853"
---
# <a name="mim_open-message"></a><span data-ttu-id="5647c-104">\_Открытое сообщение MIM</span><span class="sxs-lookup"><span data-stu-id="5647c-104">MIM\_OPEN message</span></span>

<span data-ttu-id="5647c-105">При открытии входного устройства MIDI в функции обратного вызова MIDI отправляется сообщение **\_ Open** .</span><span class="sxs-lookup"><span data-stu-id="5647c-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="5647c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5647c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5647c-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5647c-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5647c-108">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="5647c-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="5647c-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5647c-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5647c-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="5647c-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5647c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5647c-111">Return Value</span></span>

<span data-ttu-id="5647c-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5647c-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5647c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5647c-113">Requirements</span></span>



| <span data-ttu-id="5647c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5647c-114">Requirement</span></span> | <span data-ttu-id="5647c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5647c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5647c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5647c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5647c-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5647c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5647c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5647c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5647c-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5647c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5647c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5647c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5647c-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5647c-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5647c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5647c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5647c-123">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="5647c-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5647c-124">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="5647c-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





