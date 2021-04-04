---
title: Сообщение MM_WOM_OPEN (Ммсистем. h)
description: '\_ \_ Сообщение вом Open mm отправляется в окно при открытии данного устройства вывода аудио-аудио.'
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137791"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="f6307-104">ММ \_ вом \_ открытое сообщение</span><span class="sxs-lookup"><span data-stu-id="f6307-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="f6307-105">Сообщение **\_ вом \_ Open mm** отправляется в окно при открытии данного устройства вывода аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="f6307-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f6307-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6307-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*хаутпутдев*</span><span class="sxs-lookup"><span data-stu-id="f6307-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="f6307-108">Обработчик для открытого устройства.</span><span class="sxs-lookup"><span data-stu-id="f6307-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="f6307-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6307-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f6307-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f6307-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6307-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6307-111">Return Value</span></span>

<span data-ttu-id="f6307-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f6307-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6307-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f6307-113">Requirements</span></span>



| <span data-ttu-id="f6307-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f6307-114">Requirement</span></span> | <span data-ttu-id="f6307-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f6307-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6307-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6307-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6307-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6307-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f6307-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6307-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6307-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6307-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f6307-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f6307-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6307-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6307-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6307-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6307-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6307-123">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="f6307-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="f6307-124">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="f6307-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





