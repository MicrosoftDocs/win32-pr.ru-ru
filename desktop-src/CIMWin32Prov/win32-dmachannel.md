---
description: '\_Класс WMI канал DMA для Win32 представляет канал прямого доступа к памяти (DMA) в компьютерной системе под Windows.'
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Класс Win32_DMAChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896274"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="f13e1-103">\_Класс Win32 канал DMA</span><span class="sxs-lookup"><span data-stu-id="f13e1-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="f13e1-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ канал DMA для Win32** представляет канал прямого доступа к памяти (DMA) в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="f13e1-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="f13e1-105">DMA — это метод перемещения данных с устройства в память (или наоборот) без помощи микропроцессора.</span><span class="sxs-lookup"><span data-stu-id="f13e1-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="f13e1-106">Системная плата использует контроллер DMA для работы с фиксированным количеством каналов, каждый из которых может использоваться одним (и только одним) устройством за раз.</span><span class="sxs-lookup"><span data-stu-id="f13e1-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="f13e1-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f13e1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f13e1-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f13e1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13e1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f13e1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="f13e1-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f13e1-110">Members</span></span>

<span data-ttu-id="f13e1-111">Класс **Win32 \_ канал DMA** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f13e1-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="f13e1-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f13e1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f13e1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f13e1-113">Properties</span></span>

<span data-ttu-id="f13e1-114">Класс **Win32 \_ канал DMA** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f13e1-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f13e1-115">**аддресссизе**</span><span class="sxs-lookup"><span data-stu-id="f13e1-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-119">Размер адреса канала DMA в битах.</span><span class="sxs-lookup"><span data-stu-id="f13e1-119">DMA channel address size in bits.</span></span> <span data-ttu-id="f13e1-120">Допустимые значения: 8, 16, 32 или 64 бит.</span><span class="sxs-lookup"><span data-stu-id="f13e1-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="f13e1-121">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f13e1-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="f13e1-122">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="f13e1-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="f13e1-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-124">(8)</span><span class="sxs-lookup"><span data-stu-id="f13e1-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-125">(16)</span><span class="sxs-lookup"><span data-stu-id="f13e1-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-126">(32)</span><span class="sxs-lookup"><span data-stu-id="f13e1-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-127">(64)</span><span class="sxs-lookup"><span data-stu-id="f13e1-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f13e1-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-132">Доступность DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-132">Availability of the DMA.</span></span> <span data-ttu-id="f13e1-133">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f13e1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f13e1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="f13e1-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (3)</span><span class="sxs-lookup"><span data-stu-id="f13e1-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="f13e1-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Используется/недоступно** (4)</span><span class="sxs-lookup"><span data-stu-id="f13e1-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-138">Используется или недоступно</span><span class="sxs-lookup"><span data-stu-id="f13e1-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="f13e1-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Используется и доступно, а совместное использование** (5)</span><span class="sxs-lookup"><span data-stu-id="f13e1-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-140">Используется и доступно, или совместное использование</span><span class="sxs-lookup"><span data-stu-id="f13e1-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-141">**бурстмоде**</span><span class="sxs-lookup"><span data-stu-id="f13e1-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f13e1-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-145">Указывает, поддерживает ли канал DMA пакетный режим.</span><span class="sxs-lookup"><span data-stu-id="f13e1-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="f13e1-146">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-147">**битемоде**</span><span class="sxs-lookup"><span data-stu-id="f13e1-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-150">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-151">Режим выполнения DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-151">DMA execution mode.</span></span>

<span data-ttu-id="f13e1-152">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f13e1-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f13e1-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="f13e1-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Не выполняется в режиме подсчета байтов** (3)</span><span class="sxs-lookup"><span data-stu-id="f13e1-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-156">Не выполняется в режиме подсчета байтов</span><span class="sxs-lookup"><span data-stu-id="f13e1-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="f13e1-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Выполнение в режиме "подсчета байта"** (4)</span><span class="sxs-lookup"><span data-stu-id="f13e1-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-158">Выполнение в режиме подсчета байтов</span><span class="sxs-lookup"><span data-stu-id="f13e1-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-159">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f13e1-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f13e1-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-163">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="f13e1-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="f13e1-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-165">**чаннелтиминг**</span><span class="sxs-lookup"><span data-stu-id="f13e1-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-168">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-169">Время канала DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-169">DMA channel timing.</span></span>

<span data-ttu-id="f13e1-170">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f13e1-171">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-172">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f13e1-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="f13e1-173">**Совместимость с ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="f13e1-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="f13e1-174">**Введите A** (4)</span><span class="sxs-lookup"><span data-stu-id="f13e1-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="f13e1-175">**Тип B** (5)</span><span class="sxs-lookup"><span data-stu-id="f13e1-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="f13e1-176">**Тип F** (6)</span><span class="sxs-lookup"><span data-stu-id="f13e1-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f13e1-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-180">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f13e1-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-181">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f13e1-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f13e1-182">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f13e1-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f13e1-183">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-184">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f13e1-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-187">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f13e1-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-188">Имя класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f13e1-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="f13e1-189">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f13e1-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-193">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f13e1-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-194">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="f13e1-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="f13e1-195">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-196">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f13e1-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-199">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f13e1-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-200">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f13e1-200">Description of the object.</span></span>

