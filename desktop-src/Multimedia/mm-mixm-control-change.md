---
title: Сообщение MM_MIXM_CONTROL_CHANGE (Ммсистем. h)
description: '\_ \_ \_ Устройство-микшер отправляет сообщение об изменении элемента управления миксм mm, чтобы уведомить приложение о том, что изменилось состояние элемента управления, связанного с звуковой линией. Приложение должно обновить отображаемые и кэшированные значения для указанного элемента управления.'
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650384"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="9f460-105">\_ \_ Сообщение об изменении элемента управления миксм mm \_</span><span class="sxs-lookup"><span data-stu-id="9f460-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="9f460-106">Устройство-микшер отправляет сообщение об **\_ \_ \_ изменении элемента управления миксм mm** , чтобы уведомить приложение о том, что изменилось состояние элемента управления, связанного с звуковой линией.</span><span class="sxs-lookup"><span data-stu-id="9f460-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="9f460-107">Приложение должно обновить отображаемые и кэшированные значения для указанного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9f460-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="9f460-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f460-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*хмиксер*</span><span class="sxs-lookup"><span data-stu-id="9f460-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="9f460-110">Маркер устройства микшера (**хмиксер**), отправившего сообщение уведомления.</span><span class="sxs-lookup"><span data-stu-id="9f460-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="9f460-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*двконтролид*</span><span class="sxs-lookup"><span data-stu-id="9f460-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="9f460-112">Идентификатор элемента управления микшера, состояние которого изменилось.</span><span class="sxs-lookup"><span data-stu-id="9f460-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="9f460-113">Этот идентификатор совпадает с элементом **двконтролид** структуры **миксерконтрол**, возвращенной функцией **миксержетлинеконтролс**.</span><span class="sxs-lookup"><span data-stu-id="9f460-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f460-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f460-114">Remarks</span></span>

<span data-ttu-id="9f460-115">Приложение должно открыть микшер устройства и указать окно обратного вызова для получения сообщения об **\_ \_ \_ изменении элемента управления mm миксм** .</span><span class="sxs-lookup"><span data-stu-id="9f460-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f460-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9f460-116">Requirements</span></span>



| <span data-ttu-id="9f460-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9f460-117">Requirement</span></span> | <span data-ttu-id="9f460-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f460-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f460-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f460-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f460-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f460-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f460-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f460-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f460-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f460-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f460-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f460-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f460-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f460-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f460-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f460-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f460-126">Аудио Миксерс</span><span class="sxs-lookup"><span data-stu-id="9f460-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="9f460-127">Сообщения микшера звука</span><span class="sxs-lookup"><span data-stu-id="9f460-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





