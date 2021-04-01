---
title: Сообщение MM_WIM_OPEN (Ммсистем. h)
description: '\_ \_ При открытии входного устройства с звуковой звукозаписью в окне будет отправлено сообщение с открытым WIM-файлом.'
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072023"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="746bd-104">MM \_ , \_ сообщение Open WIM</span><span class="sxs-lookup"><span data-stu-id="746bd-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="746bd-105">При открытии входного устройства с звуковой звукозаписью в окне будет отправлено сообщение с **\_ \_ открытым WIM** -файлом.</span><span class="sxs-lookup"><span data-stu-id="746bd-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="746bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="746bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746bd-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*хинпутдев*</span><span class="sxs-lookup"><span data-stu-id="746bd-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="746bd-108">Обработчик для открытого устройства.</span><span class="sxs-lookup"><span data-stu-id="746bd-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="746bd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="746bd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="746bd-110">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="746bd-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="746bd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="746bd-111">Return Value</span></span>

<span data-ttu-id="746bd-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="746bd-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="746bd-113">Требования</span><span class="sxs-lookup"><span data-stu-id="746bd-113">Requirements</span></span>



| <span data-ttu-id="746bd-114">Требование</span><span class="sxs-lookup"><span data-stu-id="746bd-114">Requirement</span></span> | <span data-ttu-id="746bd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="746bd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="746bd-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="746bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="746bd-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="746bd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="746bd-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="746bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="746bd-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="746bd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="746bd-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="746bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="746bd-121"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="746bd-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="746bd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="746bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746bd-123">Звуковая волна</span><span class="sxs-lookup"><span data-stu-id="746bd-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="746bd-124">Сообщения волны</span><span class="sxs-lookup"><span data-stu-id="746bd-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





