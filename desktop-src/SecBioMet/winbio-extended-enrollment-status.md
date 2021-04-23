---
title: Структура WINBIO_EXTENDED_ENROLLMENT_STATUS (Винбио \_ types. h)
description: Содержит дополнительные сведения о состоянии выполняемой регистрации.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- API структуры WINBIO_EXTENDED_ENROLLMENT_STATUS биометрическая платформа Windows
- PWINBIO_EXTENDED_ENROLLMENT_STATUS API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135347"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="4557e-105">\_ \_ Структура состояния расширенной регистрации винбио \_</span><span class="sxs-lookup"><span data-stu-id="4557e-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="4557e-106">Содержит дополнительные сведения о состоянии выполняемой регистрации.</span><span class="sxs-lookup"><span data-stu-id="4557e-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="4557e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4557e-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="4557e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4557e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4557e-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="4557e-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-110">Состояние образца коллекции для шаблона регистрации.</span><span class="sxs-lookup"><span data-stu-id="4557e-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="4557e-111">Для этого элемента возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="4557e-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="4557e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4557e-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="4557e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4557e-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="4557e-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4557e-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="4557e-115">Регистрация готова к сохранению.</span><span class="sxs-lookup"><span data-stu-id="4557e-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="4557e-116"><dt>**ВИНБИО \_ E \_ Недопустимая \_ операция**</dt></span><span class="sxs-lookup"><span data-stu-id="4557e-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4557e-117">Регистрация не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4557e-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="4557e-118"><dt>**ВИНБИО \_ я \_ больше \_ данных**</dt></span><span class="sxs-lookup"><span data-stu-id="4557e-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="4557e-119">Для завершения шаблона требуются дополнительные примеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="4557e-120"><dt>**ВИНБИО \_ \_ неправильная \_ запись**</dt></span><span class="sxs-lookup"><span data-stu-id="4557e-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="4557e-121">Самый последний пример не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="4557e-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="4557e-122">**режектдетаил**</span><span class="sxs-lookup"><span data-stu-id="4557e-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-123">Причина, по которой последний пример непригоден для использования, если значение элемента **темплатестатус** равно **винбио \_ E \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4557e-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="4557e-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-125">Лучшая оценка из адаптера подсистемы для процента завершенного шаблона в виде значения от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="4557e-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-126">**Фактор**</span><span class="sxs-lookup"><span data-stu-id="4557e-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-127">Тип биометрического блока, для которого эта структура содержит сведения о возможностях и требованиях к регистрации адаптера подсистемы.</span><span class="sxs-lookup"><span data-stu-id="4557e-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="4557e-128">Например, если значение элемента **коэффициента** — **винбио \_ типа \_ отпечатков пальцев**, структура [**\_ \_ \_ сведений о расширенном подсистеме винбио**](winbio-extended-engine-info.md) применяется к сканеру отпечатков пальцев и содержит соответствующие сведения в структуре **спеЦифк. отпечатков пальцев** .</span><span class="sxs-lookup"><span data-stu-id="4557e-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-129">**Подфакт**</span><span class="sxs-lookup"><span data-stu-id="4557e-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-130">Значение **\_ \_ ПОДтипа БИОметрической метрики винбио** , которое предоставляет дополнительные сведения о регистрации.</span><span class="sxs-lookup"><span data-stu-id="4557e-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-131">**Specific**</span><span class="sxs-lookup"><span data-stu-id="4557e-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-132">Сведения о состоянии регистрации, выполняемой для определенного биометрического фактора.</span><span class="sxs-lookup"><span data-stu-id="4557e-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="4557e-133">**Null**</span><span class="sxs-lookup"><span data-stu-id="4557e-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-134">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4557e-134">Reserved.</span></span> <span data-ttu-id="4557e-135">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4557e-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-136">**фаЦиалфеатурес**</span><span class="sxs-lookup"><span data-stu-id="4557e-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-137">Сведения о состоянии регистрации, которая выполняется для функций лица.</span><span class="sxs-lookup"><span data-stu-id="4557e-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="4557e-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="4557e-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-139">Расположение в пикселях рамки камеры лица, которое необходимо зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="4557e-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="4557e-140">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="4557e-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="4557e-141">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="4557e-142">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-143">**расстояние;**</span><span class="sxs-lookup"><span data-stu-id="4557e-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-144">Расстояние между фактическим расположением лица и идеальным фокусом для лица.</span><span class="sxs-lookup"><span data-stu-id="4557e-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="4557e-145">Это значение находится в диапазоне от-100 до 100.</span><span class="sxs-lookup"><span data-stu-id="4557e-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="4557e-146">0 указывает на идеальное расстояние, положительные значения указывают на то, что фактическое расположение грани слишком далеко, а отрицательные значения указывают на то, что фактическое расположение слишком близко.</span><span class="sxs-lookup"><span data-stu-id="4557e-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4557e-147">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="4557e-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-148">Сведения о состоянии регистрации, выполняемой для шаблонов отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="4557e-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="4557e-149">**женералсамплес**</span><span class="sxs-lookup"><span data-stu-id="4557e-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-150">Общее число выборок, необходимых для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-151">**Center**</span><span class="sxs-lookup"><span data-stu-id="4557e-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-152">Число выборок для центра отпечатка пальца, необходимых для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-153">**топедже**</span><span class="sxs-lookup"><span data-stu-id="4557e-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-154">Число выборок для верхнего края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-155">**боттомедже**</span><span class="sxs-lookup"><span data-stu-id="4557e-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-156">Число выборок для нижнего края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-157">**лефтедже**</span><span class="sxs-lookup"><span data-stu-id="4557e-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-158">Число выборок для левого края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-159">**ригхтедже**</span><span class="sxs-lookup"><span data-stu-id="4557e-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-160">Число выборок для правого края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="4557e-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4557e-161">**IRI**</span><span class="sxs-lookup"><span data-stu-id="4557e-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-162">Сведения о состоянии регистрации, выполняемой для шаблонов IRI.</span><span class="sxs-lookup"><span data-stu-id="4557e-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="4557e-163">**Эйебаундингбокс \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4557e-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-164">Расположение в кадре камеры одного из IRI, которое регистрируется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4557e-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="4557e-165">Если система распознавания IRI ведет наблюдение только за одним глазом, это должно быть переведение этого глаза.</span><span class="sxs-lookup"><span data-stu-id="4557e-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="4557e-166">Если система распознавания IRI отслеживает оба глаза, но только один глаз находится в кадре камеры, то эта размещается в виде диафрагмы в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="4557e-167">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это может быть диафрагма правильного взгляда на человека.</span><span class="sxs-lookup"><span data-stu-id="4557e-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="4557e-168">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="4557e-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="4557e-169">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="4557e-170">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-171">**Эйебаундингбокс \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4557e-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-172">Расположение в кадре камеры одного из IRI, которое регистрируется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="4557e-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="4557e-173">Если система распознавания IRI отслеживает только один глаз или только один глаз находится в кадре камеры, это значение пустое.</span><span class="sxs-lookup"><span data-stu-id="4557e-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="4557e-174">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это может быть сочетание левого взгляда.</span><span class="sxs-lookup"><span data-stu-id="4557e-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="4557e-175">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="4557e-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="4557e-176">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="4557e-177">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-178">**Пупилцентер \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4557e-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-179">Расположение центра одного из пупилс отдельного объекта для регистрации.</span><span class="sxs-lookup"><span data-stu-id="4557e-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="4557e-180">Если система распознавания IRI ведет наблюдение только за одним глазом, это должно быть центр пупилности этого глаза.</span><span class="sxs-lookup"><span data-stu-id="4557e-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="4557e-181">Если система распознавания IRI отслеживает оба глаза, но в кадре камеры находится только один глаз, то эта единица является центром пупил глаз в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="4557e-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="4557e-182">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это будет пупился от того, насколько он подходит.</span><span class="sxs-lookup"><span data-stu-id="4557e-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-183">**Пупилцентер \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4557e-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-184">Расположение центра одного из пупилс отдельного объекта для регистрации.</span><span class="sxs-lookup"><span data-stu-id="4557e-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="4557e-185">Если система распознавания IRI отслеживает только один глаз или только один глаз находится в кадре камеры, это значение пустое.</span><span class="sxs-lookup"><span data-stu-id="4557e-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="4557e-186">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это будет пупил от левого взгляда на человека.</span><span class="sxs-lookup"><span data-stu-id="4557e-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="4557e-187">**расстояние;**</span><span class="sxs-lookup"><span data-stu-id="4557e-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-188">Расстояние между фактическим расположением диафрагмы и идеальным фокальным расстоянием для диафрагмы.</span><span class="sxs-lookup"><span data-stu-id="4557e-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="4557e-189">Это значение находится в диапазоне от-100 до 100.</span><span class="sxs-lookup"><span data-stu-id="4557e-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="4557e-190">0 указывает на идеальное расстояние, положительные значения указывают на то, что фактическое расположение диафрагмы слишком далеко, а отрицательные значения указывают на то, что фактическое расположение слишком близко.</span><span class="sxs-lookup"><span data-stu-id="4557e-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4557e-191">**Голосовая связь**</span><span class="sxs-lookup"><span data-stu-id="4557e-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-192">Сведения о состоянии регистрации, выполняемой для шаблонов голоса.</span><span class="sxs-lookup"><span data-stu-id="4557e-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="4557e-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="4557e-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="4557e-194">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4557e-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4557e-195">Требования</span><span class="sxs-lookup"><span data-stu-id="4557e-195">Requirements</span></span>



| <span data-ttu-id="4557e-196">Требование</span><span class="sxs-lookup"><span data-stu-id="4557e-196">Requirement</span></span> | <span data-ttu-id="4557e-197">Значение</span><span class="sxs-lookup"><span data-stu-id="4557e-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4557e-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4557e-198">Minimum supported client</span></span><br/> | <span data-ttu-id="4557e-199">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4557e-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="4557e-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4557e-200">Minimum supported server</span></span><br/> | <span data-ttu-id="4557e-201">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4557e-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="4557e-202">Header</span><span class="sxs-lookup"><span data-stu-id="4557e-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="4557e-203"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="4557e-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





