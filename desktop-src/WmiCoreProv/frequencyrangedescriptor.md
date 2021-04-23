---
description: Представляет контейнер для характеристик поддерживаемого диапазона частоты.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Класс Фрекуенциранжедескриптор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692273"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="6562f-103">Класс Фрекуенциранжедескриптор</span><span class="sxs-lookup"><span data-stu-id="6562f-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="6562f-104">Класс WMI **фрекуенциранжедескриптор** представляет контейнер для характеристик поддерживаемого диапазона частоты.</span><span class="sxs-lookup"><span data-stu-id="6562f-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="6562f-105">Экземпляры этого класса являются элементами массива **мониторфрекранжес** в [**вмимониторлистедфрекуенциранжес**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="6562f-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6562f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6562f-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="6562f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6562f-107">Members</span></span>

<span data-ttu-id="6562f-108">Класс **фрекуенциранжедескриптор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6562f-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="6562f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6562f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6562f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6562f-110">Properties</span></span>

<span data-ttu-id="6562f-111">Класс **фрекуенциранжедескриптор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6562f-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6562f-112">**активехеигхт**</span><span class="sxs-lookup"><span data-stu-id="6562f-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-115">Высота активного изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6562f-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-116">**активевидс**</span><span class="sxs-lookup"><span data-stu-id="6562f-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-119">Ширина (в пикселях) активного изображения.</span><span class="sxs-lookup"><span data-stu-id="6562f-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="6562f-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-123">Тип ограничения для диапазона частот.</span><span class="sxs-lookup"><span data-stu-id="6562f-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-124">**максхсинкденоминатор**</span><span class="sxs-lookup"><span data-stu-id="6562f-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-127">Максимальный делитель горизонтальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6562f-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-128">**максхсинкнумератор**</span><span class="sxs-lookup"><span data-stu-id="6562f-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-131">Максимальный числитель по горизонтальной синхронизации в килохертз (кГц).</span><span class="sxs-lookup"><span data-stu-id="6562f-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="6562f-132">**макспикселрате**</span><span class="sxs-lookup"><span data-stu-id="6562f-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-135">Максимальная пиксельная скорость в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="6562f-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="6562f-136">**максвсинкденоминатор**</span><span class="sxs-lookup"><span data-stu-id="6562f-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-139">Максимальный делитель вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6562f-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-140">**максвсинкнумератор**</span><span class="sxs-lookup"><span data-stu-id="6562f-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-143">Максимальный вертикальный числитель синхронизации в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="6562f-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="6562f-144">**минхсинкденоминатор**</span><span class="sxs-lookup"><span data-stu-id="6562f-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-147">Минимальный знаменатель горизонтальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6562f-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-148">**минхсинкнумератор**</span><span class="sxs-lookup"><span data-stu-id="6562f-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-151">Минимальный числитель по горизонтальной синхронизации в, килохертз (кГц).</span><span class="sxs-lookup"><span data-stu-id="6562f-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="6562f-152">**минвсинкденоминатор**</span><span class="sxs-lookup"><span data-stu-id="6562f-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-155">Минимальный знаменатель синхронизации по вертикали.</span><span class="sxs-lookup"><span data-stu-id="6562f-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="6562f-156">**минвсинкнумератор**</span><span class="sxs-lookup"><span data-stu-id="6562f-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6562f-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-159">Минимальный числитель синхронизации по вертикали, в герцах (Гц).</span><span class="sxs-lookup"><span data-stu-id="6562f-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="6562f-160">**Лета**</span><span class="sxs-lookup"><span data-stu-id="6562f-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6562f-161">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6562f-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6562f-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6562f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6562f-163">Лета.</span><span class="sxs-lookup"><span data-stu-id="6562f-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6562f-164">Требования</span><span class="sxs-lookup"><span data-stu-id="6562f-164">Requirements</span></span>



| <span data-ttu-id="6562f-165">Требование</span><span class="sxs-lookup"><span data-stu-id="6562f-165">Requirement</span></span> | <span data-ttu-id="6562f-166">Значение</span><span class="sxs-lookup"><span data-stu-id="6562f-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6562f-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6562f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="6562f-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6562f-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6562f-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6562f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="6562f-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6562f-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6562f-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6562f-171">Namespace</span></span><br/>                | <span data-ttu-id="6562f-172">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="6562f-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6562f-173">MOF</span><span class="sxs-lookup"><span data-stu-id="6562f-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6562f-174"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6562f-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6562f-175">DLL</span><span class="sxs-lookup"><span data-stu-id="6562f-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6562f-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6562f-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6562f-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6562f-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6562f-178">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="6562f-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




