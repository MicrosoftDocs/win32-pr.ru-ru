---
title: Сообщение MM_MIXM_LINE_CHANGE (Ммсистем. h)
description: '\_ \_ \_ Устройство микшера отправляет сообщение об изменении строки mm миксм, чтобы уведомить приложение о том, что изменилось состояние звуковой линии на указанном устройстве. Приложение должно обновить отображаемые и кэшированные значения для указанной звуковой строки.'
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681996"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="248ae-105">\_ \_ \_ Сообщение об изменении миксм строки mm</span><span class="sxs-lookup"><span data-stu-id="248ae-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="248ae-106">Устройство микшера отправляет сообщение об **\_ \_ \_ изменении строки mm миксм** , чтобы уведомить приложение о том, что изменилось состояние звуковой линии на указанном устройстве.</span><span class="sxs-lookup"><span data-stu-id="248ae-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="248ae-107">Приложение должно обновить отображаемые и кэшированные значения для указанной звуковой строки.</span><span class="sxs-lookup"><span data-stu-id="248ae-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="248ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="248ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="248ae-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*хмиксер*</span><span class="sxs-lookup"><span data-stu-id="248ae-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="248ae-110">Маркер устройства микшера, отправившего сообщение уведомления.</span><span class="sxs-lookup"><span data-stu-id="248ae-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="248ae-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*двлинеид*</span><span class="sxs-lookup"><span data-stu-id="248ae-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="248ae-112">Идентификатор строки для звуковой строки, которая изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="248ae-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="248ae-113">Этот идентификатор совпадает с элементом **двлинеид** структуры **миксерлине**, возвращенной функцией **миксержетлинеинфо**.</span><span class="sxs-lookup"><span data-stu-id="248ae-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="248ae-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="248ae-114">Remarks</span></span>

<span data-ttu-id="248ae-115">Приложение должно открыть микшерное устройство и указать окно обратного вызова для получения сообщения **об \_ \_ \_ изменении mm миксм Line** .</span><span class="sxs-lookup"><span data-stu-id="248ae-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="248ae-116">Требования</span><span class="sxs-lookup"><span data-stu-id="248ae-116">Requirements</span></span>



| <span data-ttu-id="248ae-117">Требование</span><span class="sxs-lookup"><span data-stu-id="248ae-117">Requirement</span></span> | <span data-ttu-id="248ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="248ae-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="248ae-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="248ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="248ae-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="248ae-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="248ae-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="248ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="248ae-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="248ae-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="248ae-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="248ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="248ae-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="248ae-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="248ae-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="248ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248ae-126">Аудио Миксерс</span><span class="sxs-lookup"><span data-stu-id="248ae-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="248ae-127">Сообщения микшера звука</span><span class="sxs-lookup"><span data-stu-id="248ae-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





