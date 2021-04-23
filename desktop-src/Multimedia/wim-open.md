---
title: Сообщение WIM_OPEN (Ммсистем. h)
description: '\_При открытии входного устройства с звуковой звукозаписью сообщение о открытом формате WIM отправляется в функцию обратного вызова звукового сигнала звуковой волны.'
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- WIM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989212"
---
# <a name="wim_open-message"></a><span data-ttu-id="719ef-104">\_Сообщение Open WIM</span><span class="sxs-lookup"><span data-stu-id="719ef-104">WIM\_OPEN message</span></span>

<span data-ttu-id="719ef-105">При открытии входного устройства с звуковой звукозаписью сообщение о **\_ открытом формате WIM** отправляется в функцию обратного вызова звукового сигнала звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="719ef-105">The **WIM\_OPEN** message is sent to a waveform-audio input callback function when a waveform-audio input device is opened.</span></span>


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="719ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="719ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="719ef-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="719ef-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="719ef-108">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="719ef-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="719ef-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="719ef-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="719ef-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="719ef-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="719ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="719ef-111">Return Value</span></span>

<span data-ttu-id="719ef-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="719ef-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="719ef-113">Требования</span><span class="sxs-lookup"><span data-stu-id="719ef-113">Requirements</span></span>



| <span data-ttu-id="719ef-114">Требование</span><span class="sxs-lookup"><span data-stu-id="719ef-114">Requirement</span></span> | <span data-ttu-id="719ef-115">Значение</span><span class="sxs-lookup"><span data-stu-id="719ef-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="719ef-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="719ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="719ef-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="719ef-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="719ef-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="719ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="719ef-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="719ef-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="719ef-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="719ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="719ef-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="719ef-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="719ef-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="719ef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719ef-123">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="719ef-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="719ef-124">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="719ef-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





