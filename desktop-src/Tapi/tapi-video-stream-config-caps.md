---
description: '\_ \_ \_ Структура Caps config для настройки потока видео TAPI \_ содержится в структуре " \_ ЗАГЛУШКи" конфигурации потока TAPI, \_ \_ Если для элемента капстипе задан элемент видеокап объединения стреамконфигкапстипе.'
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Структура TAPI_VIDEO_STREAM_CONFIG_CAPS (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679747"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="0998d-103">\_ \_ \_ Структура ограничений конфигурации потока видео TAPI \_</span><span class="sxs-lookup"><span data-stu-id="0998d-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="0998d-104">\[ Эта структура недоступна для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0998d-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0998d-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="0998d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0998d-106">Структура **\_ \_ \_ \_ Caps config для настройки потока видео TAPI** содержится в структуре [**" \_ \_ \_ заглушки" конфигурации потока TAPI**](tapi-stream-config-caps.md) , если для элемента **капстипе** задан элемент **видеокап** объединения [**стреамконфигкапстипе**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="0998d-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="0998d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0998d-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="0998d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0998d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0998d-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0998d-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-110">Понятное описание типа конфигурации аудиопотока для показа пользователям приложений.</span><span class="sxs-lookup"><span data-stu-id="0998d-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-111">**видеостандард**</span><span class="sxs-lookup"><span data-stu-id="0998d-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-112">Используемый стандарт видео.</span><span class="sxs-lookup"><span data-stu-id="0998d-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-113">**инпутсизе**</span><span class="sxs-lookup"><span data-stu-id="0998d-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-114">Размер входных данных кадра.</span><span class="sxs-lookup"><span data-stu-id="0998d-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-115">**минкроппингсизе**</span><span class="sxs-lookup"><span data-stu-id="0998d-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-116">Минимальный размер обрезки.</span><span class="sxs-lookup"><span data-stu-id="0998d-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-117">**макскроппингсизе**</span><span class="sxs-lookup"><span data-stu-id="0998d-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-118">Максимальный размер обрезки.</span><span class="sxs-lookup"><span data-stu-id="0998d-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-119">**кропгрануларитикс**</span><span class="sxs-lookup"><span data-stu-id="0998d-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-120">Детализация обрезки, допустимой вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="0998d-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-121">**кропгрануларитии**</span><span class="sxs-lookup"><span data-stu-id="0998d-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-122">Детализация обрезки, допустимой вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="0998d-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-123">**кропалигнкс**</span><span class="sxs-lookup"><span data-stu-id="0998d-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-124">Выравнивание обрезки по оси x.</span><span class="sxs-lookup"><span data-stu-id="0998d-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-125">**кропалигни**</span><span class="sxs-lookup"><span data-stu-id="0998d-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-126">Выравнивание обрезки по оси y.</span><span class="sxs-lookup"><span data-stu-id="0998d-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-127">**минаутпутсизе**</span><span class="sxs-lookup"><span data-stu-id="0998d-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-128">Минимальный результирующий размер окна видео.</span><span class="sxs-lookup"><span data-stu-id="0998d-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-129">**максаутпутсизе**</span><span class="sxs-lookup"><span data-stu-id="0998d-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-130">Максимальный итоговый размер окна видео.</span><span class="sxs-lookup"><span data-stu-id="0998d-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-131">**аутпутгрануларитикс**</span><span class="sxs-lookup"><span data-stu-id="0998d-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-132">Степень гранулярности выходного размера вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="0998d-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-133">**аутпутгрануларитии**</span><span class="sxs-lookup"><span data-stu-id="0998d-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-134">Степень гранулярности выходного размера вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="0998d-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-135">**стретчтапскс**</span><span class="sxs-lookup"><span data-stu-id="0998d-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-136">Растяжение по оси x.</span><span class="sxs-lookup"><span data-stu-id="0998d-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-137">**стретчтапси**</span><span class="sxs-lookup"><span data-stu-id="0998d-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-138">Растяните по оси y.</span><span class="sxs-lookup"><span data-stu-id="0998d-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-139">**шринктапскс**</span><span class="sxs-lookup"><span data-stu-id="0998d-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-140">Уменьшите по оси x.</span><span class="sxs-lookup"><span data-stu-id="0998d-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-141">**шринктапси**</span><span class="sxs-lookup"><span data-stu-id="0998d-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-142">Уменьшите по оси y.</span><span class="sxs-lookup"><span data-stu-id="0998d-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-143">**минфрамеинтервал**</span><span class="sxs-lookup"><span data-stu-id="0998d-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-144">Минимальный интервал видеокадра.</span><span class="sxs-lookup"><span data-stu-id="0998d-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-145">**максфрамеинтервал**</span><span class="sxs-lookup"><span data-stu-id="0998d-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-146">Максимальный интервал кадров видео.</span><span class="sxs-lookup"><span data-stu-id="0998d-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-147">**минбитсперсеконд**</span><span class="sxs-lookup"><span data-stu-id="0998d-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-148">Минимальное число бит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0998d-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="0998d-149">**максбитсперсеконд**</span><span class="sxs-lookup"><span data-stu-id="0998d-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="0998d-150">Максимальное число бит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0998d-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0998d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="0998d-151">Requirements</span></span>



| <span data-ttu-id="0998d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="0998d-152">Requirement</span></span> | <span data-ttu-id="0998d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="0998d-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0998d-154">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0998d-154">TAPI version</span></span><br/> | <span data-ttu-id="0998d-155">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0998d-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="0998d-156">Header</span><span class="sxs-lookup"><span data-stu-id="0998d-156">Header</span></span><br/>       | <dl> <span data-ttu-id="0998d-157"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0998d-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0998d-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0998d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0998d-159">**\_ \_ ограничения конфигурации потока \_ TAPI**</span><span class="sxs-lookup"><span data-stu-id="0998d-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




