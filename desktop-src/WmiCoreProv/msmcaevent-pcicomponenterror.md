---
description: Указывает на ошибку компонента PCI об архитектуре проверки компьютеров (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Класс MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702849"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="9c814-104">\_Класс мсмкаевент пЦикомпонентеррор</span><span class="sxs-lookup"><span data-stu-id="9c814-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="9c814-105">Класс **мсмкаевент \_ пЦикомпонентеррор** указывает на ошибку компонента PCI "архитектура проверки машин" (MCA).</span><span class="sxs-lookup"><span data-stu-id="9c814-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="9c814-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="9c814-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="9c814-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9c814-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9c814-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9c814-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c814-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c814-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="9c814-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9c814-110">Members</span></span>

<span data-ttu-id="9c814-111">Класс **мсмкаевент \_ пЦикомпонентеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c814-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="9c814-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c814-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c814-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c814-113">Properties</span></span>

<span data-ttu-id="9c814-114">Класс **мсмкаевент \_ пЦикомпонентеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c814-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c814-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="9c814-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c814-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9c814-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="9c814-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c814-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-122">Число дополнительных ошибок в записи.</span><span class="sxs-lookup"><span data-stu-id="9c814-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-123">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="9c814-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c814-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-126">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c814-126">CPU that reported the error.</span></span> <span data-ttu-id="9c814-127">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="9c814-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-128">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="9c814-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-131">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="9c814-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="9c814-132">Значение</span><span class="sxs-lookup"><span data-stu-id="9c814-132">Value</span></span>                                                                                                | <span data-ttu-id="9c814-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9c814-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9c814-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9c814-135">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="9c814-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9c814-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9c814-137">Аварий</span><span class="sxs-lookup"><span data-stu-id="9c814-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="9c814-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9c814-139">Исправимая</span><span class="sxs-lookup"><span data-stu-id="9c814-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c814-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9c814-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c814-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c814-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c814-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c814-144">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="9c814-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-145">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="9c814-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c814-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-148">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="9c814-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-149">**\_ \_ состояние ошибки соответствия \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="9c814-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-150">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c814-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-152">Код внутренней ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c814-152">Internal error code.</span></span>

<span data-ttu-id="9c814-153">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c814-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c814-154">**\_ \_ Буснумбер сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-155">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-157">Номер шины компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-158">**\_ \_ Класскодебасекласс сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-159">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-161">Код класса базового класса компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-162">**\_ \_ Класскодеинтерфаце сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-163">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-165">Интерфейс кода класса компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-166">**\_ \_ Класскодесубкласс сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-167">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-169">Подкласс кода класса компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-170">**Идентификатор устройства для \_ \_ сведений о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-171">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c814-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-173">Идентификатор устройства компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-174">**\_ \_ Девиценумбер сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-175">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-177">Номер устройства компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-178">**\_ \_ Функтионнумбер сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-179">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-181">Номер функции компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-182">**\_ \_ Сегментнумбер сведения о СОотношении PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-183">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-185">Номер сегмента компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-186">**\_ \_ ИД поставщика информации о соответствии PCI \_**</span><span class="sxs-lookup"><span data-stu-id="9c814-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c814-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-189">Идентификатор поставщика компонента PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-190">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="9c814-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-191">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9c814-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9c814-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-193">Массив байтов, содержащий необработанную запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c814-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="9c814-194">Число элементов в массиве, которое указывает свойство **size** .</span><span class="sxs-lookup"><span data-stu-id="9c814-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-195">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="9c814-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-196">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c814-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-198">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c814-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="9c814-199">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c814-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c814-200">**Размер**</span><span class="sxs-lookup"><span data-stu-id="9c814-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c814-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-203">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c814-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-204">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9c814-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c814-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-207">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="9c814-207">Type of event log message.</span></span> <span data-ttu-id="9c814-208">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="9c814-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="9c814-209">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="9c814-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c814-210">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c814-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c814-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c814-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c814-212">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="9c814-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="9c814-213">Значения</span><span class="sxs-lookup"><span data-stu-id="9c814-213">Values</span></span>                                                                               | <span data-ttu-id="9c814-214">Значение</span><span class="sxs-lookup"><span data-stu-id="9c814-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9c814-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="9c814-216">Состояние ошибки согласования PCI \_ \_ \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9c814-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="9c814-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="9c814-218">Сведения о соотношении PCI \_ \_ являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="9c814-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="9c814-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="9c814-220">\_ \_ Допустимый номер памяти для согласования PCI \_ .</span><span class="sxs-lookup"><span data-stu-id="9c814-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="9c814-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="9c814-222">\_ \_ \_ Допустимый номер операции ввода-вывода PCI.</span><span class="sxs-lookup"><span data-stu-id="9c814-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="9c814-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="9c814-224">\_ \_ \_ Пара данных регс \_ -сопоставлений PCI является допустимой.</span><span class="sxs-lookup"><span data-stu-id="9c814-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="9c814-225">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c814-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c814-226">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c814-226">Remarks</span></span>

<span data-ttu-id="9c814-227">Класс **мсмкаевент \_ пЦикомпонентеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="9c814-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c814-228">Требования</span><span class="sxs-lookup"><span data-stu-id="9c814-228">Requirements</span></span>



| <span data-ttu-id="9c814-229">Требование</span><span class="sxs-lookup"><span data-stu-id="9c814-229">Requirement</span></span> | <span data-ttu-id="9c814-230">Значение</span><span class="sxs-lookup"><span data-stu-id="9c814-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c814-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c814-231">Minimum supported client</span></span><br/> | <span data-ttu-id="9c814-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c814-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9c814-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c814-233">Minimum supported server</span></span><br/> | <span data-ttu-id="9c814-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c814-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9c814-235">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c814-235">Namespace</span></span><br/>                | <span data-ttu-id="9c814-236">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="9c814-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9c814-237">MOF</span><span class="sxs-lookup"><span data-stu-id="9c814-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c814-238"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c814-239">DLL</span><span class="sxs-lookup"><span data-stu-id="9c814-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c814-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c814-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c814-241">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c814-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c814-242">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="9c814-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9c814-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="9c814-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

