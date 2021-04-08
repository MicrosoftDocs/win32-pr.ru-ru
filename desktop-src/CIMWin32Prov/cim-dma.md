---
description: Класс CIM \_ DMA представляет архитектуру компьютера с прямым доступом к памяти (DMA).
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: Класс CIM_DMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990601"
---
# <a name="cim_dma-class"></a><span data-ttu-id="becee-103">\_Класс DMA CIM</span><span class="sxs-lookup"><span data-stu-id="becee-103">CIM\_DMA class</span></span>

<span data-ttu-id="becee-104">Класс **CIM \_ DMA** представляет архитектуру компьютера с прямым доступом к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="becee-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="becee-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="becee-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="becee-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="becee-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="becee-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="becee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="becee-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="becee-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="becee-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="becee-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="becee-110">Члены</span><span class="sxs-lookup"><span data-stu-id="becee-110">Members</span></span>

<span data-ttu-id="becee-111">Класс **\_ DMA CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="becee-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="becee-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="becee-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="becee-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="becee-113">Properties</span></span>

<span data-ttu-id="becee-114">Класс **CIM \_ DMA** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="becee-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="becee-115">**аддресссизе**</span><span class="sxs-lookup"><span data-stu-id="becee-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="becee-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="becee-119">Размер адреса канала DMA в битах.</span><span class="sxs-lookup"><span data-stu-id="becee-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="becee-120">Допустимые значения: 8, 16, 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="becee-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="becee-121">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="becee-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="becee-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="becee-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-123">(8)</span><span class="sxs-lookup"><span data-stu-id="becee-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-124">(16)</span><span class="sxs-lookup"><span data-stu-id="becee-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-125">(32)</span><span class="sxs-lookup"><span data-stu-id="becee-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-126">(64)</span><span class="sxs-lookup"><span data-stu-id="becee-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-127">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="becee-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="becee-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="becee-131">Доступность DMA.</span><span class="sxs-lookup"><span data-stu-id="becee-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="becee-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="becee-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="becee-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="becee-134">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="becee-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="becee-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (3)</span><span class="sxs-lookup"><span data-stu-id="becee-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="becee-136">Доступен.</span><span class="sxs-lookup"><span data-stu-id="becee-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="becee-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Используется/недоступно** (4)</span><span class="sxs-lookup"><span data-stu-id="becee-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="becee-138">Используется (недоступно).</span><span class="sxs-lookup"><span data-stu-id="becee-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="becee-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Используется и доступно, а совместное использование** (5)</span><span class="sxs-lookup"><span data-stu-id="becee-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="becee-140">Используется, но доступно (совместное использование).</span><span class="sxs-lookup"><span data-stu-id="becee-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-141">**бурстмоде**</span><span class="sxs-lookup"><span data-stu-id="becee-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="becee-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="becee-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="becee-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="becee-145">Если **значение — true**, канал DMA поддерживает пакетный режим.</span><span class="sxs-lookup"><span data-stu-id="becee-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="becee-146">**битемоде**</span><span class="sxs-lookup"><span data-stu-id="becee-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-149">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="becee-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="becee-150">Указывает, может ли DMA выполняться в режиме Count-to-Byte.</span><span class="sxs-lookup"><span data-stu-id="becee-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="becee-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="becee-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="becee-152">Другое</span><span class="sxs-lookup"><span data-stu-id="becee-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="becee-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="becee-154">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="becee-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="becee-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Не выполняется в режиме подсчета байтов** (3)</span><span class="sxs-lookup"><span data-stu-id="becee-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="becee-156">Невозможно выполнить в режиме подсчета по байтам.</span><span class="sxs-lookup"><span data-stu-id="becee-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="becee-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Выполнение в режиме "подсчета байта"** (4)</span><span class="sxs-lookup"><span data-stu-id="becee-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="becee-158">Возможность выполнения в режиме подсчета по байтам.</span><span class="sxs-lookup"><span data-stu-id="becee-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-159">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="becee-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="becee-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="becee-163">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="becee-163">Short textual description of the object.</span></span>

