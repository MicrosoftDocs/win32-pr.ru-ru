---
description: Представляет ошибку шины PCI архитектуры MCA. Этот класс доступен только для компьютеров, работающих в 64-разрядной операционной системе Windows.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Класс MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809688"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="3c387-104">\_Класс мсмкаевент пЦибусеррор</span><span class="sxs-lookup"><span data-stu-id="3c387-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="3c387-105">Класс **мсмкаевент \_ пЦибусеррор** представляет ошибку шины PCI архитектуры MCA.</span><span class="sxs-lookup"><span data-stu-id="3c387-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="3c387-106">Этот класс доступен только для компьютеров, работающих в 64-разрядной операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="3c387-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="3c387-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c387-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3c387-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="3c387-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c387-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c387-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="3c387-110">Члены</span><span class="sxs-lookup"><span data-stu-id="3c387-110">Members</span></span>

<span data-ttu-id="3c387-111">Класс **мсмкаевент \_ пЦибусеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c387-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="3c387-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c387-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c387-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c387-113">Properties</span></span>

<span data-ttu-id="3c387-114">Класс **мсмкаевент \_ пЦибусеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c387-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c387-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="3c387-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c387-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3c387-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="3c387-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c387-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-122">Число дополнительных ошибок в записи.</span><span class="sxs-lookup"><span data-stu-id="3c387-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-123">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="3c387-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c387-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-126">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c387-126">CPU that reported the error.</span></span> <span data-ttu-id="3c387-127">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="3c387-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-128">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="3c387-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c387-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-131">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="3c387-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="3c387-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-132">Value</span></span>                                                                                                | <span data-ttu-id="3c387-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3c387-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3c387-135">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="3c387-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="3c387-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3c387-137">Аварий</span><span class="sxs-lookup"><span data-stu-id="3c387-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="3c387-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3c387-139">Исправимая</span><span class="sxs-lookup"><span data-stu-id="3c387-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c387-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="3c387-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c387-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c387-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c387-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c387-144">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="3c387-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-145">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="3c387-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c387-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-148">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="3c387-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-149">**\_адрес шины \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="3c387-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-150">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-152">Память или адрес ввода-вывода на шине PCI во время события.</span><span class="sxs-lookup"><span data-stu-id="3c387-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="3c387-153">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-154">**\_cmd шины \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="3c387-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-155">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-157">Команда или операция шины во время события.</span><span class="sxs-lookup"><span data-stu-id="3c387-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="3c387-158">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-159">**\_данные шины \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="3c387-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-160">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-162">Данные на шине PCI во время события.</span><span class="sxs-lookup"><span data-stu-id="3c387-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="3c387-163">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-164">**\_ \_ состояние ошибки шины \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="3c387-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-165">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-167">Состояние шины во время ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c387-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="3c387-168">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-169">**\_ \_ тип ошибки шины \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="3c387-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-170">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c387-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-172">Тип ошибки шины PCI.</span><span class="sxs-lookup"><span data-stu-id="3c387-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="3c387-173">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-173">Value</span></span>                                                                                                | <span data-ttu-id="3c387-174">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3c387-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3c387-176">Неизвестная или OEM-ошибка, специфичная для системы.</span><span class="sxs-lookup"><span data-stu-id="3c387-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="3c387-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3c387-178">Ошибка четности данных.</span><span class="sxs-lookup"><span data-stu-id="3c387-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="3c387-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3c387-180">Системная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c387-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="3c387-181"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3c387-182">Прекращение работы мастера.</span><span class="sxs-lookup"><span data-stu-id="3c387-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="3c387-183"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3c387-184">Истекло время ожидания шины или отсутствует устройство (нет ДЕВСЕЛ \# ).</span><span class="sxs-lookup"><span data-stu-id="3c387-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="3c387-185"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="3c387-186">Ошибка четности основных данных.</span><span class="sxs-lookup"><span data-stu-id="3c387-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="3c387-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="3c387-188">Ошибка четности адреса.</span><span class="sxs-lookup"><span data-stu-id="3c387-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="3c387-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="3c387-190">Ошибка четности команды.</span><span class="sxs-lookup"><span data-stu-id="3c387-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="3c387-191">**\_Идентификатор шины \_ PCI \_ буснумбер**</span><span class="sxs-lookup"><span data-stu-id="3c387-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-192">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c387-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-194">Назначенный идентификатор шины PCI, в которой произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c387-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-195">**\_Идентификатор шины \_ PCI \_ сегментнумбер**</span><span class="sxs-lookup"><span data-stu-id="3c387-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-196">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c387-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-198">Назначенный идентификатор сегмента шины PCI, в которой произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c387-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-199">**\_ \_ идентификатор запрашивающей стороны шины PCI \_**</span><span class="sxs-lookup"><span data-stu-id="3c387-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-200">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-202">Идентификатор запрашивающей стороны шины PCI во время события.</span><span class="sxs-lookup"><span data-stu-id="3c387-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="3c387-203">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-204">**\_ \_ идентификатор отвечающего устройства шины PCI \_**</span><span class="sxs-lookup"><span data-stu-id="3c387-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-205">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-207">Идентификатор респондента шины PCI во время события.</span><span class="sxs-lookup"><span data-stu-id="3c387-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="3c387-208">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-209">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="3c387-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-210">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c387-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3c387-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-212">Массив байтов, содержащий необработанную запись об ошибке, представленную в Windows уровнем абстрагирования системы (SAL).</span><span class="sxs-lookup"><span data-stu-id="3c387-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="3c387-213">Число элементов в массиве задается свойством **size** .</span><span class="sxs-lookup"><span data-stu-id="3c387-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-214">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="3c387-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-215">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-217">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c387-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="3c387-218">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c387-219">**Размер**</span><span class="sxs-lookup"><span data-stu-id="3c387-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-220">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c387-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-222">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c387-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-223">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c387-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-224">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c387-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-226">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="3c387-226">Type of event log message.</span></span> <span data-ttu-id="3c387-227">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="3c387-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="3c387-228">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="3c387-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c387-229">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c387-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c387-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c387-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c387-231">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="3c387-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="3c387-232">Значения</span><span class="sxs-lookup"><span data-stu-id="3c387-232">Values</span></span>                                                                                  | <span data-ttu-id="3c387-233">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="3c387-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="3c387-235">\_ \_ Состояние ошибки шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="3c387-236"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="3c387-237">\_ \_ Тип ошибки шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="3c387-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="3c387-239">\_Идентификатор шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="3c387-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="3c387-241">\_Адрес шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="3c387-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="3c387-243">\_Данные шины PCI \_ являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="3c387-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="3c387-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="3c387-245">\_ \_ Cmd-шина PCI является допустимой.</span><span class="sxs-lookup"><span data-stu-id="3c387-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="3c387-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="3c387-247">\_ \_ Идентификатор запрашивающей стороны шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="3c387-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="3c387-249">\_ \_ Допустимый идентификатор респондента шины PCI \_ .</span><span class="sxs-lookup"><span data-stu-id="3c387-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="3c387-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="3c387-251">\_ \_ Идентификатор целевого объекта шины PCI \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="3c387-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="3c387-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="3c387-253">\_ \_ Идентификатор изготовителя шины PCI \_ действителен.</span><span class="sxs-lookup"><span data-stu-id="3c387-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="3c387-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="3c387-255">\_ \_ Структура данных OEM шины PCI \_ \_ является допустимой.</span><span class="sxs-lookup"><span data-stu-id="3c387-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="3c387-256">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c387-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c387-257">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c387-257">Remarks</span></span>

<span data-ttu-id="3c387-258">Класс **мсмкаевент \_ пЦибусеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="3c387-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c387-259">Требования</span><span class="sxs-lookup"><span data-stu-id="3c387-259">Requirements</span></span>



| <span data-ttu-id="3c387-260">Требование</span><span class="sxs-lookup"><span data-stu-id="3c387-260">Requirement</span></span> | <span data-ttu-id="3c387-261">Значение</span><span class="sxs-lookup"><span data-stu-id="3c387-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c387-262">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c387-262">Minimum supported client</span></span><br/> | <span data-ttu-id="3c387-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c387-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3c387-264">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c387-264">Minimum supported server</span></span><br/> | <span data-ttu-id="3c387-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c387-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3c387-266">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c387-266">Namespace</span></span><br/>                | <span data-ttu-id="3c387-267">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="3c387-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3c387-268">MOF</span><span class="sxs-lookup"><span data-stu-id="3c387-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c387-269"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c387-270">DLL</span><span class="sxs-lookup"><span data-stu-id="3c387-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c387-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c387-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c387-272">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c387-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c387-273">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="3c387-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="3c387-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="3c387-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

