---
title: Объединение WINBIO_PRESENCE_PROPERTIES (Винбио \_ types. h)
description: Содержит биометрические значения, используемые биометрическая платформа Windows для определения наличия конкретного пользователя.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API-интерфейс биометрическая платформа Windows объединения WINBIO_PRESENCE_PROPERTIES
- PWINBIO_PRESENCE_PROPERTIES API биометрическая платформа Windows указателя Union
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489555"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="d4167-105">\_ \_ Объединение свойств присутствия винбио</span><span class="sxs-lookup"><span data-stu-id="d4167-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="d4167-106">Содержит биометрические значения, используемые биометрическая платформа Windows для определения наличия конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4167-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4167-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4167-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="d4167-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d4167-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4167-109">**фаЦиалфеатурес**</span><span class="sxs-lookup"><span data-stu-id="d4167-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-110">Значения, определяющие расположение лиц, которые биометрическая платформа Windows использовали для определения наличия конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4167-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="d4167-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="d4167-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-112">Расположение в кадре камеры, лицевой стороны лица, в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4167-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="d4167-113">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="d4167-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d4167-114">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d4167-115">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="d4167-116">**расстояние;**</span><span class="sxs-lookup"><span data-stu-id="d4167-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-117">Расстояние между фактическим расположением лица и идеальным фокусом для лица.</span><span class="sxs-lookup"><span data-stu-id="d4167-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="d4167-118">Это значение находится в диапазоне от-100 до 100.</span><span class="sxs-lookup"><span data-stu-id="d4167-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="d4167-119">0 указывает на идеальное расстояние, положительные значения указывают на то, что фактическое расположение грани слишком далеко, а отрицательные значения указывают на то, что фактическое расположение слишком близко.</span><span class="sxs-lookup"><span data-stu-id="d4167-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d4167-120">**IRI**</span><span class="sxs-lookup"><span data-stu-id="d4167-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-121">Значения для расположения IRI, которые биометрическая платформа Windows использовали для определения того, что имеется пользователь.</span><span class="sxs-lookup"><span data-stu-id="d4167-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="d4167-122">**Эйебаундингбокс \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d4167-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-123">Расположение в кадре камеры одного из IRI, которое регистрируется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4167-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="d4167-124">Если система распознавания IRI ведет наблюдение только за одним глазом, это должно быть переведение этого глаза.</span><span class="sxs-lookup"><span data-stu-id="d4167-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="d4167-125">Если система распознавания IRI отслеживает оба глаза, но только один глаз находится в кадре камеры, то эта размещается в виде диафрагмы в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="d4167-126">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это может быть диафрагма правильного взгляда на человека.</span><span class="sxs-lookup"><span data-stu-id="d4167-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="d4167-127">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="d4167-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d4167-128">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d4167-129">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="d4167-130">**Эйебаундингбокс \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d4167-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-131">Расположение в кадре камеры одного из IRI, которое регистрируется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4167-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="d4167-132">Если система распознавания IRI отслеживает только один глаз или только один глаз находится в кадре камеры, это значение пустое.</span><span class="sxs-lookup"><span data-stu-id="d4167-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="d4167-133">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это может быть сочетание левого взгляда.</span><span class="sxs-lookup"><span data-stu-id="d4167-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="d4167-134">Размер рамки камеры определяет верхний предел числа пикселей для данной должности.</span><span class="sxs-lookup"><span data-stu-id="d4167-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="d4167-135">Получите свойство **винбио \_ со \_ \_ \_ сведениями о расширенном датчике** , чтобы определить размер рамки камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="d4167-136">Клиент, использующий монитор присутствия, должен выполнить операцию масштабирования для отображения расположения в рамке камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="d4167-137">**Пупилцентер \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d4167-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-138">Расположение центра одного из пупилс отдельного объекта для регистрации.</span><span class="sxs-lookup"><span data-stu-id="d4167-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="d4167-139">Если система распознавания IRI ведет наблюдение только за одним глазом, это должно быть центр пупилности этого глаза.</span><span class="sxs-lookup"><span data-stu-id="d4167-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="d4167-140">Если система распознавания IRI отслеживает оба глаза, но в кадре камеры находится только один глаз, то эта единица является центром пупил глаз в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="d4167-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="d4167-141">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это будет пупился от того, насколько он подходит.</span><span class="sxs-lookup"><span data-stu-id="d4167-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="d4167-142">**Пупилцентер \_ 2**</span><span class="sxs-lookup"><span data-stu-id="d4167-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-143">Расположение центра одного из пупилс отдельного объекта для регистрации.</span><span class="sxs-lookup"><span data-stu-id="d4167-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="d4167-144">Если система распознавания IRI отслеживает только один глаз или только один глаз находится в кадре камеры, это значение пустое.</span><span class="sxs-lookup"><span data-stu-id="d4167-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="d4167-145">Если система распознавания IRI отслеживает оба глаза, и оба глаза находятся в кадре камеры, то, скорее всего, это будет пупил от левого взгляда на человека.</span><span class="sxs-lookup"><span data-stu-id="d4167-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="d4167-146">**расстояние;**</span><span class="sxs-lookup"><span data-stu-id="d4167-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="d4167-147">Расстояние между фактическим расположением диафрагмы и идеальным фокальным расстоянием для диафрагмы.</span><span class="sxs-lookup"><span data-stu-id="d4167-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="d4167-148">Это значение находится в диапазоне от-100 до 100.</span><span class="sxs-lookup"><span data-stu-id="d4167-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="d4167-149">0 указывает на идеальное расстояние, положительные значения указывают на то, что фактическое расположение диафрагмы слишком далеко, а отрицательные значения указывают на то, что фактическое расположение слишком близко.</span><span class="sxs-lookup"><span data-stu-id="d4167-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4167-150">Требования</span><span class="sxs-lookup"><span data-stu-id="d4167-150">Requirements</span></span>



| <span data-ttu-id="d4167-151">Требование</span><span class="sxs-lookup"><span data-stu-id="d4167-151">Requirement</span></span> | <span data-ttu-id="d4167-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d4167-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4167-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4167-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d4167-154">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d4167-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="d4167-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4167-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d4167-156">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="d4167-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="d4167-157">Header</span><span class="sxs-lookup"><span data-stu-id="d4167-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4167-158"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="d4167-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