<span data-ttu-id="becee-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="becee-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="becee-165">**чаннелтиминг**</span><span class="sxs-lookup"><span data-stu-id="becee-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-168">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="becee-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="becee-169">Время канала DMA.</span><span class="sxs-lookup"><span data-stu-id="becee-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="becee-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="becee-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="becee-171">Другое</span><span class="sxs-lookup"><span data-stu-id="becee-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="becee-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="becee-173">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="becee-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="becee-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Совместимость с ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="becee-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="becee-175">Совместимость с ISA.</span><span class="sxs-lookup"><span data-stu-id="becee-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="becee-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Введите A** (4)</span><span class="sxs-lookup"><span data-stu-id="becee-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="becee-177">Введите A.</span><span class="sxs-lookup"><span data-stu-id="becee-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="becee-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Тип B** (5)</span><span class="sxs-lookup"><span data-stu-id="becee-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="becee-179">Тип B.</span><span class="sxs-lookup"><span data-stu-id="becee-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="becee-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Тип F** (6)</span><span class="sxs-lookup"><span data-stu-id="becee-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="becee-181">Введите F.</span><span class="sxs-lookup"><span data-stu-id="becee-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="becee-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-185">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="becee-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="becee-186">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="becee-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="becee-187">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="becee-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="becee-188">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="becee-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-191">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="becee-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="becee-192">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="becee-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="becee-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="becee-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-196">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="becee-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="becee-197">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="becee-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="becee-198">**Описание**</span><span class="sxs-lookup"><span data-stu-id="becee-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-201">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="becee-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="becee-202">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="becee-202">Textual description of the object.</span></span>

