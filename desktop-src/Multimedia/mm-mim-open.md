---
title: Сообщение MM_MIM_OPEN (Ммсистем. h)
description: '\_ \_ При открытии входного устройства MIDI в окне будет отправлено сообщение с открытым параметром mm MIM.'
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891393"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="76595-104">\_ \_ Открытое сообщение для MIM</span><span class="sxs-lookup"><span data-stu-id="76595-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="76595-105">При открытии входного устройства MIDI в окне будет отправлено сообщение с **\_ \_ открытым параметром mm MIM** .</span><span class="sxs-lookup"><span data-stu-id="76595-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="76595-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76595-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*хинпут*</span><span class="sxs-lookup"><span data-stu-id="76595-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="76595-108">Обработано открытое устройство ввода MIDI.</span><span class="sxs-lookup"><span data-stu-id="76595-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="76595-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="76595-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="76595-110">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="76595-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76595-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76595-111">Return Value</span></span>

<span data-ttu-id="76595-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76595-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76595-113">Требования</span><span class="sxs-lookup"><span data-stu-id="76595-113">Requirements</span></span>



| <span data-ttu-id="76595-114">Требование</span><span class="sxs-lookup"><span data-stu-id="76595-114">Requirement</span></span> | <span data-ttu-id="76595-115">Значение</span><span class="sxs-lookup"><span data-stu-id="76595-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76595-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76595-116">Minimum supported client</span></span><br/> | <span data-ttu-id="76595-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76595-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="76595-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76595-118">Minimum supported server</span></span><br/> | <span data-ttu-id="76595-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76595-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="76595-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="76595-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="76595-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76595-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76595-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76595-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76595-123">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="76595-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="76595-124">Сообщения MIDI</span><span class="sxs-lookup"><span data-stu-id="76595-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





