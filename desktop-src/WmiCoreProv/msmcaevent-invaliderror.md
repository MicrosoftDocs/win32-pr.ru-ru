---
description: Указывает на недействительную ошибку архитектуры проверки машин (MCA). Недопустимая ошибка MCA определяет формат ошибки, который не соответствует спецификациям Windows. Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: Класс MSMCAEvent_InvalidError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692272"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="221fa-105">\_Класс мсмкаевент инвалидеррор</span><span class="sxs-lookup"><span data-stu-id="221fa-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="221fa-106">Класс **мсмкаевент \_ инвалидеррор** указывает на недействительную ошибку архитектуры проверки машин (MCA).</span><span class="sxs-lookup"><span data-stu-id="221fa-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="221fa-107">Недопустимая ошибка MCA определяет формат ошибки, который не соответствует спецификациям Windows.</span><span class="sxs-lookup"><span data-stu-id="221fa-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="221fa-108">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="221fa-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="221fa-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="221fa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="221fa-110">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="221fa-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="221fa-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="221fa-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="221fa-112">Члены</span><span class="sxs-lookup"><span data-stu-id="221fa-112">Members</span></span>

<span data-ttu-id="221fa-113">Класс **мсмкаевент \_ инвалидеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="221fa-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="221fa-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="221fa-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="221fa-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="221fa-115">Properties</span></span>

<span data-ttu-id="221fa-116">Класс **мсмкаевент \_ инвалидеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="221fa-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="221fa-117">**Активен**</span><span class="sxs-lookup"><span data-stu-id="221fa-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="221fa-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-120">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="221fa-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-121">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="221fa-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="221fa-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-124">Число дополнительных ошибок в записи MCA.</span><span class="sxs-lookup"><span data-stu-id="221fa-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-125">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="221fa-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="221fa-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-128">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="221fa-128">CPU that reported the error.</span></span> <span data-ttu-id="221fa-129">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="221fa-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-130">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="221fa-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-131">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="221fa-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-133">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="221fa-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="221fa-134">Значение</span><span class="sxs-lookup"><span data-stu-id="221fa-134">Value</span></span>                                                                                                | <span data-ttu-id="221fa-135">Значение</span><span class="sxs-lookup"><span data-stu-id="221fa-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="221fa-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="221fa-137">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="221fa-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="221fa-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="221fa-139">Аварий</span><span class="sxs-lookup"><span data-stu-id="221fa-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="221fa-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="221fa-141">Исправимая</span><span class="sxs-lookup"><span data-stu-id="221fa-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="221fa-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="221fa-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="221fa-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="221fa-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="221fa-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="221fa-146">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="221fa-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-147">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="221fa-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="221fa-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-150">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="221fa-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-151">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="221fa-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-152">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="221fa-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="221fa-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-154">Массив байтов, содержащий необработанную запись об ошибке, представленную в Windows уровнем абстрагирования системы (SAL).</span><span class="sxs-lookup"><span data-stu-id="221fa-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="221fa-155">Число элементов в массиве задается свойством **size** .</span><span class="sxs-lookup"><span data-stu-id="221fa-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="221fa-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-157">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="221fa-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-159">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="221fa-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="221fa-160">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="221fa-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="221fa-161">**Размер**</span><span class="sxs-lookup"><span data-stu-id="221fa-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="221fa-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-164">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="221fa-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="221fa-165">**Тип**</span><span class="sxs-lookup"><span data-stu-id="221fa-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="221fa-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="221fa-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="221fa-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="221fa-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="221fa-168">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="221fa-168">Type of event log message.</span></span> <span data-ttu-id="221fa-169">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="221fa-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="221fa-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="221fa-170">Remarks</span></span>

<span data-ttu-id="221fa-171">Класс **мсмкаевент \_ инвалидеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="221fa-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="221fa-172">Требования</span><span class="sxs-lookup"><span data-stu-id="221fa-172">Requirements</span></span>



| <span data-ttu-id="221fa-173">Требование</span><span class="sxs-lookup"><span data-stu-id="221fa-173">Requirement</span></span> | <span data-ttu-id="221fa-174">Значение</span><span class="sxs-lookup"><span data-stu-id="221fa-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="221fa-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="221fa-175">Minimum supported client</span></span><br/> | <span data-ttu-id="221fa-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="221fa-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="221fa-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="221fa-177">Minimum supported server</span></span><br/> | <span data-ttu-id="221fa-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="221fa-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="221fa-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="221fa-179">Namespace</span></span><br/>                | <span data-ttu-id="221fa-180">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="221fa-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="221fa-181">MOF</span><span class="sxs-lookup"><span data-stu-id="221fa-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="221fa-182"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="221fa-183">DLL</span><span class="sxs-lookup"><span data-stu-id="221fa-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="221fa-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="221fa-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="221fa-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="221fa-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="221fa-186">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="221fa-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="221fa-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="221fa-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