<span data-ttu-id="becee-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="becee-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="becee-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="becee-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="becee-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="becee-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-207">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="becee-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="becee-208">Номер канала DMA.</span><span class="sxs-lookup"><span data-stu-id="becee-208">DMA channel number.</span></span> <span data-ttu-id="becee-209">Это число является частью значения ключа объекта.</span><span class="sxs-lookup"><span data-stu-id="becee-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="becee-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="becee-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-211">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="becee-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="becee-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-213">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="becee-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="becee-214">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="becee-214">Date and time the object was installed.</span></span> <span data-ttu-id="becee-215">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="becee-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="becee-216">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="becee-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="becee-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="becee-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-218">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="becee-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="becee-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-220">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="becee-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="becee-221">Максимальное число байтов, которое может быть передано этим каналом DMA.</span><span class="sxs-lookup"><span data-stu-id="becee-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="becee-222">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="becee-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="becee-223">**Name**</span><span class="sxs-lookup"><span data-stu-id="becee-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-226">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="becee-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="becee-227">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="becee-227">Label by which the object is known.</span></span> <span data-ttu-id="becee-228">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="becee-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="becee-229">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="becee-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="becee-230">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="becee-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="becee-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="becee-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-233">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="becee-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="becee-234">Указывает текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="becee-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="becee-235">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="becee-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="becee-236">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="becee-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="becee-237">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="becee-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="becee-238">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="becee-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="becee-239">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="becee-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-240">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="becee-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="becee-241">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="becee-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="becee-242">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="becee-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="becee-243">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="becee-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="becee-244">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="becee-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="becee-245">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="becee-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="becee-246">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="becee-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="becee-247">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="becee-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="becee-248">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="becee-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-249">**трансфервидсс**</span><span class="sxs-lookup"><span data-stu-id="becee-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-250">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="becee-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="becee-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-252">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="becee-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="becee-253">Массив, указывающий все значения ширины передачи в битах, поддерживаемые этим каналом DMA.</span><span class="sxs-lookup"><span data-stu-id="becee-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="becee-254">Допустимые значения: 8, 16, 32, 64 и 128 бит.</span><span class="sxs-lookup"><span data-stu-id="becee-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="becee-255">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="becee-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="becee-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="becee-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-257">(8)</span><span class="sxs-lookup"><span data-stu-id="becee-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-258">(16)</span><span class="sxs-lookup"><span data-stu-id="becee-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-259">(32)</span><span class="sxs-lookup"><span data-stu-id="becee-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-260">(64)</span><span class="sxs-lookup"><span data-stu-id="becee-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="becee-261">(128)</span><span class="sxs-lookup"><span data-stu-id="becee-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-262">**типектиминг**</span><span class="sxs-lookup"><span data-stu-id="becee-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-263">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-265">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="becee-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="becee-266">Указывает, поддерживается ли синхронизация типа C (пакетная).</span><span class="sxs-lookup"><span data-stu-id="becee-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="becee-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="becee-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="becee-268">Другое</span><span class="sxs-lookup"><span data-stu-id="becee-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="becee-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="becee-270">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="becee-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="becee-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Совместимость с ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="becee-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="becee-272">Совместимость с ISA.</span><span class="sxs-lookup"><span data-stu-id="becee-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="becee-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (4)</span><span class="sxs-lookup"><span data-stu-id="becee-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="becee-274">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="becee-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="becee-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Поддерживается** (5)</span><span class="sxs-lookup"><span data-stu-id="becee-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="becee-276">Поддерживается.</span><span class="sxs-lookup"><span data-stu-id="becee-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="becee-277">**вордмоде**</span><span class="sxs-lookup"><span data-stu-id="becee-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becee-278">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="becee-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="becee-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="becee-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="becee-280">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="becee-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="becee-281">Указывает, можно ли выполнить DMA в режиме подсчета слов.</span><span class="sxs-lookup"><span data-stu-id="becee-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="becee-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="becee-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="becee-283">Другое</span><span class="sxs-lookup"><span data-stu-id="becee-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="becee-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="becee-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="becee-285">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="becee-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="becee-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Не выполняется в режиме "подсчета слов"** (3)</span><span class="sxs-lookup"><span data-stu-id="becee-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="becee-287">Невозможно выполнить в режиме подсчета слов.</span><span class="sxs-lookup"><span data-stu-id="becee-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="becee-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Выполнить в режиме "подсчета слов"** (4)</span><span class="sxs-lookup"><span data-stu-id="becee-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="becee-289">Возможность выполнения в режиме подсчета слов.</span><span class="sxs-lookup"><span data-stu-id="becee-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="becee-290">Комментарии</span><span class="sxs-lookup"><span data-stu-id="becee-290">Remarks</span></span>

<span data-ttu-id="becee-291">Класс **\_ DMA CIM** является производным от [**CIM \_ системресаурце**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="becee-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="becee-292">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="becee-292">WMI does not implement this class.</span></span> <span data-ttu-id="becee-293">Классы, производные от **CIM \_ DMA**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="becee-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="becee-294">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="becee-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="becee-295">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="becee-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="becee-296">Требования</span><span class="sxs-lookup"><span data-stu-id="becee-296">Requirements</span></span>



| <span data-ttu-id="becee-297">Требование</span><span class="sxs-lookup"><span data-stu-id="becee-297">Requirement</span></span> | <span data-ttu-id="becee-298">Значение</span><span class="sxs-lookup"><span data-stu-id="becee-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="becee-299">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="becee-299">Minimum supported client</span></span><br/> | <span data-ttu-id="becee-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="becee-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="becee-301">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="becee-301">Minimum supported server</span></span><br/> | <span data-ttu-id="becee-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="becee-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="becee-303">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="becee-303">Namespace</span></span><br/>                | <span data-ttu-id="becee-304">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="becee-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="becee-305">MOF</span><span class="sxs-lookup"><span data-stu-id="becee-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="becee-306"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="becee-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="becee-307">DLL</span><span class="sxs-lookup"><span data-stu-id="becee-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="becee-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="becee-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="becee-309">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="becee-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="becee-310">**\_СИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="becee-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

