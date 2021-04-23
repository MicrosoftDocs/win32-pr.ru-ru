---
description: Представляет возможности и управление процессором.
ms.assetid: 70cf9776-eeda-42c2-90c4-704ecf1cdafe
title: Класс CIM_Processor (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.Role
- CIM_Processor.Family
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.UpgradeMethod
- CIM_Processor.MaxClockSpeed
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.AddressWidth
- CIM_Processor.LoadPercentage
- CIM_Processor.Stepping
- CIM_Processor.UniqueID
- CIM_Processor.CPUStatus
- CIM_Processor.ExternalBusClockSpeed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00e78834c0a3a782c5fdc48cd52a67b85aa2a241
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808381"
---
# <a name="cim_processor-class-hyper-v-management"></a><span data-ttu-id="7687a-103">Класс CIM_Processor (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7687a-103">CIM_Processor class (Hyper-V management)</span></span>

<span data-ttu-id="7687a-104">Представляет возможности и управление процессором.</span><span class="sxs-lookup"><span data-stu-id="7687a-104">Represents the capabilities and management of a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7687a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7687a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.1"), UMLPackagePath("CIM::Device::Processor"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  string Role;
  uint16 Family;
  string OtherFamilyDescription;
  uint16 UpgradeMethod;
  uint32 MaxClockSpeed;
  uint32 CurrentClockSpeed;
  uint16 DataWidth;
  uint16 AddressWidth;
  uint16 LoadPercentage;
  string Stepping;
  string UniqueID;
  uint16 CPUStatus;
  uint32 ExternalBusClockSpeed;
};
```

## <a name="members"></a><span data-ttu-id="7687a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7687a-106">Members</span></span>

<span data-ttu-id="7687a-107">Класс **\_ процессора CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7687a-107">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="7687a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="7687a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7687a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7687a-109">Properties</span></span>

<span data-ttu-id="7687a-110">Класс **\_ процессора CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7687a-110">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7687a-111">**аддрессвидс**</span><span class="sxs-lookup"><span data-stu-id="7687a-111">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), **Пунит** ("bit")</span><span class="sxs-lookup"><span data-stu-id="7687a-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-115">Ширина адреса процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="7687a-115">The processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-116">**кпустатус**</span><span class="sxs-lookup"><span data-stu-id="7687a-116">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7687a-119">Текущее состояние процессора.</span><span class="sxs-lookup"><span data-stu-id="7687a-119">The current status of the processor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7687a-120">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7687a-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Enabled"></span><span id="cpu_enabled"></span><span id="CPU_ENABLED"></span>

<span data-ttu-id="7687a-121">**ЦП включен** (1)</span><span class="sxs-lookup"><span data-stu-id="7687a-121">**CPU Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_by_User"></span><span id="cpu_disabled_by_user"></span><span id="CPU_DISABLED_BY_USER"></span>

<span data-ttu-id="7687a-122">**ЦП отключен пользователем** (2)</span><span class="sxs-lookup"><span data-stu-id="7687a-122">**CPU Disabled by User** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Disabled_By_BIOS__POST_Error_"></span><span id="cpu_disabled_by_bios__post_error_"></span><span id="CPU_DISABLED_BY_BIOS__POST_ERROR_"></span>

<span data-ttu-id="7687a-123">**ЦП отключен BIOS (Ошибка POST)** (3)</span><span class="sxs-lookup"><span data-stu-id="7687a-123">**CPU Disabled By BIOS (POST Error)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Is_Idle"></span><span id="cpu_is_idle"></span><span id="CPU_IS_IDLE"></span>

<span data-ttu-id="7687a-124">**ЦП бездействует** (4)</span><span class="sxs-lookup"><span data-stu-id="7687a-124">**CPU Is Idle** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7687a-125">**Другие** (7)</span><span class="sxs-lookup"><span data-stu-id="7687a-125">**Other** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7687a-126">**куррентклоккспид**</span><span class="sxs-lookup"><span data-stu-id="7687a-126">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7687a-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-129">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF- \| процессор \| 017,6 "), **Пунит** (" Герц \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="7687a-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.6"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-130">Текущая скорость процессора (в МГц).</span><span class="sxs-lookup"><span data-stu-id="7687a-130">The current speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-131">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="7687a-131">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-134">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), **Пунит** ("bit")</span><span class="sxs-lookup"><span data-stu-id="7687a-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-135">Ширина данных процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="7687a-135">The processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-136">**екстерналбусклоккспид**</span><span class="sxs-lookup"><span data-stu-id="7687a-136">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7687a-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-139">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц"), **Пунит** ("Герц \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="7687a-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-140">Скорость (в МГц) интерфейса внешней шины (также называемая интерфейсной шиной).</span><span class="sxs-lookup"><span data-stu-id="7687a-140">The speed, in MHz, of the external bus interface (also known as the front side bus).</span></span>

</dd> <dt>

<span data-ttu-id="7687a-141">**Семейство**</span><span class="sxs-lookup"><span data-stu-id="7687a-141">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -процессор 017,3 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Осерфамилидескриптион**")</span><span class="sxs-lookup"><span data-stu-id="7687a-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-145">Тип семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="7687a-145">The processor family type.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7687a-146">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7687a-146">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7687a-147">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7687a-147">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="7687a-148">**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="7687a-148">**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="7687a-149">**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="7687a-149">**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="7687a-150">**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="7687a-150">**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="7687a-151">**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="7687a-151">**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="7687a-152">**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="7687a-152">**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="7687a-153">**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="7687a-153">**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="7687a-154">**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="7687a-154">**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="7687a-155">**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="7687a-155">**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="7687a-156">**Торговая марка Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="7687a-156">**Pentium(R) brand** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="7687a-157">**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="7687a-157">**Pentium(R) Pro** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="7687a-158">**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="7687a-158">**Pentium(R) II** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="7687a-159">**Процессор Pentium (R) с технологией MMX (TM** ) (14)</span><span class="sxs-lookup"><span data-stu-id="7687a-159">**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="7687a-160">**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="7687a-160">**Celeron(TM)** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="7687a-161">**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="7687a-161">**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="7687a-162">**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="7687a-162">**Pentium(R) III** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="7687a-163">**Семейство M1** (18)</span><span class="sxs-lookup"><span data-stu-id="7687a-163">**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="7687a-164">**Семейство m2** (19)</span><span class="sxs-lookup"><span data-stu-id="7687a-164">**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__M_processor"></span><span id="intel_r__celeron_r__m_processor"></span><span id="INTEL_R__CELERON_R__M_PROCESSOR"></span>

<span data-ttu-id="7687a-165">**Процессор Intel (r) Celeron (r) M** (20)</span><span class="sxs-lookup"><span data-stu-id="7687a-165">**Intel(R) Celeron(R) M processor** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__4_HT_processor"></span><span id="intel_r__pentium_r__4_ht_processor"></span><span id="INTEL_R__PENTIUM_R__4_HT_PROCESSOR"></span>

<span data-ttu-id="7687a-166">**Процессор Intel (r) Pentium (r) 4 HT** (21)</span><span class="sxs-lookup"><span data-stu-id="7687a-166">**Intel(R) Pentium(R) 4 HT processor** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="7687a-167">**Семейство K5** (24)</span><span class="sxs-lookup"><span data-stu-id="7687a-167">**K5 Family** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="7687a-168">**Семейство K6** (25)</span><span class="sxs-lookup"><span data-stu-id="7687a-168">**K6 Family** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="7687a-169">**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="7687a-169">**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="7687a-170">**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="7687a-170">**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-171">**Семейство процессоров AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="7687a-171">**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="7687a-172">**Процессор AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="7687a-172">**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="7687a-173">**Семейство AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="7687a-173">**AMD29000 Family** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="7687a-174">**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="7687a-174">**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="7687a-175">**Семейство Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="7687a-175">**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="7687a-176">**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="7687a-176">**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="7687a-177">**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="7687a-177">**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="7687a-178">**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="7687a-178">**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="7687a-179">**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="7687a-179">**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="7687a-180">**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="7687a-180">**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="7687a-181">**Power PC X704** (38)</span><span class="sxs-lookup"><span data-stu-id="7687a-181">**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="7687a-182">**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="7687a-182">**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_processor"></span><span id="intel_r__core_tm__duo_processor"></span><span id="INTEL_R__CORE_TM__DUO_PROCESSOR"></span>

<span data-ttu-id="7687a-183">**Процессор Intel (R) Core (TM) Duo** (40)</span><span class="sxs-lookup"><span data-stu-id="7687a-183">**Intel(R) Core(TM) Duo processor** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Duo_mobile_processor"></span><span id="intel_r__core_tm__duo_mobile_processor"></span><span id="INTEL_R__CORE_TM__DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="7687a-184">**Процессор Intel (R) Core (TM) Duo для мобильных устройств** (41)</span><span class="sxs-lookup"><span data-stu-id="7687a-184">**Intel(R) Core(TM) Duo mobile processor** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_mobile_processor"></span><span id="intel_r__core_tm__solo_mobile_processor"></span><span id="INTEL_R__CORE_TM__SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="7687a-185">**Процессор Intel (R) Core (TM) solo для мобильных устройств** (42)</span><span class="sxs-lookup"><span data-stu-id="7687a-185">**Intel(R) Core(TM) Solo mobile processor** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Atom_TM__processor"></span><span id="intel_r__atom_tm__processor"></span><span id="INTEL_R__ATOM_TM__PROCESSOR"></span>

<span data-ttu-id="7687a-186">**Процессор Intel (R) Atom (TM)** (43)</span><span class="sxs-lookup"><span data-stu-id="7687a-186">**Intel(R) Atom(TM) processor** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="7687a-187">**Семейство Alpha** (48)</span><span class="sxs-lookup"><span data-stu-id="7687a-187">**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="7687a-188">**Альфа-21064** (49)</span><span class="sxs-lookup"><span data-stu-id="7687a-188">**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="7687a-189">**Альфа-21066** (50)</span><span class="sxs-lookup"><span data-stu-id="7687a-189">**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="7687a-190">**Альфа-21164** (51)</span><span class="sxs-lookup"><span data-stu-id="7687a-190">**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="7687a-191">**Альфа-21164PC** (52)</span><span class="sxs-lookup"><span data-stu-id="7687a-191">**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="7687a-192">**Альфа-21164a** (53)</span><span class="sxs-lookup"><span data-stu-id="7687a-192">**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="7687a-193">**Альфа-21264** (54)</span><span class="sxs-lookup"><span data-stu-id="7687a-193">**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="7687a-194">**Альфа-21364** (55)</span><span class="sxs-lookup"><span data-stu-id="7687a-194">**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Ultra_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_ultra_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_ULTRA_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-195">**Семейство процессоров AMD турион (TM) II Ultra Dual-Core Mobile M** (56)</span><span class="sxs-lookup"><span data-stu-id="7687a-195">**AMD Turion(TM) II Ultra Dual-Core Mobile M Processor Family** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_turion_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_TURION_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-196">**Семейство процессоров AMD турион (TM) II Dual-Core Mobile M** (57)</span><span class="sxs-lookup"><span data-stu-id="7687a-196">**AMD Turion(TM) II Dual-Core Mobile M Processor Family** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Dual-Core_Mobile_M_Processor_Family"></span><span id="amd_athlon_tm__ii_dual-core_mobile_m_processor_family"></span><span id="AMD_ATHLON_TM__II_DUAL-CORE_MOBILE_M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-197">**Семейство процессоров AMD Athlon (TM) II Dual-Core Mobile M** (58)</span><span class="sxs-lookup"><span data-stu-id="7687a-197">**AMD Athlon(TM) II Dual-Core Mobile M Processor Family** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__6100_Series_Processor"></span><span id="amd_opteron_tm__6100_series_processor"></span><span id="AMD_OPTERON_TM__6100_SERIES_PROCESSOR"></span>

<span data-ttu-id="7687a-198">**Процессор серии AMD Opteron (TM) 6100** (59)</span><span class="sxs-lookup"><span data-stu-id="7687a-198">**AMD Opteron(TM) 6100 Series Processor** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__4100_Series_Processor"></span><span id="amd_opteron_tm__4100_series_processor"></span><span id="AMD_OPTERON_TM__4100_SERIES_PROCESSOR"></span>

<span data-ttu-id="7687a-199">**Процессор серии AMD Opteron (TM) 4100** (60)</span><span class="sxs-lookup"><span data-stu-id="7687a-199">**AMD Opteron(TM) 4100 Series Processor** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="7687a-200">**Семейство MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="7687a-200">**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="7687a-201">**MIPS R4000** (65)</span><span class="sxs-lookup"><span data-stu-id="7687a-201">**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="7687a-202">**MIPS R4200** (66)</span><span class="sxs-lookup"><span data-stu-id="7687a-202">**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="7687a-203">**MIPS R4400** (67)</span><span class="sxs-lookup"><span data-stu-id="7687a-203">**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="7687a-204">**MIPS R4600** (68)</span><span class="sxs-lookup"><span data-stu-id="7687a-204">**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="7687a-205">**MIPS R10000** (69)</span><span class="sxs-lookup"><span data-stu-id="7687a-205">**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="7687a-206">**Семейство SPARC** (80)</span><span class="sxs-lookup"><span data-stu-id="7687a-206">**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="7687a-207">Очень **SPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="7687a-207">**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="7687a-208">**МИКРОSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="7687a-208">**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="7687a-209">**Микроsparc ииеп** (83)</span><span class="sxs-lookup"><span data-stu-id="7687a-209">**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="7687a-210">**Ултраспарк** (84)</span><span class="sxs-lookup"><span data-stu-id="7687a-210">**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="7687a-211">**УЛТРАСПАРК II** (85)</span><span class="sxs-lookup"><span data-stu-id="7687a-211">**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="7687a-212">**Ултраспарк III** (86)</span><span class="sxs-lookup"><span data-stu-id="7687a-212">**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="7687a-213">**УЛТРАСПАРК III** (87)</span><span class="sxs-lookup"><span data-stu-id="7687a-213">**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="7687a-214">**Ултраспарк ИИИИ** (88)</span><span class="sxs-lookup"><span data-stu-id="7687a-214">**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="7687a-215">**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="7687a-215">**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="7687a-216">**семейство 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="7687a-216">**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="7687a-217">**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="7687a-217">**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="7687a-218">**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="7687a-218">**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="7687a-219">**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="7687a-219">**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="7687a-220">**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="7687a-220">**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="7687a-221">**Семейство Хоббит** (112)</span><span class="sxs-lookup"><span data-stu-id="7687a-221">**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="7687a-222">**Семейство крусое (TM) TM5000** (120)</span><span class="sxs-lookup"><span data-stu-id="7687a-222">**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="7687a-223">**Семейство крусое (TM) TM3000** (121)</span><span class="sxs-lookup"><span data-stu-id="7687a-223">**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="7687a-224">**Семейство еффицеон (TM) TM8000** (122)</span><span class="sxs-lookup"><span data-stu-id="7687a-224">**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="7687a-225">**Веитек** (128)</span><span class="sxs-lookup"><span data-stu-id="7687a-225">**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="7687a-226">**Процессор Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="7687a-226">**Itanium(TM) Processor** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-227">**Семейство процессоров AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="7687a-227">**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Opteron_TM__Processor_Family"></span><span id="amd_opteron_tm__processor_family"></span><span id="AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-228">**Семейство процессоров AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="7687a-228">**AMD Opteron(TM) Processor Family** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__Processor_Family"></span><span id="amd_sempron_tm__processor_family"></span><span id="AMD_SEMPRON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-229">**Семейство процессоров AMD Семпрон (TM)** (133)</span><span class="sxs-lookup"><span data-stu-id="7687a-229">**AMD Sempron(TM) Processor Family** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_Mobile_Technology"></span><span id="amd_turion_tm__64_mobile_technology"></span><span id="AMD_TURION_TM__64_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="7687a-230">**Технология AMD турион (TM) 64 для мобильных устройств** (134)</span><span class="sxs-lookup"><span data-stu-id="7687a-230">**AMD Turion(TM) 64 Mobile Technology** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_AMD_Opteron_TM__Processor_Family"></span><span id="dual-core_amd_opteron_tm__processor_family"></span><span id="DUAL-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-231">**Семейство процессоров AMD Opteron (TM) с двумя ядрами** (135)</span><span class="sxs-lookup"><span data-stu-id="7687a-231">**Dual-Core AMD Opteron(TM) Processor Family** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__64_X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__64_x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__64_X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-232">**AMD Athlon (TM) 64 X2 Dual-Core семейство процессоров** (136)</span><span class="sxs-lookup"><span data-stu-id="7687a-232">**AMD Athlon(TM) 64 X2 Dual-Core Processor Family** (136)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__64_X2_Mobile_Technology"></span><span id="amd_turion_tm__64_x2_mobile_technology"></span><span id="AMD_TURION_TM__64_X2_MOBILE_TECHNOLOGY"></span>

<span data-ttu-id="7687a-233">**Технология AMD турион (TM) 64 с мобильными устройствами x2** (137)</span><span class="sxs-lookup"><span data-stu-id="7687a-233">**AMD Turion(TM) 64 X2 Mobile Technology** (137)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_AMD_Opteron_TM__Processor_Family"></span><span id="quad-core_amd_opteron_tm__processor_family"></span><span id="QUAD-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-234">**Семейство четырехъядерных процессоров AMD Opteron (TM)** (138)</span><span class="sxs-lookup"><span data-stu-id="7687a-234">**Quad-Core AMD Opteron(TM) Processor Family** (138)</span></span>


</dt> <dd></dd> <dt>

<span id="Third-Generation_AMD_Opteron_TM__Processor_Family"></span><span id="third-generation_amd_opteron_tm__processor_family"></span><span id="THIRD-GENERATION_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-235">**Семейство процессоров AMD Opteron (TM) третьего поколения** (139)</span><span class="sxs-lookup"><span data-stu-id="7687a-235">**Third-Generation AMD Opteron(TM) Processor Family** (139)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__FX_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__fx_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__FX_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-236">**Семейство процессоров AMD Phenom (TM) FX Quad-Core** (140)</span><span class="sxs-lookup"><span data-stu-id="7687a-236">**AMD Phenom(TM) FX Quad-Core Processor Family** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X4_Quad-Core_Processor_Family"></span><span id="amd_phenom_tm__x4_quad-core_processor_family"></span><span id="AMD_PHENOM_TM__X4_QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-237">**Семейство процессоров AMD Phenom (TM) X4 Quad-Core** (141)</span><span class="sxs-lookup"><span data-stu-id="7687a-237">**AMD Phenom(TM) X4 Quad-Core Processor Family** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_phenom_tm__x2_dual-core_processor_family"></span><span id="AMD_PHENOM_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-238">**AMD Phenom (TM) X2 Dual-Core семейство процессоров** (142)</span><span class="sxs-lookup"><span data-stu-id="7687a-238">**AMD Phenom(TM) X2 Dual-Core Processor Family** (142)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__X2_Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__x2_dual-core_processor_family"></span><span id="AMD_ATHLON_TM__X2_DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-239">**Семейство процессоров AMD Athlon (TM) X2 Dual-Core** (143)</span><span class="sxs-lookup"><span data-stu-id="7687a-239">**AMD Athlon(TM) X2 Dual-Core Processor Family** (143)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="7687a-240">**PA — семейство RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="7687a-240">**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="7687a-241">**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="7687a-241">**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="7687a-242">**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="7687a-242">**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="7687a-243">**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="7687a-243">**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="7687a-244">**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="7687a-244">**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="7687a-245">**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="7687a-245">**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="7687a-246">**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="7687a-246">**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="7687a-247">**Семейство V30** (160)</span><span class="sxs-lookup"><span data-stu-id="7687a-247">**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3200_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3200_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3200_SERIES"></span>

<span data-ttu-id="7687a-248">**Четырехъядерный процессор Intel (r) Xeon (r) серии 3200** (161)</span><span class="sxs-lookup"><span data-stu-id="7687a-248">**Quad-Core Intel(R) Xeon(R) processor 3200 Series** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3000_SERIES"></span>

<span data-ttu-id="7687a-249">**Двухъядерный процессор Intel (r) Xeon (r) 3000** (162)</span><span class="sxs-lookup"><span data-stu-id="7687a-249">**Dual-Core Intel(R) Xeon(R) processor 3000 Series** (162)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5300_SERIES"></span>

<span data-ttu-id="7687a-250">**Четырехъядерный процессор Intel (r) Xeon (r) серии 5300** (163)</span><span class="sxs-lookup"><span data-stu-id="7687a-250">**Quad-Core Intel(R) Xeon(R) processor 5300 Series** (163)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5100_SERIES"></span>

<span data-ttu-id="7687a-251">**Двухъядерный процессор Intel (r) Xeon (r) 5100** (164)</span><span class="sxs-lookup"><span data-stu-id="7687a-251">**Dual-Core Intel(R) Xeon(R) processor 5100 Series** (164)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5000_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5000_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5000_SERIES"></span>

<span data-ttu-id="7687a-252">**Двухъядерный процессор Intel (r) Xeon (r) 5000** (165)</span><span class="sxs-lookup"><span data-stu-id="7687a-252">**Dual-Core Intel(R) Xeon(R) processor 5000 Series** (165)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_LV"></span><span id="dual-core_intel_r__xeon_r__processor_lv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_LV"></span>

<span data-ttu-id="7687a-253">**Процессор с двумя ядрами Intel (r) Xeon (r) LV** (166)</span><span class="sxs-lookup"><span data-stu-id="7687a-253">**Dual-Core Intel(R) Xeon(R) processor LV** (166)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_ULV"></span><span id="dual-core_intel_r__xeon_r__processor_ulv"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_ULV"></span>

<span data-ttu-id="7687a-254">**Двухъядерный процессор Intel (r) Xeon (r)** (167)</span><span class="sxs-lookup"><span data-stu-id="7687a-254">**Dual-Core Intel(R) Xeon(R) processor ULV** (167)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7100_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7100_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7100_SERIES"></span>

<span data-ttu-id="7687a-255">**Двухъядерный процессор Intel (r) Xeon (r) 7100** (168)</span><span class="sxs-lookup"><span data-stu-id="7687a-255">**Dual-Core Intel(R) Xeon(R) processor 7100 Series** (168)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5400_SERIES"></span>

<span data-ttu-id="7687a-256">**Четырехъядерный процессор Intel (r) Xeon (r) серии 5400** (169)</span><span class="sxs-lookup"><span data-stu-id="7687a-256">**Quad-Core Intel(R) Xeon(R) processor 5400 Series** (169)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor"></span><span id="quad-core_intel_r__xeon_r__processor"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="7687a-257">**Четырехъядерный процессор Intel (r) Xeon (r** ) (170)</span><span class="sxs-lookup"><span data-stu-id="7687a-257">**Quad-Core Intel(R) Xeon(R) processor** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5200_SERIES"></span>

<span data-ttu-id="7687a-258">**Двухъядерный процессор Intel (r) Xeon (r) 5200** (171)</span><span class="sxs-lookup"><span data-stu-id="7687a-258">**Dual-Core Intel(R) Xeon(R) processor 5200 Series** (171)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7200_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7200_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7200_SERIES"></span>

<span data-ttu-id="7687a-259">**Двухъядерный процессор Intel (r) Xeon (r) 7200** (172)</span><span class="sxs-lookup"><span data-stu-id="7687a-259">**Dual-Core Intel(R) Xeon(R) processor 7200 Series** (172)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7300_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7300_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7300_SERIES"></span>

<span data-ttu-id="7687a-260">**Четырехъядерный процессор Intel (r) Xeon (r) серии 7300** (173)</span><span class="sxs-lookup"><span data-stu-id="7687a-260">**Quad-Core Intel(R) Xeon(R) processor 7300 Series** (173)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7400_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="7687a-261">**Четырехъядерный процессор Intel (r) Xeon (r) серии 7400** (174)</span><span class="sxs-lookup"><span data-stu-id="7687a-261">**Quad-Core Intel(R) Xeon(R) processor 7400 Series** (174)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7400_SERIES"></span>

<span data-ttu-id="7687a-262">**Процессор с несколькими ядрами Intel (r) Xeon (r) серии 7400** (175)</span><span class="sxs-lookup"><span data-stu-id="7687a-262">**Multi-Core Intel(R) Xeon(R) processor 7400 Series** (175)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="7687a-263">**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="7687a-263">**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="7687a-264">**Процессор Pentium (r) III с технологией Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="7687a-264">**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="7687a-265">**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="7687a-265">**Pentium(R) 4** (178)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="7687a-266">**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="7687a-266">**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd></dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="7687a-267">**Семейство AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="7687a-267">**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="7687a-268">**Процессор Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="7687a-268">**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__XP_Family"></span><span id="amd_athlon_tm__xp_family"></span><span id="AMD_ATHLON_TM__XP_FAMILY"></span>

<span data-ttu-id="7687a-269">**Семейство AMD Athlon (TM) XP** (182)</span><span class="sxs-lookup"><span data-stu-id="7687a-269">**AMD Athlon(TM) XP Family** (182)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__MP_Family"></span><span id="amd_athlon_tm__mp_family"></span><span id="AMD_ATHLON_TM__MP_FAMILY"></span>

<span data-ttu-id="7687a-270">**Семейство процессоров AMD Athlon (TM) MP** (183)</span><span class="sxs-lookup"><span data-stu-id="7687a-270">**AMD Athlon(TM) MP Family** (183)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="7687a-271">**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="7687a-271">**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__M_processor"></span><span id="intel_r__pentium_r__m_processor"></span><span id="INTEL_R__PENTIUM_R__M_PROCESSOR"></span>

<span data-ttu-id="7687a-272">**Процессор Intel (r) Pentium (r) M** (185)</span><span class="sxs-lookup"><span data-stu-id="7687a-272">**Intel(R) Pentium(R) M processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Celeron_R__D_processor"></span><span id="intel_r__celeron_r__d_processor"></span><span id="INTEL_R__CELERON_R__D_PROCESSOR"></span>

<span data-ttu-id="7687a-273">**Процессор Intel (r) Celeron (r) D** (186)</span><span class="sxs-lookup"><span data-stu-id="7687a-273">**Intel(R) Celeron(R) D processor** (186)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__D_processor"></span><span id="intel_r__pentium_r__d_processor"></span><span id="INTEL_R__PENTIUM_R__D_PROCESSOR"></span>

<span data-ttu-id="7687a-274">**Процессор Intel (r) Pentium (r) D** (187)</span><span class="sxs-lookup"><span data-stu-id="7687a-274">**Intel(R) Pentium(R) D processor** (187)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Pentium_R__Processor_Extreme_Edition"></span><span id="intel_r__pentium_r__processor_extreme_edition"></span><span id="INTEL_R__PENTIUM_R__PROCESSOR_EXTREME_EDITION"></span>

<span data-ttu-id="7687a-275">**Процессор Intel (r) Pentium (r) Extreme Edition** (188)</span><span class="sxs-lookup"><span data-stu-id="7687a-275">**Intel(R) Pentium(R) Processor Extreme Edition** (188)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__Solo_Processor"></span><span id="intel_r__core_tm__solo_processor"></span><span id="INTEL_R__CORE_TM__SOLO_PROCESSOR"></span>

<span data-ttu-id="7687a-276">**Процессор Intel (R) Core (TM) solo** (189)</span><span class="sxs-lookup"><span data-stu-id="7687a-276">**Intel(R) Core(TM) Solo Processor** (189)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="7687a-277">**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="7687a-277">**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_Processor"></span><span id="intel_r__core_tm_2_duo_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_PROCESSOR"></span>

<span data-ttu-id="7687a-278">**Процессор Intel (R) Core (TM) 2 Duo** (191)</span><span class="sxs-lookup"><span data-stu-id="7687a-278">**Intel(R) Core(TM)2 Duo Processor** (191)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_processor"></span><span id="intel_r__core_tm_2_solo_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_PROCESSOR"></span>

<span data-ttu-id="7687a-279">**Процессор Intel (R) Core (TM) 2 Solo** (192)</span><span class="sxs-lookup"><span data-stu-id="7687a-279">**Intel(R) Core(TM)2 Solo processor** (192)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_processor"></span><span id="intel_r__core_tm_2_extreme_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_PROCESSOR"></span>

<span data-ttu-id="7687a-280">**Процессор Intel (R) Core (TM) 2 Extreme** (193)</span><span class="sxs-lookup"><span data-stu-id="7687a-280">**Intel(R) Core(TM)2 Extreme processor** (193)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Quad_processor"></span><span id="intel_r__core_tm_2_quad_processor"></span><span id="INTEL_R__CORE_TM_2_QUAD_PROCESSOR"></span>

<span data-ttu-id="7687a-281">**Четырехъядерный процессор Intel (R) Core (TM) 2** (194)</span><span class="sxs-lookup"><span data-stu-id="7687a-281">**Intel(R) Core(TM)2 Quad processor** (194)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Extreme_mobile_processor"></span><span id="intel_r__core_tm_2_extreme_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_EXTREME_MOBILE_PROCESSOR"></span>

<span data-ttu-id="7687a-282">**Процессор Intel (R) Core (TM) 2 Extreme для мобильных устройств** (195)</span><span class="sxs-lookup"><span data-stu-id="7687a-282">**Intel(R) Core(TM)2 Extreme mobile processor** (195)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Duo_mobile_processor"></span><span id="intel_r__core_tm_2_duo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_DUO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="7687a-283">**Процессор Intel (R) Core (TM) 2 Duo для мобильных устройств** (196)</span><span class="sxs-lookup"><span data-stu-id="7687a-283">**Intel(R) Core(TM)2 Duo mobile processor** (196)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM_2_Solo_mobile_processor"></span><span id="intel_r__core_tm_2_solo_mobile_processor"></span><span id="INTEL_R__CORE_TM_2_SOLO_MOBILE_PROCESSOR"></span>

<span data-ttu-id="7687a-284">**Процессор Intel (R) Core (TM) 2 Solo для мобильных устройств** (197)</span><span class="sxs-lookup"><span data-stu-id="7687a-284">**Intel(R) Core(TM)2 Solo mobile processor** (197)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i7_processor"></span><span id="intel_r__core_tm__i7_processor"></span><span id="INTEL_R__CORE_TM__I7_PROCESSOR"></span>

<span data-ttu-id="7687a-285">**Процессор Intel (R) Core (TM) i7** (198)</span><span class="sxs-lookup"><span data-stu-id="7687a-285">**Intel(R) Core(TM) i7 processor** (198)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Celeron_R__Processor"></span><span id="dual-core_intel_r__celeron_r__processor"></span><span id="DUAL-CORE_INTEL_R__CELERON_R__PROCESSOR"></span>

<span data-ttu-id="7687a-286">**Процессор с двумя ядрами Intel (r) Celeron (r)** (199)</span><span class="sxs-lookup"><span data-stu-id="7687a-286">**Dual-Core Intel(R) Celeron(R) Processor** (199)</span></span>


</dt> <dd></dd> <dt>

<span id="S_390_and_zSeries_Family"></span><span id="s_390_and_zseries_family"></span><span id="S_390_AND_ZSERIES_FAMILY"></span>

<span data-ttu-id="7687a-287">**Семейство S/390 и зсериес** (200)</span><span class="sxs-lookup"><span data-stu-id="7687a-287">**S/390 and zSeries Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G4"></span><span id="esa_390_g4"></span>

<span data-ttu-id="7687a-288">**ESA/390 G4** (201)</span><span class="sxs-lookup"><span data-stu-id="7687a-288">**ESA/390 G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G5"></span><span id="esa_390_g5"></span>

<span data-ttu-id="7687a-289">**ESA/390 G5** (202)</span><span class="sxs-lookup"><span data-stu-id="7687a-289">**ESA/390 G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="ESA_390_G6"></span><span id="esa_390_g6"></span>

<span data-ttu-id="7687a-290">**ESA/390 G6** (203)</span><span class="sxs-lookup"><span data-stu-id="7687a-290">**ESA/390 G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architectur_base"></span><span id="z_architectur_base"></span><span id="Z_ARCHITECTUR_BASE"></span>

<span data-ttu-id="7687a-291">**основание z/арчитектур** (204)</span><span class="sxs-lookup"><span data-stu-id="7687a-291">**z/Architectur base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i5_processor"></span><span id="intel_r__core_tm__i5_processor"></span><span id="INTEL_R__CORE_TM__I5_PROCESSOR"></span>

<span data-ttu-id="7687a-292">**Процессор Intel (R) Core (TM) i5** (205)</span><span class="sxs-lookup"><span data-stu-id="7687a-292">**Intel(R) Core(TM) i5 processor** (205)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Core_TM__i3_processor"></span><span id="intel_r__core_tm__i3_processor"></span><span id="INTEL_R__CORE_TM__I3_PROCESSOR"></span>

<span data-ttu-id="7687a-293">**Процессор Intel (R) Core (TM) i3** (206)</span><span class="sxs-lookup"><span data-stu-id="7687a-293">**Intel(R) Core(TM) i3 processor** (206)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-M_Processor_Family"></span><span id="via_c7_tm_-m_processor_family"></span><span id="VIA_C7_TM_-M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-294">**Семейство процессоров VIA C7 (TM)-M** (210)</span><span class="sxs-lookup"><span data-stu-id="7687a-294">**VIA C7(TM)-M Processor Family** (210)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM_-D_Processor_Family"></span><span id="via_c7_tm_-d_processor_family"></span><span id="VIA_C7_TM_-D_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-295">**VIA C7 (TM)-D, семейство процессоров** (211)</span><span class="sxs-lookup"><span data-stu-id="7687a-295">**VIA C7(TM)-D Processor Family** (211)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_C7_TM__Processor_Family"></span><span id="via_c7_tm__processor_family"></span><span id="VIA_C7_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-296">**Семейство процессоров VIA C7 (TM)** (212)</span><span class="sxs-lookup"><span data-stu-id="7687a-296">**VIA C7(TM) Processor Family** (212)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Eden_TM__Processor_Family"></span><span id="via_eden_tm__processor_family"></span><span id="VIA_EDEN_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-297">**Семейство процессоров VIA Еден (TM)** (213)</span><span class="sxs-lookup"><span data-stu-id="7687a-297">**VIA Eden(TM) Processor Family** (213)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor"></span><span id="multi-core_intel_r__xeon_r__processor"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR"></span>

<span data-ttu-id="7687a-298">**Процессор с несколькими ядрами Intel (r) Xeon (r)** (214)</span><span class="sxs-lookup"><span data-stu-id="7687a-298">**Multi-Core Intel(R) Xeon(R) processor** (214)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="7687a-299">**Двухъядерный процессор Intel (r) Xeon (r) 3Xxx Series** (215)</span><span class="sxs-lookup"><span data-stu-id="7687a-299">**Dual-Core Intel(R) Xeon(R) processor 3xxx Series** (215)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_3xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_3xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_3XXX_SERIES"></span>

<span data-ttu-id="7687a-300">**Четырехъядерный процессор Intel (r) Xeon (r) серии 3xxx** (216)</span><span class="sxs-lookup"><span data-stu-id="7687a-300">**Quad-Core Intel(R) Xeon(R) processor 3xxx Series** (216)</span></span>


</dt> <dd></dd> <dt>

<span id="VIA_Nano_TM__Processor_Family"></span><span id="via_nano_tm__processor_family"></span><span id="VIA_NANO_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-301">**Семейство процессоров VIA Nano (TM)** (217)</span><span class="sxs-lookup"><span data-stu-id="7687a-301">**VIA Nano(TM) Processor Family** (217)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="7687a-302">**Двухъядерный процессор Intel (r) Xeon (r) 5Xxx Series** (218)</span><span class="sxs-lookup"><span data-stu-id="7687a-302">**Dual-Core Intel(R) Xeon(R) processor 5xxx Series** (218)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_5xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_5xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_5XXX_SERIES"></span>

<span data-ttu-id="7687a-303">**Четырехъядерный процессор Intel (r) Xeon (r) серии 5xxx** (219)</span><span class="sxs-lookup"><span data-stu-id="7687a-303">**Quad-Core Intel(R) Xeon(R) processor 5xxx Series** (219)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="dual-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="DUAL-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="7687a-304">**Двухъядерный процессор Intel (r) Xeon (r) 7Xxx Series** (221)</span><span class="sxs-lookup"><span data-stu-id="7687a-304">**Dual-Core Intel(R) Xeon(R) processor 7xxx Series** (221)</span></span>


</dt> <dd></dd> <dt>

<span id="Quad-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="quad-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="QUAD-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="7687a-305">**Четырехъядерный процессор Intel (r) Xeon (r) серии 7xxx** (222)</span><span class="sxs-lookup"><span data-stu-id="7687a-305">**Quad-Core Intel(R) Xeon(R) processor 7xxx Series** (222)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_7xxx_Series"></span><span id="multi-core_intel_r__xeon_r__processor_7xxx_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_7XXX_SERIES"></span>

<span data-ttu-id="7687a-306">**Многоядерный процессор Intel (r) Xeon (r) 7Xxx Series** (223)</span><span class="sxs-lookup"><span data-stu-id="7687a-306">**Multi-Core Intel(R) Xeon(R) processor 7xxx Series** (223)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Core_Intel_R__Xeon_R__processor_3400_Series"></span><span id="multi-core_intel_r__xeon_r__processor_3400_series"></span><span id="MULTI-CORE_INTEL_R__XEON_R__PROCESSOR_3400_SERIES"></span>

<span data-ttu-id="7687a-307">**Процессор с несколькими ядрами Intel (r) Xeon (r) серии 3400** (224)</span><span class="sxs-lookup"><span data-stu-id="7687a-307">**Multi-Core Intel(R) Xeon(R) processor 3400 Series** (224)</span></span>


</dt> <dd></dd> <dt>

<span id="Embedded_AMD_Opteron_TM__Quad-Core_Processor_Family"></span><span id="embedded_amd_opteron_tm__quad-core_processor_family"></span><span id="EMBEDDED_AMD_OPTERON_TM__QUAD-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-308">**Семейство встраиваемых процессоров AMD Opteron (TM) Quad-Core** (230)</span><span class="sxs-lookup"><span data-stu-id="7687a-308">**Embedded AMD Opteron(TM) Quad-Core Processor Family** (230)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__Triple-Core_Processor_Family"></span><span id="amd_phenom_tm__triple-core_processor_family"></span><span id="AMD_PHENOM_TM__TRIPLE-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-309">**Семейство процессоров AMD Phenom (TM) Triple-Core** (231)</span><span class="sxs-lookup"><span data-stu-id="7687a-309">**AMD Phenom(TM) Triple-Core Processor Family** (231)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Ultra_Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__ultra_dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__ULTRA_DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-310">**Семейство процессоров AMD турион (TM) Ultra Dual-Core Mobile** (232)</span><span class="sxs-lookup"><span data-stu-id="7687a-310">**AMD Turion(TM) Ultra Dual-Core Mobile Processor Family** (232)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Turion_TM__Dual-Core_Mobile_Processor_Family"></span><span id="amd_turion_tm__dual-core_mobile_processor_family"></span><span id="AMD_TURION_TM__DUAL-CORE_MOBILE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-311">**AMD турион (TM) Dual-Core семейство мобильных процессоров** (233)</span><span class="sxs-lookup"><span data-stu-id="7687a-311">**AMD Turion(TM) Dual-Core Mobile Processor Family** (233)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Dual-Core_Processor_Family"></span><span id="amd_athlon_tm__dual-core_processor_family"></span><span id="AMD_ATHLON_TM__DUAL-CORE_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-312">**Семейство процессоров AMD Athlon (TM) Dual-Core** (234)</span><span class="sxs-lookup"><span data-stu-id="7687a-312">**AMD Athlon(TM) Dual-Core Processor Family** (234)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__SI_Processor_Family"></span><span id="amd_sempron_tm__si_processor_family"></span><span id="AMD_SEMPRON_TM__SI_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-313">**Семейство процессоров AMD Семпрон (TM) Si** (235)</span><span class="sxs-lookup"><span data-stu-id="7687a-313">**AMD Sempron(TM) SI Processor Family** (235)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Phenom_TM__II_Processor_Family"></span><span id="amd_phenom_tm__ii_processor_family"></span><span id="AMD_PHENOM_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-314">**Семейство процессоров AMD Phenom (TM) II** (236)</span><span class="sxs-lookup"><span data-stu-id="7687a-314">**AMD Phenom(TM) II Processor Family** (236)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__II_Processor_Family"></span><span id="amd_athlon_tm__ii_processor_family"></span><span id="AMD_ATHLON_TM__II_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-315">**Семейство процессоров AMD Athlon (TM) II** (237)</span><span class="sxs-lookup"><span data-stu-id="7687a-315">**AMD Athlon(TM) II Processor Family** (237)</span></span>


</dt> <dd></dd> <dt>

<span id="Six-Core_AMD_Opteron_TM__Processor_Family"></span><span id="six-core_amd_opteron_tm__processor_family"></span><span id="SIX-CORE_AMD_OPTERON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-316">**Семейство процессоров AMD Opteron (TM) с шестью ядрами** (238)</span><span class="sxs-lookup"><span data-stu-id="7687a-316">**Six-Core AMD Opteron(TM) Processor Family** (238)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Sempron_TM__M_Processor_Family"></span><span id="amd_sempron_tm__m_processor_family"></span><span id="AMD_SEMPRON_TM__M_PROCESSOR_FAMILY"></span>

<span data-ttu-id="7687a-317">**Семейство процессоров AMD Семпрон (TM) M** (239)</span><span class="sxs-lookup"><span data-stu-id="7687a-317">**AMD Sempron(TM) M Processor Family** (239)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="7687a-318">**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="7687a-318">**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="7687a-319">Процессоры **i960** (251)</span><span class="sxs-lookup"><span data-stu-id="7687a-319">**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__SMBIOS_Extension_"></span><span id="reserved__smbios_extension_"></span><span id="RESERVED__SMBIOS_EXTENSION_"></span>

<span data-ttu-id="7687a-320">**Зарезервировано (расширение SMBIOS)** (254)</span><span class="sxs-lookup"><span data-stu-id="7687a-320">**Reserved (SMBIOS Extension)** (254)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Lo_"></span><span id="reserved__un-initialized_flash_content_-_lo_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_LO_"></span>

<span data-ttu-id="7687a-321">**Зарезервировано (с неинициализированным содержимым Flash)** (255)</span><span class="sxs-lookup"><span data-stu-id="7687a-321">**Reserved (Un-initialized Flash Content - Lo)** (255)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="7687a-322">**Sh-3** (260)</span><span class="sxs-lookup"><span data-stu-id="7687a-322">**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="7687a-323">**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="7687a-323">**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="7687a-324">**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="7687a-324">**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="7687a-325">**Стронгарм** (281)</span><span class="sxs-lookup"><span data-stu-id="7687a-325">**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="7687a-326">**6x86** (300)</span><span class="sxs-lookup"><span data-stu-id="7687a-326">**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="7687a-327">**Медиагкс** (301)</span><span class="sxs-lookup"><span data-stu-id="7687a-327">**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="7687a-328">**Мии** (302)</span><span class="sxs-lookup"><span data-stu-id="7687a-328">**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="7687a-329">**Винчип** (320)</span><span class="sxs-lookup"><span data-stu-id="7687a-329">**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="7687a-330">**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="7687a-330">**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="7687a-331">**Процессор видео** (500)</span><span class="sxs-lookup"><span data-stu-id="7687a-331">**Video Processor** (500)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__For_Future_Special_Purpose_Assignment_"></span><span id="reserved__for_future_special_purpose_assignment_"></span><span id="RESERVED__FOR_FUTURE_SPECIAL_PURPOSE_ASSIGNMENT_"></span>

<span data-ttu-id="7687a-332">**Зарезервировано (для будущего назначения специального назначения)** (65534)</span><span class="sxs-lookup"><span data-stu-id="7687a-332">**Reserved (For Future Special Purpose Assignment)** (65534)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved__Un-initialized_Flash_Content_-_Hi_"></span><span id="reserved__un-initialized_flash_content_-_hi_"></span><span id="RESERVED__UN-INITIALIZED_FLASH_CONTENT_-_HI_"></span>

<span data-ttu-id="7687a-333">**Зарезервировано (неинициализированное содержимое Flash — Hi)** (65535)</span><span class="sxs-lookup"><span data-stu-id="7687a-333">**Reserved (Un-initialized Flash Content - Hi)** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7687a-334">**лоадперцентаже**</span><span class="sxs-lookup"><span data-stu-id="7687a-334">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-335">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-337">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент"), [**датчик**](/windows/desktop/WmiSdk/standard-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрпроцессорлоад "), **Пунит** (" Percent ")</span><span class="sxs-lookup"><span data-stu-id="7687a-337">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-338">Загрузка процессора, усредненная за последнюю минуту, в процентах.</span><span class="sxs-lookup"><span data-stu-id="7687a-338">The loading of the processor, averaged over the last minute, as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-339">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="7687a-339">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-340">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7687a-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-342">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF- \| процессор \| 017,5 "), **Пунит** (" Герц \* 10 ^ 6 ")</span><span class="sxs-lookup"><span data-stu-id="7687a-342">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.5"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-343">Максимальная скорость процессора (в МГц).</span><span class="sxs-lookup"><span data-stu-id="7687a-343">The maximum speed, in MHz, of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-344">**осерфамилидескриптион**</span><span class="sxs-lookup"><span data-stu-id="7687a-344">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7687a-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-347">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="7687a-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-348">Тип семейства процессоров, если свойство **Family** имеет значение **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="7687a-348">The processor family type when the **Family** property is set to **Other** ("1").</span></span> <span data-ttu-id="7687a-349">Для этой строки следует задать значение NULL, если свойство Family имеет любое значение, отличное от **other**.</span><span class="sxs-lookup"><span data-stu-id="7687a-349">This string should be set to NULL when the Family property is any value other than **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-350">**Роль**</span><span class="sxs-lookup"><span data-stu-id="7687a-350">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7687a-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7687a-353">Роль процессора, например "Центральный процессор" или "математический процессор".</span><span class="sxs-lookup"><span data-stu-id="7687a-353">The role of the processor, for example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="7687a-354">**Отладка по шагам**</span><span class="sxs-lookup"><span data-stu-id="7687a-354">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7687a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-357">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="7687a-357">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-358">Уровень редакции процессора в семействе процессоров.</span><span class="sxs-lookup"><span data-stu-id="7687a-358">The revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-359">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="7687a-359">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7687a-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7687a-362">Глобальный уникальный идентификатор процессора в области семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="7687a-362">A globally unique identifier for the processor, within the scope of the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="7687a-363">**упградемесод**</span><span class="sxs-lookup"><span data-stu-id="7687a-363">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7687a-364">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7687a-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7687a-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7687a-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7687a-366">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -процессор 017,7 ")</span><span class="sxs-lookup"><span data-stu-id="7687a-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|017.7")</span></span>
</dt> </dl>

<span data-ttu-id="7687a-367">Сведения о сокете ЦП, которые содержат данные о том, как можно обновить процессор.</span><span class="sxs-lookup"><span data-stu-id="7687a-367">The CPU socket information that includes data on how the processor can be upgraded.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7687a-368">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7687a-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7687a-369">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7687a-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="7687a-370">**Дочерняя плата** (3)</span><span class="sxs-lookup"><span data-stu-id="7687a-370">**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="7687a-371">**Сокет ЗИФ** (4)</span><span class="sxs-lookup"><span data-stu-id="7687a-371">**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="7687a-372">**Замена/свинка назад** (5)</span><span class="sxs-lookup"><span data-stu-id="7687a-372">**Replacement/Piggy Back** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="7687a-373">**Нет** (6)</span><span class="sxs-lookup"><span data-stu-id="7687a-373">**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="7687a-374">**Сокет Лиф** (7)</span><span class="sxs-lookup"><span data-stu-id="7687a-374">**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="7687a-375">**Слот 1** (8)</span><span class="sxs-lookup"><span data-stu-id="7687a-375">**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="7687a-376">**Слот 2** (9)</span><span class="sxs-lookup"><span data-stu-id="7687a-376">**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="7687a-377">**370-контактный разъем** (10)</span><span class="sxs-lookup"><span data-stu-id="7687a-377">**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="7687a-378">**Слот A** (11)</span><span class="sxs-lookup"><span data-stu-id="7687a-378">**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="7687a-379">**Гнездо M** (12)</span><span class="sxs-lookup"><span data-stu-id="7687a-379">**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="7687a-380">**Сокет 423** (13)</span><span class="sxs-lookup"><span data-stu-id="7687a-380">**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="7687a-381">**Сокет A (сокет 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="7687a-381">**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="7687a-382">**Сокет 478** (15)</span><span class="sxs-lookup"><span data-stu-id="7687a-382">**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="7687a-383">**Сокет 754** (16)</span><span class="sxs-lookup"><span data-stu-id="7687a-383">**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="7687a-384">**Сокет 940** (17)</span><span class="sxs-lookup"><span data-stu-id="7687a-384">**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="7687a-385">**Сокет 939** (18)</span><span class="sxs-lookup"><span data-stu-id="7687a-385">**Socket 939** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_mPGA604"></span><span id="socket_mpga604"></span><span id="SOCKET_MPGA604"></span>

<span data-ttu-id="7687a-386">**Сокет mPGA604** (19)</span><span class="sxs-lookup"><span data-stu-id="7687a-386">**Socket mPGA604** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA771"></span><span id="socket_lga771"></span><span id="SOCKET_LGA771"></span>

<span data-ttu-id="7687a-387">**Сокет LGA771** (20)</span><span class="sxs-lookup"><span data-stu-id="7687a-387">**Socket LGA771** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA775"></span><span id="socket_lga775"></span><span id="SOCKET_LGA775"></span>

<span data-ttu-id="7687a-388">**Сокет LGA775** (21)</span><span class="sxs-lookup"><span data-stu-id="7687a-388">**Socket LGA775** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_S1"></span><span id="socket_s1"></span><span id="SOCKET_S1"></span>

<span data-ttu-id="7687a-389">**Сокет S1** (22)</span><span class="sxs-lookup"><span data-stu-id="7687a-389">**Socket S1** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM2"></span><span id="socket_am2"></span><span id="SOCKET_AM2"></span>

<span data-ttu-id="7687a-390">**AM2 сокета** (23)</span><span class="sxs-lookup"><span data-stu-id="7687a-390">**Socket AM2** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_F__1207_"></span><span id="socket_f__1207_"></span><span id="SOCKET_F__1207_"></span>

<span data-ttu-id="7687a-391">**Сокет F (1207)** (24)</span><span class="sxs-lookup"><span data-stu-id="7687a-391">**Socket F (1207)** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1366"></span><span id="socket_lga1366"></span><span id="SOCKET_LGA1366"></span>

<span data-ttu-id="7687a-392">**Сокет LGA1366** (25)</span><span class="sxs-lookup"><span data-stu-id="7687a-392">**Socket LGA1366** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_G34"></span><span id="socket_g34"></span><span id="SOCKET_G34"></span>

<span data-ttu-id="7687a-393">**G34 сокета** (26)</span><span class="sxs-lookup"><span data-stu-id="7687a-393">**Socket G34** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_AM3"></span><span id="socket_am3"></span><span id="SOCKET_AM3"></span>

<span data-ttu-id="7687a-394">**Сокет AM3** (27)</span><span class="sxs-lookup"><span data-stu-id="7687a-394">**Socket AM3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_C32"></span><span id="socket_c32"></span><span id="SOCKET_C32"></span>

<span data-ttu-id="7687a-395">**Сокет C32** (28)</span><span class="sxs-lookup"><span data-stu-id="7687a-395">**Socket C32** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1156"></span><span id="socket_lga1156"></span><span id="SOCKET_LGA1156"></span>

<span data-ttu-id="7687a-396">**Сокет LGA1156** (29)</span><span class="sxs-lookup"><span data-stu-id="7687a-396">**Socket LGA1156** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_LGA1567"></span><span id="socket_lga1567"></span><span id="SOCKET_LGA1567"></span>

<span data-ttu-id="7687a-397">**LGA1567 сокета** (30)</span><span class="sxs-lookup"><span data-stu-id="7687a-397">**Socket LGA1567** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_PGA988A"></span><span id="socket_pga988a"></span><span id="SOCKET_PGA988A"></span>

<span data-ttu-id="7687a-398">**Сокет PGA988A** (31)</span><span class="sxs-lookup"><span data-stu-id="7687a-398">**Socket PGA988A** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_BGA1288"></span><span id="socket_bga1288"></span><span id="SOCKET_BGA1288"></span>

<span data-ttu-id="7687a-399">**Сокет BGA1288** (32)</span><span class="sxs-lookup"><span data-stu-id="7687a-399">**Socket BGA1288** (32)</span></span>


<span data-ttu-id="7687a-400"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7687a-400"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7687a-401">Требования</span><span class="sxs-lookup"><span data-stu-id="7687a-401">Requirements</span></span>



| <span data-ttu-id="7687a-402">Требование</span><span class="sxs-lookup"><span data-stu-id="7687a-402">Requirement</span></span> | <span data-ttu-id="7687a-403">Значение</span><span class="sxs-lookup"><span data-stu-id="7687a-403">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7687a-404">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7687a-404">Minimum supported client</span></span><br/> | <span data-ttu-id="7687a-405">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7687a-405">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7687a-406">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7687a-406">Minimum supported server</span></span><br/> | <span data-ttu-id="7687a-407">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7687a-407">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7687a-408">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7687a-408">Namespace</span></span><br/>                | <span data-ttu-id="7687a-409">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7687a-409">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7687a-410">MOF</span><span class="sxs-lookup"><span data-stu-id="7687a-410">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7687a-411"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7687a-411"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7687a-412">DLL</span><span class="sxs-lookup"><span data-stu-id="7687a-412">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7687a-413"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7687a-413"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7687a-414">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7687a-414">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7687a-415">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="7687a-415">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

