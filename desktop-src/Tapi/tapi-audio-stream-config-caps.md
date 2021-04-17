---
description: Структура Caps config для настройки аудиопотока в ИНТЕРФЕЙСе TAPI \_ \_ содержится в \_ \_ \_ структуре "ЗАГЛУШКи" конфигурации потока TAPI, \_ \_ Если для элемента капстипе задан элемент аудиокап объединения стреамконфигкапстипе.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Структура TAPI_AUDIO_STREAM_CONFIG_CAPS (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675393"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="9930d-103">\_ \_ \_ Структура политик CAPS для настройки аудио потока TAPI \_</span><span class="sxs-lookup"><span data-stu-id="9930d-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="9930d-104">\[ Эта структура недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9930d-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9930d-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="9930d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9930d-106">Структура **\_ \_ \_ \_ Caps config для настройки аудиопотока в интерфейсе** TAPI содержится в структуре " [**\_ \_ \_ заглушки" конфигурации потока TAPI**](tapi-stream-config-caps.md) , если для элемента **капстипе** задан элемент **аудиокап** объединения [**стреамконфигкапстипе**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="9930d-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="9930d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9930d-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="9930d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9930d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9930d-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9930d-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-110">Понятное описание типа конфигурации аудиопотока для показа пользователям приложений.</span><span class="sxs-lookup"><span data-stu-id="9930d-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-111">**минимумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="9930d-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-112">Минимальное число каналов, связанных с потоком.</span><span class="sxs-lookup"><span data-stu-id="9930d-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-113">**максимумчаннелс**</span><span class="sxs-lookup"><span data-stu-id="9930d-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-114">Максимальное число каналов, связанных с потоком.</span><span class="sxs-lookup"><span data-stu-id="9930d-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-115">**чаннелсгрануларити**</span><span class="sxs-lookup"><span data-stu-id="9930d-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-116">Гранулярность числа каналов.</span><span class="sxs-lookup"><span data-stu-id="9930d-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-117">**минимумбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="9930d-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-118">Минимальное число битов на выборку.</span><span class="sxs-lookup"><span data-stu-id="9930d-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-119">**максимумбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="9930d-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-120">Максимальное количество битов на выборку.</span><span class="sxs-lookup"><span data-stu-id="9930d-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-121">**битсперсамплегрануларити**</span><span class="sxs-lookup"><span data-stu-id="9930d-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-122">Гранулярность битов на выборку значений.</span><span class="sxs-lookup"><span data-stu-id="9930d-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-123">**минимумсамплефрекуенци**</span><span class="sxs-lookup"><span data-stu-id="9930d-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-124">Минимальная частота выборки.</span><span class="sxs-lookup"><span data-stu-id="9930d-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-125">**максимумсамплефрекуенци**</span><span class="sxs-lookup"><span data-stu-id="9930d-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-126">Максимальная частота выборки.</span><span class="sxs-lookup"><span data-stu-id="9930d-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-127">**самплефрекуенцигрануларити**</span><span class="sxs-lookup"><span data-stu-id="9930d-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-128">Гранулярность значений частоты выборки.</span><span class="sxs-lookup"><span data-stu-id="9930d-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-129">**минимумавгбитесперсек**</span><span class="sxs-lookup"><span data-stu-id="9930d-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-130">Минимальное среднее значение в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="9930d-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-131">**максимумавгбитесперсек**</span><span class="sxs-lookup"><span data-stu-id="9930d-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-132">Максимальное значение среднего значения в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="9930d-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="9930d-133">**авгбитесперсекгрануларити**</span><span class="sxs-lookup"><span data-stu-id="9930d-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="9930d-134">Гранулярность значений байтов в секунду.</span><span class="sxs-lookup"><span data-stu-id="9930d-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9930d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="9930d-135">Requirements</span></span>



| <span data-ttu-id="9930d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="9930d-136">Requirement</span></span> | <span data-ttu-id="9930d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9930d-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9930d-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9930d-138">TAPI version</span></span><br/> | <span data-ttu-id="9930d-139">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="9930d-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="9930d-140">Header</span><span class="sxs-lookup"><span data-stu-id="9930d-140">Header</span></span><br/>       | <dl> <span data-ttu-id="9930d-141"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9930d-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9930d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9930d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9930d-143">**\_ \_ ограничения конфигурации потока \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="9930d-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




