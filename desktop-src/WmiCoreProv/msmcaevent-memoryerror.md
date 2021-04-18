---
description: Представляет событие ошибки памяти в архитектуре проверки компьютера (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: Класс MSMCAEvent_MemoryError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693451"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="5455e-104">\_Класс мсмкаевент мемореррор</span><span class="sxs-lookup"><span data-stu-id="5455e-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="5455e-105">Класс **мсмкаевент \_ мемореррор** представляет событие ошибки памяти в архитектуре проверки компьютера (MCA).</span><span class="sxs-lookup"><span data-stu-id="5455e-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="5455e-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="5455e-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="5455e-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5455e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5455e-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="5455e-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5455e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5455e-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="5455e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5455e-110">Members</span></span>

<span data-ttu-id="5455e-111">Класс **мсмкаевент \_ мемореррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5455e-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="5455e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5455e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5455e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5455e-113">Properties</span></span>

<span data-ttu-id="5455e-114">Класс **мсмкаевент \_ мемореррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5455e-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5455e-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="5455e-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5455e-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5455e-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="5455e-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5455e-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-122">Число дополнительных ошибок в записи MCA.</span><span class="sxs-lookup"><span data-stu-id="5455e-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-123">**\_данные, относящиеся к шине \_**</span><span class="sxs-lookup"><span data-stu-id="5455e-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-126">Зависимые от производителя данные, зависящие от конкретной шины.</span><span class="sxs-lookup"><span data-stu-id="5455e-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="5455e-127">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-128">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="5455e-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5455e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-131">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5455e-131">CPU that reported the error.</span></span> <span data-ttu-id="5455e-132">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="5455e-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-133">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="5455e-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-134">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5455e-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-136">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="5455e-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="5455e-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5455e-137">Value</span></span>                                                                                                | <span data-ttu-id="5455e-138">Значение</span><span class="sxs-lookup"><span data-stu-id="5455e-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="5455e-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="5455e-140">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="5455e-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="5455e-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5455e-142">Аварий</span><span class="sxs-lookup"><span data-stu-id="5455e-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="5455e-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5455e-144">Исправимая</span><span class="sxs-lookup"><span data-stu-id="5455e-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5455e-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="5455e-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5455e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5455e-148">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5455e-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5455e-149">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="5455e-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-150">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="5455e-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5455e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-153">Если значение равно нулю, это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="5455e-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-154">**\_банк MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-157">Номер модуля или РАНГа расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-158">**\_разрядное \_ Расположение MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-161">Битовая позицией в слове памяти, содержащей ошибку.</span><span class="sxs-lookup"><span data-stu-id="5455e-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-162">**\_карточка памяти**</span><span class="sxs-lookup"><span data-stu-id="5455e-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-165">Номер карты для расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-166">**MEM, \_ столбец**</span><span class="sxs-lookup"><span data-stu-id="5455e-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-169">Номер столбца расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-170">**\_устройство MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-171">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-173">Номер устройства для расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-174">**\_состояние ошибки \_ mem**</span><span class="sxs-lookup"><span data-stu-id="5455e-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-175">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-177">Состояние ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-177">Memory error status.</span></span>

<span data-ttu-id="5455e-178">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-179">**\_модуль MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-182">Номер модуля или ранга расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-183">**\_узел MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-186">Узел, содержащий ошибку памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-186">Node that contains the memory error.</span></span> <span data-ttu-id="5455e-187">Это свойство применяется только в системе с несколькими узлами.</span><span class="sxs-lookup"><span data-stu-id="5455e-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="5455e-188">Это свойство зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="5455e-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-189">**\_физический \_ адрес MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-190">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-192">Физический адрес ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-192">Physical address of the memory error.</span></span>

<span data-ttu-id="5455e-193">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-194">**\_физическая \_ Маска MEM**</span><span class="sxs-lookup"><span data-stu-id="5455e-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-195">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-197">Допустимые биты адреса в 64-разрядном физическом адресе ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="5455e-198">Физическая маска задает гранулярность физического адреса.</span><span class="sxs-lookup"><span data-stu-id="5455e-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="5455e-199">Физический адрес ошибки памяти зависит от факторов аппаратной реализации.</span><span class="sxs-lookup"><span data-stu-id="5455e-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="5455e-200">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-201">**MEM, \_ строка**</span><span class="sxs-lookup"><span data-stu-id="5455e-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5455e-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-204">Номер строки расположения ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-205">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="5455e-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-206">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5455e-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5455e-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-208">Массив байтов, содержащий необработанную запись об ошибке, представленную в Windows уровнем абстрагирования системы (SAL).</span><span class="sxs-lookup"><span data-stu-id="5455e-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="5455e-209">Число элементов в массиве задается свойством **size** .</span><span class="sxs-lookup"><span data-stu-id="5455e-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-210">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="5455e-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-211">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-213">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="5455e-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="5455e-214">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-215">**Идентификатор ЗАПРАШИВАЮЩего \_**</span><span class="sxs-lookup"><span data-stu-id="5455e-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-216">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-218">Аппаратный адрес устройства или компонента, который инициирует транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5455e-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="5455e-219">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-220">**Идентификатор РЕСПОНДЕНТа \_**</span><span class="sxs-lookup"><span data-stu-id="5455e-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-221">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-223">Аппаратный адрес респондента для транзакции.</span><span class="sxs-lookup"><span data-stu-id="5455e-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="5455e-224">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-225">**Размер**</span><span class="sxs-lookup"><span data-stu-id="5455e-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-226">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5455e-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-228">Размер необработанной записи об ошибке в байтах.</span><span class="sxs-lookup"><span data-stu-id="5455e-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-229">**Идентификатор целевого объекта \_**</span><span class="sxs-lookup"><span data-stu-id="5455e-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-230">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-232">Аппаратный адрес предполагаемого целевого объекта транзакции.</span><span class="sxs-lookup"><span data-stu-id="5455e-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="5455e-233">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5455e-234">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5455e-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-235">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5455e-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-237">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="5455e-237">Type of event log message.</span></span> <span data-ttu-id="5455e-238">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="5455e-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="5455e-239">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="5455e-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5455e-240">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5455e-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5455e-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5455e-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5455e-242">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="5455e-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="5455e-243">Значения</span><span class="sxs-lookup"><span data-stu-id="5455e-243">Values</span></span>                                                                                     | <span data-ttu-id="5455e-244">Значение</span><span class="sxs-lookup"><span data-stu-id="5455e-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="5455e-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="5455e-246">\_Состояние ошибки MEM \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="5455e-247"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="5455e-248">\_Физический \_ адрес MEM является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="5455e-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="5455e-250">\_Маска адреса MEM \_ является допустимой.</span><span class="sxs-lookup"><span data-stu-id="5455e-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="5455e-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="5455e-252">\_Узел MEM является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="5455e-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="5455e-254">\_Карточка памяти является допустимой.</span><span class="sxs-lookup"><span data-stu-id="5455e-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="5455e-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="5455e-256">\_Модуль MEM является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="5455e-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="5455e-258">\_Банк MEM является действительным.</span><span class="sxs-lookup"><span data-stu-id="5455e-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="5455e-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="5455e-260">\_Устройство MEM является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="5455e-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="5455e-262">\_Строка MEM является допустимой.</span><span class="sxs-lookup"><span data-stu-id="5455e-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="5455e-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="5455e-264">\_Столбец MEM является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="5455e-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="5455e-266">\_ \_ Допустимое расположение бита памяти.</span><span class="sxs-lookup"><span data-stu-id="5455e-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="5455e-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="5455e-268">\_ \_ Идентификатор запрашивающей стороны платформы MEM \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="5455e-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="5455e-270">\_ \_ Идентификатор ответчика платформы MEM \_ является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5455e-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="5455e-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="5455e-272">\_ \_ Целевая платформа MEM является допустимой.</span><span class="sxs-lookup"><span data-stu-id="5455e-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="5455e-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="5455e-274">\_ \_ Данные, относящиеся к шине платформы MEM \_ \_ , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="5455e-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="5455e-275"><dt>32768 (0x8000)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="5455e-276">\_ \_ \_ Допустимый идентификатор OEM платформы MEM.</span><span class="sxs-lookup"><span data-stu-id="5455e-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="5455e-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="5455e-278">\_ \_ Структура данных OEM платформы MEM \_ \_ является допустимой.</span><span class="sxs-lookup"><span data-stu-id="5455e-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="5455e-279">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5455e-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5455e-280">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5455e-280">Remarks</span></span>

<span data-ttu-id="5455e-281">Класс **мсмкаевент \_ мемореррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="5455e-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5455e-282">Требования</span><span class="sxs-lookup"><span data-stu-id="5455e-282">Requirements</span></span>



| <span data-ttu-id="5455e-283">Требование</span><span class="sxs-lookup"><span data-stu-id="5455e-283">Requirement</span></span> | <span data-ttu-id="5455e-284">Значение</span><span class="sxs-lookup"><span data-stu-id="5455e-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5455e-285">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5455e-285">Minimum supported client</span></span><br/> | <span data-ttu-id="5455e-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5455e-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5455e-287">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5455e-287">Minimum supported server</span></span><br/> | <span data-ttu-id="5455e-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5455e-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5455e-289">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5455e-289">Namespace</span></span><br/>                | <span data-ttu-id="5455e-290">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="5455e-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="5455e-291">MOF</span><span class="sxs-lookup"><span data-stu-id="5455e-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5455e-292"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="5455e-293">DLL</span><span class="sxs-lookup"><span data-stu-id="5455e-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5455e-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5455e-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5455e-295">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5455e-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5455e-296">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="5455e-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="5455e-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="5455e-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

