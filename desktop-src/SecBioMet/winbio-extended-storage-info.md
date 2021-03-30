---
title: Структура WINBIO_EXTENDED_STORAGE_INFO (Винбио \_ types. h)
description: Содержит сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического блока.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- API структуры WINBIO_EXTENDED_STORAGE_INFO биометрическая платформа Windows
- PWINBIO_EXTENDED_STORAGE_INFO API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988300"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="e46cd-105">\_ \_ \_ Структура сведений о РАСШИРЕНном хранилище винбио</span><span class="sxs-lookup"><span data-stu-id="e46cd-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="e46cd-106">Содержит сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического блока.</span><span class="sxs-lookup"><span data-stu-id="e46cd-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="e46cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e46cd-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="e46cd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e46cd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-109">**женериксторажекапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e46cd-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-110">Универсальные возможности компонента хранилища, подключенного к определенному биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="e46cd-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="e46cd-111">**Фактор**</span><span class="sxs-lookup"><span data-stu-id="e46cd-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-112">Тип биометрического блока, для которого эта структура содержит сведения о возможностях и требованиях к регистрации адаптера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e46cd-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="e46cd-113">Например, если значение элемента **коэффициента** — **винбио \_ типа " \_ отпечаток**", **Структура \_ \_ \_ сведений о расширенном хранилище винбио** применяется к сканеру отпечатков пальцев и содержит соответствующие сведения в структуре **спеЦифк. отпечатков пальцев** .</span><span class="sxs-lookup"><span data-stu-id="e46cd-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e46cd-114">**Specific**</span><span class="sxs-lookup"><span data-stu-id="e46cd-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-115">Сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического модуля, связанного с конкретным биометрической метрикой.</span><span class="sxs-lookup"><span data-stu-id="e46cd-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="e46cd-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e46cd-117">Reserved.</span></span> <span data-ttu-id="e46cd-118">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e46cd-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e46cd-119">**фаЦиалфеатурес**</span><span class="sxs-lookup"><span data-stu-id="e46cd-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-120">Сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического модуля, связанного с функциями лиц.</span><span class="sxs-lookup"><span data-stu-id="e46cd-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e46cd-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-122">Возможности распознавания лиц компонента хранилища, подключенного к определенному биометрической единице.</span><span class="sxs-lookup"><span data-stu-id="e46cd-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e46cd-123">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="e46cd-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-124">Сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического модуля, связанного с шаблонами отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="e46cd-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-125">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e46cd-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-126">Возможности распознавания отпечатков пальцев компонента хранилища, подключенного к определенной биометрической единице</span><span class="sxs-lookup"><span data-stu-id="e46cd-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e46cd-127">**IRI**</span><span class="sxs-lookup"><span data-stu-id="e46cd-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-128">Сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического модуля, связанного с шаблонами IRI.</span><span class="sxs-lookup"><span data-stu-id="e46cd-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-129">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e46cd-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-130">Возможности распознавания IRI компонента хранилища, подключенного к определенной биометрической единице</span><span class="sxs-lookup"><span data-stu-id="e46cd-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e46cd-131">**Голосовая связь**</span><span class="sxs-lookup"><span data-stu-id="e46cd-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-132">Сведения о возможностях и требованиях к регистрации адаптера хранилища для биометрического модуля, связанного с голосовыми шаблонами.</span><span class="sxs-lookup"><span data-stu-id="e46cd-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e46cd-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e46cd-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e46cd-134">Возможности распознавания речи компонента хранилища, подключенного к определенной биометрической единице</span><span class="sxs-lookup"><span data-stu-id="e46cd-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e46cd-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e46cd-135">Requirements</span></span>



| <span data-ttu-id="e46cd-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e46cd-136">Requirement</span></span> | <span data-ttu-id="e46cd-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e46cd-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e46cd-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e46cd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e46cd-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e46cd-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e46cd-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e46cd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e46cd-141">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e46cd-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="e46cd-142">Header</span><span class="sxs-lookup"><span data-stu-id="e46cd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e46cd-143"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="e46cd-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e46cd-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e46cd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e46cd-145">**\_Константы БИОметрического \_ типа винбио**</span><span class="sxs-lookup"><span data-stu-id="e46cd-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="e46cd-146">**\_Константы возможностей винбио**</span><span class="sxs-lookup"><span data-stu-id="e46cd-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





