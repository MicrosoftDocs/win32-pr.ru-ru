---
title: Структура WINBIO_EXTENDED_SENSOR_INFO (Винбио \_ types. h)
description: Содержит сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического блока.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- API структуры WINBIO_EXTENDED_SENSOR_INFO биометрическая платформа Windows
- PWINBIO_EXTENDED_SENSOR_INFO API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988301"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="a2274-105">\_ \_ Структура сведений о расширенном ДАТЧИКе винбио \_</span><span class="sxs-lookup"><span data-stu-id="a2274-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="a2274-106">Содержит сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="a2274-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2274-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2274-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="a2274-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a2274-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2274-109">**женериксенсоркапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="a2274-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-110">Универсальные возможности компонента датчика, подключенного к определенной биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="a2274-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-111">**Фактор**</span><span class="sxs-lookup"><span data-stu-id="a2274-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-112">Тип биометрического блока, для которого эта структура содержит сведения о возможностях и требованиях к регистрации адаптера датчика.</span><span class="sxs-lookup"><span data-stu-id="a2274-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="a2274-113">Например, если значение элемента **коэффициента** — **винбио \_ типа " \_ отпечаток**", то структура **\_ \_ \_ сведений о расширенном датчике винбио** применяется к считывателю отпечатков пальцев и содержит соответствующие сведения в структуре **спеЦифк. отпечаток** .</span><span class="sxs-lookup"><span data-stu-id="a2274-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-114">**Specific**</span><span class="sxs-lookup"><span data-stu-id="a2274-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-115">Сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического модуля, связанного с конкретным биометрической степенью.</span><span class="sxs-lookup"><span data-stu-id="a2274-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="a2274-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="a2274-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a2274-117">Reserved.</span></span> <span data-ttu-id="a2274-118">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a2274-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-119">**фаЦиалфеатурес**</span><span class="sxs-lookup"><span data-stu-id="a2274-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-120">Сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического модуля, связанного с функциями лиц.</span><span class="sxs-lookup"><span data-stu-id="a2274-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="a2274-121">**фрамесизе**</span><span class="sxs-lookup"><span data-stu-id="a2274-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-122">Размер рамки камеры, обозначенной как Длина и ширина в пикселях с помощью **правых** и **нижних** элементов структуры [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2274-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="a2274-123">Точка (0, 0) представляет левый верхний угол рамки.</span><span class="sxs-lookup"><span data-stu-id="a2274-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-124">**фрамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="a2274-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-125">Смещение кадра камеры для грани от видеокамеры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a2274-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="a2274-126">Значение (0, 0) указывает, что кадры камеры для поверхности и видеокамеры полностью перекрываются.</span><span class="sxs-lookup"><span data-stu-id="a2274-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-127">**мандаторйориентатион**</span><span class="sxs-lookup"><span data-stu-id="a2274-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-128">Предпочтительная ориентация для камеры.</span><span class="sxs-lookup"><span data-stu-id="a2274-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2274-129">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="a2274-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-130">Сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического модуля, связанного с шаблонами отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="a2274-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a2274-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a2274-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-132">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a2274-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2274-133">**IRI**</span><span class="sxs-lookup"><span data-stu-id="a2274-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-134">Сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического модуля, связанного с шаблонами IRI.</span><span class="sxs-lookup"><span data-stu-id="a2274-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a2274-135">**фрамесизе**</span><span class="sxs-lookup"><span data-stu-id="a2274-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-136">Размер рамки камеры, обозначенной как Длина и ширина в пикселях с помощью **правых** и **нижних** элементов структуры [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2274-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="a2274-137">Точка (0, 0) представляет левый верхний угол рамки.</span><span class="sxs-lookup"><span data-stu-id="a2274-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-138">**фрамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="a2274-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-139">Смещение кадра камеры для диафрагмы от видеокамеры (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="a2274-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="a2274-140">Значение (0, 0) указывает, что кадр камеры для диафрагмы и видеокамеры полностью перекрывается.</span><span class="sxs-lookup"><span data-stu-id="a2274-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="a2274-141">**мандаторйориентатион**</span><span class="sxs-lookup"><span data-stu-id="a2274-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-142">Предпочтительная ориентация для камеры.</span><span class="sxs-lookup"><span data-stu-id="a2274-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2274-143">**Голосовая связь**</span><span class="sxs-lookup"><span data-stu-id="a2274-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-144">Сведения о возможностях и требованиях к регистрации адаптера датчика для биометрического модуля, связанного с голосовыми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="a2274-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a2274-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a2274-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a2274-146">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a2274-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2274-147">Требования</span><span class="sxs-lookup"><span data-stu-id="a2274-147">Requirements</span></span>



| <span data-ttu-id="a2274-148">Требование</span><span class="sxs-lookup"><span data-stu-id="a2274-148">Requirement</span></span> | <span data-ttu-id="a2274-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a2274-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2274-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2274-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a2274-151">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a2274-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a2274-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2274-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a2274-153">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a2274-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="a2274-154">Header</span><span class="sxs-lookup"><span data-stu-id="a2274-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2274-155"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="a2274-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2274-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2274-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2274-157">**\_Константы возможностей винбио**</span><span class="sxs-lookup"><span data-stu-id="a2274-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="a2274-158">**\_Константы БИОметрического \_ типа винбио**</span><span class="sxs-lookup"><span data-stu-id="a2274-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="a2274-159">**\_Константы ориентации винбио**</span><span class="sxs-lookup"><span data-stu-id="a2274-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

