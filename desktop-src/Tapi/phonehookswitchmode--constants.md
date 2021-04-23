---
description: '\_Константы побитового флага фонехуксвитчмоде описывают компоненты микрофона и динамика устройства хуксвитч.'
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Константы PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680104"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="604bc-103">\_Константы фонехуксвитчмоде</span><span class="sxs-lookup"><span data-stu-id="604bc-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="604bc-104">Константы побитового флага **фонехуксвитчмоде \_** описывают компоненты микрофона и динамика устройства хуксвитч.</span><span class="sxs-lookup"><span data-stu-id="604bc-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="604bc-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**\_микрофон фонехуксвитчмоде**</span><span class="sxs-lookup"><span data-stu-id="604bc-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="604bc-106">Микрофон устройства активен, динамик выключен.</span><span class="sxs-lookup"><span data-stu-id="604bc-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="604bc-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**ФОНЕХУКСВИТЧМОДЕ \_ микспеакер**</span><span class="sxs-lookup"><span data-stu-id="604bc-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="604bc-108">Микрофон и динамик устройства активны.</span><span class="sxs-lookup"><span data-stu-id="604bc-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="604bc-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**ФОНЕХУКСВИТЧМОДЕ \_ ONhook**</span><span class="sxs-lookup"><span data-stu-id="604bc-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="604bc-110">Микрофон и динамик устройства являются onhook обработчиками.</span><span class="sxs-lookup"><span data-stu-id="604bc-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="604bc-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**ФОНЕХУКСВИТЧМОДЕ \_ докладчик**</span><span class="sxs-lookup"><span data-stu-id="604bc-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="604bc-112">Динамик устройства активен, микрофон выключен.</span><span class="sxs-lookup"><span data-stu-id="604bc-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="604bc-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**ФОНЕХУКСВИТЧМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="604bc-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="604bc-114">В настоящее время режим хуксвитча устройства неизвестен.</span><span class="sxs-lookup"><span data-stu-id="604bc-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="604bc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="604bc-115">Remarks</span></span>

<span data-ttu-id="604bc-116">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="604bc-116">No extensibility.</span></span> <span data-ttu-id="604bc-117">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="604bc-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="604bc-118">Эти константы используются для предоставления индивидуального уровня контроля над компонентами микрофона и динамиков телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="604bc-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="604bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="604bc-119">Requirements</span></span>



| <span data-ttu-id="604bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="604bc-120">Requirement</span></span> | <span data-ttu-id="604bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="604bc-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="604bc-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="604bc-122">TAPI version</span></span><br/> | <span data-ttu-id="604bc-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="604bc-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="604bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="604bc-124">Header</span></span><br/>       | <dl> <span data-ttu-id="604bc-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="604bc-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




