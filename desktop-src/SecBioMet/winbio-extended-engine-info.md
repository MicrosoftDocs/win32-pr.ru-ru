---
title: Структура WINBIO_EXTENDED_ENGINE_INFO (Винбио \_ types. h)
description: Содержит сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического блока.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- API структуры WINBIO_EXTENDED_ENGINE_INFO биометрическая платформа Windows
- PWINBIO_EXTENDED_ENGINE_INFO API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892670"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="070fc-105">\_ \_ Структура сведений о расширенном подсистеме винбио \_</span><span class="sxs-lookup"><span data-stu-id="070fc-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="070fc-106">Содержит сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="070fc-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="070fc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="070fc-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="070fc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="070fc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="070fc-109">**женериценгинекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="070fc-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-110">Универсальные возможности компонента ядра, подключенного к определенной биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="070fc-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-111">**Фактор**</span><span class="sxs-lookup"><span data-stu-id="070fc-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-112">Тип биометрического блока, для которого эта структура содержит сведения о возможностях и требованиях к регистрации адаптера подсистемы.</span><span class="sxs-lookup"><span data-stu-id="070fc-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="070fc-113">Например, если значение элемента **коэффициента** — **винбио \_ типа \_ отпечатков пальцев**, структура **\_ \_ \_ сведений о расширенном подсистеме винбио** применяется к сканеру отпечатков пальцев и содержит соответствующие сведения в структуре **спеЦифк. отпечатков пальцев** .</span><span class="sxs-lookup"><span data-stu-id="070fc-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-114">**Specific**</span><span class="sxs-lookup"><span data-stu-id="070fc-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-115">Сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического модуля, связанного с конкретным биометрической метрикой.</span><span class="sxs-lookup"><span data-stu-id="070fc-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="070fc-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-117">Reserved.</span></span> <span data-ttu-id="070fc-118">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-119">**фаЦиалфеатурес**</span><span class="sxs-lookup"><span data-stu-id="070fc-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-120">Сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического модуля, связанного с функциями лиц.</span><span class="sxs-lookup"><span data-stu-id="070fc-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="070fc-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-122">Reserved.</span></span> <span data-ttu-id="070fc-123">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-124">**енроллментрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="070fc-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="070fc-125">**Null**</span><span class="sxs-lookup"><span data-stu-id="070fc-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-126">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-126">Reserved.</span></span> <span data-ttu-id="070fc-127">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="070fc-128">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="070fc-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-129">Сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического модуля, связанного с шаблонами отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="070fc-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="070fc-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-131">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-131">Reserved.</span></span> <span data-ttu-id="070fc-132">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-133">**енроллментрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="070fc-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-134">Количество хороших выборок, необходимых для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-135">**женералсамплес**</span><span class="sxs-lookup"><span data-stu-id="070fc-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-136">Общее число хороших выборок, необходимых для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-137">**Center**</span><span class="sxs-lookup"><span data-stu-id="070fc-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-138">Количество хороших выборок для центра отпечатка пальца, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-139">**топедже**</span><span class="sxs-lookup"><span data-stu-id="070fc-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-140">Число хороших выборок для верхнего края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-141">**боттомедже**</span><span class="sxs-lookup"><span data-stu-id="070fc-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-142">Число хороших выборок для нижнего края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-143">**лефтедже**</span><span class="sxs-lookup"><span data-stu-id="070fc-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-144">Число хороших выборок для левого края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-145">**ригхтедже**</span><span class="sxs-lookup"><span data-stu-id="070fc-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-146">Количество хороших выборок для правого края отпечатка, необходимого для создания нового шаблона отпечатка.</span><span class="sxs-lookup"><span data-stu-id="070fc-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="070fc-147">**IRI**</span><span class="sxs-lookup"><span data-stu-id="070fc-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-148">Сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического модуля, связанного с шаблонами IRI.</span><span class="sxs-lookup"><span data-stu-id="070fc-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="070fc-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-150">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-150">Reserved.</span></span> <span data-ttu-id="070fc-151">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-152">**енроллментрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="070fc-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="070fc-153">**Null**</span><span class="sxs-lookup"><span data-stu-id="070fc-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-154">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-154">Reserved.</span></span> <span data-ttu-id="070fc-155">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="070fc-156">**Голосовая связь**</span><span class="sxs-lookup"><span data-stu-id="070fc-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-157">Сведения о возможностях и требованиях к регистрации адаптера подсистемы для биометрического модуля, связанного с голосовыми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="070fc-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="070fc-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="070fc-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-159">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-159">Reserved.</span></span> <span data-ttu-id="070fc-160">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="070fc-161">**енроллментрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="070fc-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="070fc-162">**Null**</span><span class="sxs-lookup"><span data-stu-id="070fc-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="070fc-163">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="070fc-163">Reserved.</span></span> <span data-ttu-id="070fc-164">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="070fc-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="070fc-165">Требования</span><span class="sxs-lookup"><span data-stu-id="070fc-165">Requirements</span></span>



| <span data-ttu-id="070fc-166">Требование</span><span class="sxs-lookup"><span data-stu-id="070fc-166">Requirement</span></span> | <span data-ttu-id="070fc-167">Значение</span><span class="sxs-lookup"><span data-stu-id="070fc-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070fc-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="070fc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="070fc-169">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="070fc-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="070fc-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="070fc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="070fc-171">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="070fc-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="070fc-172">Header</span><span class="sxs-lookup"><span data-stu-id="070fc-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="070fc-173"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="070fc-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="070fc-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="070fc-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070fc-175">**\_Константы возможностей винбио**</span><span class="sxs-lookup"><span data-stu-id="070fc-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="070fc-176">**\_Константы БИОметрического \_ типа винбио**</span><span class="sxs-lookup"><span data-stu-id="070fc-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





