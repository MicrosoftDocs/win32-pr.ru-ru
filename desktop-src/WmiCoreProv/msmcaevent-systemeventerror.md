---
description: Указывает, что произошло системное событие интеллектуального управления платформой (IPMI). Эта ошибка записывается в журнал системных событий SMBIOS (SEL). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: Класс MSMCAEvent_SystemEventError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647575"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="9ba45-105">\_Класс мсмкаевент системевентеррор</span><span class="sxs-lookup"><span data-stu-id="9ba45-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="9ba45-106">Класс **мсмкаевент \_ системевентеррор** указывает на то, что произошло системное событие интеллектуального управления платформой (IPMI).</span><span class="sxs-lookup"><span data-stu-id="9ba45-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="9ba45-107">Эта ошибка записывается в журнал системных событий SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="9ba45-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="9ba45-108">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="9ba45-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="9ba45-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba45-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9ba45-110">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9ba45-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba45-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba45-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="9ba45-112">Члены</span><span class="sxs-lookup"><span data-stu-id="9ba45-112">Members</span></span>

<span data-ttu-id="9ba45-113">Класс **мсмкаевент \_ системевентеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ba45-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="9ba45-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ba45-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ba45-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ba45-115">Properties</span></span>

<span data-ttu-id="9ba45-116">Класс **мсмкаевент \_ системевентеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ba45-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ba45-117">**Активен**</span><span class="sxs-lookup"><span data-stu-id="9ba45-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9ba45-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-120">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9ba45-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-121">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="9ba45-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba45-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-124">Число дополнительных ошибок в записи.</span><span class="sxs-lookup"><span data-stu-id="9ba45-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-125">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="9ba45-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba45-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-128">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ba45-128">CPU that reported the error.</span></span> <span data-ttu-id="9ba45-129">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="9ba45-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-130">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="9ba45-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-131">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-133">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="9ba45-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="9ba45-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba45-134">Value</span></span>                                                                                                | <span data-ttu-id="9ba45-135">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba45-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9ba45-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9ba45-137">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="9ba45-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9ba45-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9ba45-139">Аварий</span><span class="sxs-lookup"><span data-stu-id="9ba45-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="9ba45-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9ba45-141">Исправимая</span><span class="sxs-lookup"><span data-stu-id="9ba45-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9ba45-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9ba45-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ba45-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ba45-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-146">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="9ba45-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-147">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="9ba45-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba45-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-150">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="9ba45-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-151">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="9ba45-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-152">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-154">Массив байтов, содержащий необработанную запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ba45-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="9ba45-155">Число элементов в массиве, которое указывает свойство **size** .</span><span class="sxs-lookup"><span data-stu-id="9ba45-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="9ba45-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-157">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ba45-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-159">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="9ba45-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="9ba45-160">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ba45-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-161">**SEL, \_ файл1**</span><span class="sxs-lookup"><span data-stu-id="9ba45-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-162">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-164">Поле данных события 1.</span><span class="sxs-lookup"><span data-stu-id="9ba45-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-165">**SEL \_ файл2**</span><span class="sxs-lookup"><span data-stu-id="9ba45-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-166">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-168">Поле данных события 2.</span><span class="sxs-lookup"><span data-stu-id="9ba45-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-169">**SEL \_ DATA3**</span><span class="sxs-lookup"><span data-stu-id="9ba45-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-170">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-172">Поле данных события 3.</span><span class="sxs-lookup"><span data-stu-id="9ba45-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-173">**\_ \_ тип каталога событий \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-174">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-176">Тип каталога событий.</span><span class="sxs-lookup"><span data-stu-id="9ba45-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-177">**\_версия SEL ЕВМ \_**</span><span class="sxs-lookup"><span data-stu-id="9ba45-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-178">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-180">Версия формата сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ba45-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-181">**\_идентификатор генератора SEL \_**</span><span class="sxs-lookup"><span data-stu-id="9ba45-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ba45-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-184">Идентификатор программного обеспечения, если событие было создано программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="9ba45-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-185">**\_идентификатор записи \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-186">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ba45-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-188">Идентификатор записи, используемый для доступа к журналу системных событий SMBIOS (SEL).</span><span class="sxs-lookup"><span data-stu-id="9ba45-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-189">**\_тип записи \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-190">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-192">Тип записи.</span><span class="sxs-lookup"><span data-stu-id="9ba45-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-193">**\_номер датчика \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-194">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-196">Номер датчика, создавшего событие.</span><span class="sxs-lookup"><span data-stu-id="9ba45-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-197">**\_Тип датчика \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-198">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9ba45-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-200">Код типа датчика, создавшего событие.</span><span class="sxs-lookup"><span data-stu-id="9ba45-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-201">**\_Метка времени \_ SEL**</span><span class="sxs-lookup"><span data-stu-id="9ba45-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-202">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ba45-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-204">Метка времени журнала событий.</span><span class="sxs-lookup"><span data-stu-id="9ba45-204">Timestamp of the event log.</span></span>

<span data-ttu-id="9ba45-205">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ba45-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-206">**Размер**</span><span class="sxs-lookup"><span data-stu-id="9ba45-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba45-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-209">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ba45-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-210">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9ba45-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-211">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ba45-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-213">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="9ba45-213">Type of event log message.</span></span> <span data-ttu-id="9ba45-214">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="9ba45-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="9ba45-215">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="9ba45-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ba45-216">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ba45-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ba45-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ba45-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ba45-218">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="9ba45-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="9ba45-219">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba45-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="9ba45-220">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba45-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="9ba45-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="9ba45-222">**SEL \_ \_Идентификатор записи** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="9ba45-223"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="9ba45-224">**SEL \_ \_Тип записи** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="9ba45-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="9ba45-226">**SEL \_ \_Идентификатор генератора** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="9ba45-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="9ba45-228">**SEL \_ \_Версия ЕВМ** является допустимой.</span><span class="sxs-lookup"><span data-stu-id="9ba45-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="9ba45-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="9ba45-230">**SEL \_ \_Тип датчика** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="9ba45-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="9ba45-232">**SEL \_ Допустимый \_ номер датчика** .</span><span class="sxs-lookup"><span data-stu-id="9ba45-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="9ba45-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="9ba45-234">**SEL \_ Указана допустимая \_ Папка Event dir** .</span><span class="sxs-lookup"><span data-stu-id="9ba45-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="9ba45-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="9ba45-236">**SEL \_ СОБЫТИЕ \_ файл1** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="9ba45-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="9ba45-238">**SEL \_ СОБЫТИЕ \_ файл2** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="9ba45-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="9ba45-240">**SEL \_ \_DATA3 события** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9ba45-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="9ba45-241">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ba45-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ba45-242">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ba45-242">Remarks</span></span>

<span data-ttu-id="9ba45-243">Класс **мсмкаевент \_ системевентеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="9ba45-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba45-244">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba45-244">Requirements</span></span>



| <span data-ttu-id="9ba45-245">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba45-245">Requirement</span></span> | <span data-ttu-id="9ba45-246">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba45-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba45-247">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ba45-247">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba45-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ba45-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9ba45-249">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ba45-249">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba45-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ba45-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9ba45-251">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ba45-251">Namespace</span></span><br/>                | <span data-ttu-id="9ba45-252">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="9ba45-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9ba45-253">MOF</span><span class="sxs-lookup"><span data-stu-id="9ba45-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ba45-254"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ba45-255">DLL</span><span class="sxs-lookup"><span data-stu-id="9ba45-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ba45-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ba45-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba45-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba45-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba45-258">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="9ba45-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9ba45-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="9ba45-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

