---
title: Сообщение WOM_OPEN (Ммсистем. h)
description: '\_При открытии выходного устройства с аудио-аудиосигналом вом открытое сообщение отправляется в функцию выходного обратного вызова аудио-звука.'
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135070"
---
# <a name="wom_open-message"></a><span data-ttu-id="b6b47-104">ВОМ \_ открытое сообщение</span><span class="sxs-lookup"><span data-stu-id="b6b47-104">WOM\_OPEN message</span></span>

<span data-ttu-id="b6b47-105">При открытии выходного устройства с аудио-аудиосигналом **вом \_ открытое** сообщение отправляется в функцию выходного обратного вызова аудио-звука.</span><span class="sxs-lookup"><span data-stu-id="b6b47-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b6b47-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6b47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b47-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b6b47-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b6b47-108">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b6b47-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6b47-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b6b47-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b6b47-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b6b47-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b47-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6b47-111">Return Value</span></span>

<span data-ttu-id="b6b47-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b6b47-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b47-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b6b47-113">Requirements</span></span>



| <span data-ttu-id="b6b47-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b6b47-114">Requirement</span></span> | <span data-ttu-id="b6b47-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b6b47-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b47-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6b47-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b47-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6b47-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b6b47-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6b47-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b47-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6b47-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6b47-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6b47-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b47-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6b47-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b47-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6b47-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b47-123">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="b6b47-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="b6b47-124">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="b6b47-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