<span data-ttu-id="f13e1-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="f13e1-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f13e1-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-205">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-206">Номер канала DMA, часть значения ключа объекта.</span><span class="sxs-lookup"><span data-stu-id="f13e1-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="f13e1-207">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f13e1-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-209">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f13e1-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-211">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-212">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f13e1-212">Date and time the object was installed.</span></span> <span data-ttu-id="f13e1-213">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="f13e1-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f13e1-214">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="f13e1-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-216">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f13e1-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-218">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-219">Максимальное число байтов, которое может быть передано этим каналом DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="f13e1-220">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f13e1-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="f13e1-221">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-222">**Name**</span><span class="sxs-lookup"><span data-stu-id="f13e1-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-225">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f13e1-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-226">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f13e1-226">Label by which the object is known.</span></span> <span data-ttu-id="f13e1-227">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="f13e1-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f13e1-228">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-229">**порт**.</span><span class="sxs-lookup"><span data-stu-id="f13e1-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f13e1-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-232">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Structures \| [**\_ разделяемого \_ \_ дескриптора ресурсов**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| DMA \| Port")</span><span class="sxs-lookup"><span data-stu-id="f13e1-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-233">Порт DMA, используемый адаптером шины узла.</span><span class="sxs-lookup"><span data-stu-id="f13e1-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="f13e1-234">Это имеет смысл для шин MCA-Type.</span><span class="sxs-lookup"><span data-stu-id="f13e1-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="f13e1-235">Пример: 12</span><span class="sxs-lookup"><span data-stu-id="f13e1-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="f13e1-236">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f13e1-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f13e1-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-239">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f13e1-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-240">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f13e1-240">Current status of the object.</span></span> <span data-ttu-id="f13e1-241">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="f13e1-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f13e1-242">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="f13e1-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f13e1-243">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="f13e1-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f13e1-244">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="f13e1-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f13e1-245">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f13e1-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f13e1-246">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f13e1-247">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f13e1-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f13e1-248">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f13e1-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f13e1-249">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f13e1-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f13e1-250">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f13e1-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-251">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f13e1-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f13e1-252">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f13e1-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f13e1-253">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f13e1-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f13e1-254">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f13e1-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f13e1-255">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f13e1-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f13e1-256">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f13e1-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f13e1-257">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f13e1-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f13e1-258">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f13e1-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f13e1-259">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f13e1-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-260">**трансфервидсс**</span><span class="sxs-lookup"><span data-stu-id="f13e1-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-261">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f13e1-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-263">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-264">Массив всех значений ширины передачи (в битах), поддерживаемых этим каналом DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="f13e1-265">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f13e1-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="f13e1-266">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="f13e1-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="f13e1-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-268">(8)</span><span class="sxs-lookup"><span data-stu-id="f13e1-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-269">(16)</span><span class="sxs-lookup"><span data-stu-id="f13e1-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-270">(32)</span><span class="sxs-lookup"><span data-stu-id="f13e1-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-271">(64)</span><span class="sxs-lookup"><span data-stu-id="f13e1-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f13e1-272">(128)</span><span class="sxs-lookup"><span data-stu-id="f13e1-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-273">**типектиминг**</span><span class="sxs-lookup"><span data-stu-id="f13e1-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-274">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-276">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-277">Поддержка времени типа C (ускорения).</span><span class="sxs-lookup"><span data-stu-id="f13e1-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="f13e1-278">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f13e1-279">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-280">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f13e1-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="f13e1-281">**Совместимость с ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="f13e1-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f13e1-282">**Не поддерживается** (4)</span><span class="sxs-lookup"><span data-stu-id="f13e1-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="f13e1-283">**Поддерживается** (5)</span><span class="sxs-lookup"><span data-stu-id="f13e1-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f13e1-284">**вордмоде**</span><span class="sxs-lookup"><span data-stu-id="f13e1-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f13e1-285">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f13e1-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f13e1-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f13e1-287">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Данные DMA системных ресурсов DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="f13e1-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="f13e1-288">Режим выполнения DMA.</span><span class="sxs-lookup"><span data-stu-id="f13e1-288">DMA execution mode.</span></span>

<span data-ttu-id="f13e1-289">Это свойство наследуется [**от \_ канала передачи CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f13e1-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f13e1-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f13e1-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f13e1-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="f13e1-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Не выполняется в режиме "подсчета слов"** (3)</span><span class="sxs-lookup"><span data-stu-id="f13e1-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-293">Не выполняется в режиме подсчета слов</span><span class="sxs-lookup"><span data-stu-id="f13e1-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="f13e1-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Выполнить в режиме "подсчета слов"** (4)</span><span class="sxs-lookup"><span data-stu-id="f13e1-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f13e1-295">Выполнение в режиме подсчета слов</span><span class="sxs-lookup"><span data-stu-id="f13e1-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f13e1-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f13e1-296">Remarks</span></span>

<span data-ttu-id="f13e1-297">Класс **Win32 \_ канал DMA** является производным от [**\_ канала DMA CIM**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="f13e1-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f13e1-298">Требования</span><span class="sxs-lookup"><span data-stu-id="f13e1-298">Requirements</span></span>



| <span data-ttu-id="f13e1-299">Требование</span><span class="sxs-lookup"><span data-stu-id="f13e1-299">Requirement</span></span> | <span data-ttu-id="f13e1-300">Значение</span><span class="sxs-lookup"><span data-stu-id="f13e1-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f13e1-301">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f13e1-301">Minimum supported client</span></span><br/> | <span data-ttu-id="f13e1-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f13e1-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f13e1-303">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f13e1-303">Minimum supported server</span></span><br/> | <span data-ttu-id="f13e1-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f13e1-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f13e1-305">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f13e1-305">Namespace</span></span><br/>                | <span data-ttu-id="f13e1-306">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f13e1-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f13e1-307">MOF</span><span class="sxs-lookup"><span data-stu-id="f13e1-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f13e1-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f13e1-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f13e1-309">DLL</span><span class="sxs-lookup"><span data-stu-id="f13e1-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f13e1-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f13e1-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f13e1-311">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f13e1-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13e1-312">**канал передачи CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f13e1-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="f13e1-313">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="f13e1-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

