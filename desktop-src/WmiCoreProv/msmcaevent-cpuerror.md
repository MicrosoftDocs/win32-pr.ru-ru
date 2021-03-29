---
description: Представляет событие ошибки ЦП. Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: Класс MSMCAEvent_CPUError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541503"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="3c48d-104">\_Класс мсмкаевент кпуеррор</span><span class="sxs-lookup"><span data-stu-id="3c48d-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="3c48d-105">Класс **мсмкаевент \_ кпуеррор** представляет событие ошибки ЦП.</span><span class="sxs-lookup"><span data-stu-id="3c48d-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="3c48d-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="3c48d-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="3c48d-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c48d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3c48d-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="3c48d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c48d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c48d-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="3c48d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="3c48d-110">Members</span></span>

<span data-ttu-id="3c48d-111">Класс **мсмкаевент \_ кпуеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c48d-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="3c48d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c48d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c48d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c48d-113">Properties</span></span>

<span data-ttu-id="3c48d-114">Класс **мсмкаевент \_ кпуеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c48d-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c48d-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="3c48d-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3c48d-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="3c48d-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="3c48d-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-122">Число дополнительных ошибок в записи MCA.</span><span class="sxs-lookup"><span data-stu-id="3c48d-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-123">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="3c48d-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-126">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c48d-126">CPU that reported the error.</span></span> <span data-ttu-id="3c48d-127">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="3c48d-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-128">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="3c48d-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c48d-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-131">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="3c48d-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="3c48d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3c48d-132">Value</span></span>                                                                                                | <span data-ttu-id="3c48d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3c48d-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="3c48d-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="3c48d-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="3c48d-135">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="3c48d-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="3c48d-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3c48d-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3c48d-137">Аварий</span><span class="sxs-lookup"><span data-stu-id="3c48d-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="3c48d-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3c48d-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3c48d-139">Исправимая</span><span class="sxs-lookup"><span data-stu-id="3c48d-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c48d-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="3c48d-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3c48d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3c48d-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-144">Уникальный идентификатор для этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="3c48d-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-145">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="3c48d-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-148">Квалификаторы: **вмимиссингдата** (-1)</span><span class="sxs-lookup"><span data-stu-id="3c48d-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-149">Уровень кэша, буфер перевода (TLB) или структура Micro-архитектуры, в которой произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c48d-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="3c48d-150">Значение 0 (ноль) обозначает первый уровень.</span><span class="sxs-lookup"><span data-stu-id="3c48d-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-151">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="3c48d-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-154">Если значение равно нулю, это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="3c48d-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-155">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="3c48d-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-156">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3c48d-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-158">Массив байтов, содержащий необработанную запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3c48d-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="3c48d-159">Число элементов в массиве, которое указывает свойство **size** .</span><span class="sxs-lookup"><span data-stu-id="3c48d-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-160">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="3c48d-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-161">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c48d-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-163">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c48d-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="3c48d-164">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c48d-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-165">**Размер**</span><span class="sxs-lookup"><span data-stu-id="3c48d-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-168">Размер необработанной записи об ошибке в байтах.</span><span class="sxs-lookup"><span data-stu-id="3c48d-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3c48d-169">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c48d-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c48d-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c48d-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c48d-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c48d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c48d-172">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="3c48d-172">Type of event log message.</span></span> <span data-ttu-id="3c48d-173">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="3c48d-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c48d-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c48d-174">Remarks</span></span>

<span data-ttu-id="3c48d-175">Класс **мсмкаевент \_ кпуеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="3c48d-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c48d-176">Требования</span><span class="sxs-lookup"><span data-stu-id="3c48d-176">Requirements</span></span>



| <span data-ttu-id="3c48d-177">Требование</span><span class="sxs-lookup"><span data-stu-id="3c48d-177">Requirement</span></span> | <span data-ttu-id="3c48d-178">Значение</span><span class="sxs-lookup"><span data-stu-id="3c48d-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c48d-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c48d-179">Minimum supported client</span></span><br/> | <span data-ttu-id="3c48d-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c48d-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="3c48d-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c48d-181">Minimum supported server</span></span><br/> | <span data-ttu-id="3c48d-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c48d-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="3c48d-183">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c48d-183">Namespace</span></span><br/>                | <span data-ttu-id="3c48d-184">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="3c48d-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3c48d-185">MOF</span><span class="sxs-lookup"><span data-stu-id="3c48d-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c48d-186"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c48d-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c48d-187">DLL</span><span class="sxs-lookup"><span data-stu-id="3c48d-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c48d-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c48d-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c48d-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c48d-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c48d-190">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="3c48d-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="3c48d-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="3c48d-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

