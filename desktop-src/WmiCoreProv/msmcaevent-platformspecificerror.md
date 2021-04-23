---
description: Указывает на ошибку платформы проверки машинного уровня (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: Класс MSMCAEvent_PlatformSpecificError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497436"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="ab63f-104">\_Класс мсмкаевент платформспеЦифицеррор</span><span class="sxs-lookup"><span data-stu-id="ab63f-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="ab63f-105">Класс **мсмкаевент \_ платформспеЦифицеррор** указывает на ошибку платформы проверки компьютера (MCA), относящуюся к конкретной платформе.</span><span class="sxs-lookup"><span data-stu-id="ab63f-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="ab63f-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="ab63f-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="ab63f-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ab63f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ab63f-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="ab63f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab63f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab63f-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="ab63f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ab63f-110">Members</span></span>

<span data-ttu-id="ab63f-111">Класс **мсмкаевент \_ платформспеЦифицеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab63f-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="ab63f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab63f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab63f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab63f-113">Properties</span></span>

<span data-ttu-id="ab63f-114">Класс **мсмкаевент \_ платформспеЦифицеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab63f-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab63f-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="ab63f-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ab63f-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ab63f-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="ab63f-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab63f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-122">Число дополнительных ошибок в записи.</span><span class="sxs-lookup"><span data-stu-id="ab63f-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-123">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="ab63f-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab63f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-126">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ab63f-126">CPU that reported the error.</span></span> <span data-ttu-id="ab63f-127">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="ab63f-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-128">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="ab63f-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ab63f-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-131">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="ab63f-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="ab63f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ab63f-132">Value</span></span>                                                                                                | <span data-ttu-id="ab63f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ab63f-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="ab63f-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="ab63f-135">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="ab63f-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="ab63f-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ab63f-137">Аварий</span><span class="sxs-lookup"><span data-stu-id="ab63f-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="ab63f-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ab63f-139">Исправимая</span><span class="sxs-lookup"><span data-stu-id="ab63f-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab63f-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ab63f-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab63f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ab63f-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-144">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="ab63f-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-145">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="ab63f-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab63f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-148">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="ab63f-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-149">**\_идентификатор компонента \_ OEM**</span><span class="sxs-lookup"><span data-stu-id="ab63f-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-150">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ab63f-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-152">Уникальный идентификатор компонента, который сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ab63f-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-153">**\_данные, \_ относящиеся к шине платформы \_**</span><span class="sxs-lookup"><span data-stu-id="ab63f-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-154">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-156">Зависимые от производителя данные, зависящие от конкретной шины.</span><span class="sxs-lookup"><span data-stu-id="ab63f-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="ab63f-157">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-158">**\_состояние ошибки \_ платформы**</span><span class="sxs-lookup"><span data-stu-id="ab63f-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-159">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-161">Универсальное состояние ошибки платформы.</span><span class="sxs-lookup"><span data-stu-id="ab63f-161">Generic platform error status.</span></span>

<span data-ttu-id="ab63f-162">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-163">**\_идентификатор запрашивающей стороны платформы \_**</span><span class="sxs-lookup"><span data-stu-id="ab63f-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-164">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-166">Идентификатор запрашивающего объекта во время события.</span><span class="sxs-lookup"><span data-stu-id="ab63f-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="ab63f-167">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-168">**\_идентификатор респондента платформы \_**</span><span class="sxs-lookup"><span data-stu-id="ab63f-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-169">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-171">Идентификатор респондента во время события.</span><span class="sxs-lookup"><span data-stu-id="ab63f-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="ab63f-172">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-173">**\_идентификатор целевого объекта платформы \_**</span><span class="sxs-lookup"><span data-stu-id="ab63f-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-174">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-176">Целевой идентификатор во время события.</span><span class="sxs-lookup"><span data-stu-id="ab63f-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="ab63f-177">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-178">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="ab63f-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-179">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ab63f-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-181">Массив байтов, содержащий необработанную запись об ошибке, представленную в Windows уровнем абстрагирования системы (SAL).</span><span class="sxs-lookup"><span data-stu-id="ab63f-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="ab63f-182">Число элементов в массиве задается свойством **size** .</span><span class="sxs-lookup"><span data-stu-id="ab63f-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-183">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="ab63f-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-184">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-186">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="ab63f-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="ab63f-187">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-188">**Размер**</span><span class="sxs-lookup"><span data-stu-id="ab63f-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-189">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab63f-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-191">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ab63f-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-192">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ab63f-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab63f-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-195">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="ab63f-195">Type of event log message.</span></span> <span data-ttu-id="ab63f-196">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="ab63f-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="ab63f-197">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="ab63f-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab63f-198">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab63f-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab63f-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab63f-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab63f-200">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="ab63f-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="ab63f-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ab63f-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="ab63f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ab63f-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="ab63f-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="ab63f-204">**Платформа \_ \_Состояние ошибки** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="ab63f-205"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="ab63f-206">**Платформа \_ \_ \_ Идентификатор запроса об ошибке** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="ab63f-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="ab63f-208">**Платформа \_ \_ \_ Идентификатор респондента ошибки** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="ab63f-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="ab63f-210">**Платформа \_ \_ \_ Идентификатор целевого объекта ошибки** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="ab63f-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="ab63f-212">**Платформа \_ \_ \_ Данные, относящиеся к ошибкам** , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="ab63f-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="ab63f-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="ab63f-214">**Платформа \_ \_ \_ Код ошибки OEM** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="ab63f-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="ab63f-216">**Платформа \_ Ошибка \_ \_ \_ структуры данных OEM** .</span><span class="sxs-lookup"><span data-stu-id="ab63f-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="ab63f-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="ab63f-218">**Платформа \_ Ошибка \_ : \_ \_ путь к устройству изготовителя оборудования** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="ab63f-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="ab63f-219">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab63f-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab63f-220">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab63f-220">Remarks</span></span>

<span data-ttu-id="ab63f-221">Класс **мсмкаевент \_ платформспеЦифицеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="ab63f-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab63f-222">Требования</span><span class="sxs-lookup"><span data-stu-id="ab63f-222">Requirements</span></span>



| <span data-ttu-id="ab63f-223">Требование</span><span class="sxs-lookup"><span data-stu-id="ab63f-223">Requirement</span></span> | <span data-ttu-id="ab63f-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ab63f-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab63f-225">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab63f-225">Minimum supported client</span></span><br/> | <span data-ttu-id="ab63f-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab63f-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="ab63f-227">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab63f-227">Minimum supported server</span></span><br/> | <span data-ttu-id="ab63f-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab63f-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="ab63f-229">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab63f-229">Namespace</span></span><br/>                | <span data-ttu-id="ab63f-230">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="ab63f-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ab63f-231">MOF</span><span class="sxs-lookup"><span data-stu-id="ab63f-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab63f-232"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab63f-233">DLL</span><span class="sxs-lookup"><span data-stu-id="ab63f-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab63f-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab63f-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab63f-235">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab63f-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab63f-236">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="ab63f-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="ab63f-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="ab63f-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

