---
title: Сообщение MM_MIM_CLOSE (Ммсистем. h)
description: '\_ \_ Сообщение закрытия mm MIM отправляется в окно при закрытии входного устройства MIDI.'
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- MM_MIM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988959"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="f310d-104">\_Сообщение о закрытии "mm MIM" \_</span><span class="sxs-lookup"><span data-stu-id="f310d-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="f310d-105">Сообщение **\_ \_ закрытия mm MIM** отправляется в окно при закрытии входного устройства MIDI.</span><span class="sxs-lookup"><span data-stu-id="f310d-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f310d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f310d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f310d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="f310d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="f310d-108">Обработано устройство ввода MIDI, которое было закрыто.</span><span class="sxs-lookup"><span data-stu-id="f310d-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="f310d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f310d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f310d-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="f310d-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f310d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f310d-111">Return Value</span></span>

<span data-ttu-id="f310d-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f310d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f310d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f310d-113">Remarks</span></span>

<span data-ttu-id="f310d-114">После отправки этого сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="f310d-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f310d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f310d-115">Requirements</span></span>



| <span data-ttu-id="f310d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f310d-116">Requirement</span></span> | <span data-ttu-id="f310d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f310d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f310d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f310d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f310d-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f310d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f310d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f310d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f310d-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f310d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f310d-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f310d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f310d-123"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f310d-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f310d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f310d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f310d-125">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="f310d-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="f310d-126">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="f310d-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





