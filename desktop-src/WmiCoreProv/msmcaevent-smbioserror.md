---
description: Указывает системную ошибку BIOS в архитектуре проверки компьютеров (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Класс MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266090"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="a8436-104">\_Класс мсмкаевент смбиосеррор</span><span class="sxs-lookup"><span data-stu-id="a8436-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="a8436-105">Класс **мсмкаевент \_ смбиосеррор** указывает на ошибку BIOS системы архитектуры MCA.</span><span class="sxs-lookup"><span data-stu-id="a8436-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="a8436-106">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="a8436-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="a8436-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a8436-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a8436-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="a8436-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8436-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8436-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="a8436-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a8436-110">Members</span></span>

<span data-ttu-id="a8436-111">Класс **мсмкаевент \_ смбиосеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8436-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="a8436-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8436-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8436-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8436-113">Properties</span></span>

<span data-ttu-id="a8436-114">Класс **мсмкаевент \_ смбиосеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8436-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8436-115">**Активен**</span><span class="sxs-lookup"><span data-stu-id="a8436-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a8436-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-118">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a8436-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-119">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="a8436-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8436-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-122">Число дополнительных ошибок в записи.</span><span class="sxs-lookup"><span data-stu-id="a8436-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-123">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="a8436-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8436-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-126">ЦП, сообщающий об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8436-126">CPU that reported the error.</span></span> <span data-ttu-id="a8436-127">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="a8436-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-128">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="a8436-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a8436-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-131">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="a8436-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="a8436-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a8436-132">Value</span></span>                                                                                                | <span data-ttu-id="a8436-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a8436-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a8436-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="a8436-135">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="a8436-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="a8436-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a8436-137">Аварий</span><span class="sxs-lookup"><span data-stu-id="a8436-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="a8436-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a8436-139">Исправимая</span><span class="sxs-lookup"><span data-stu-id="a8436-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8436-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="a8436-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8436-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8436-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a8436-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a8436-144">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="a8436-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-145">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="a8436-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8436-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-148">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="a8436-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-149">**раврекорд**</span><span class="sxs-lookup"><span data-stu-id="a8436-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-150">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a8436-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a8436-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-152">Массив байтов, содержащий необработанную запись об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8436-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="a8436-153">Число элементов в массиве, которое указывает свойство **size** .</span><span class="sxs-lookup"><span data-stu-id="a8436-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-154">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="a8436-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-155">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a8436-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-157">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="a8436-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="a8436-158">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a8436-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a8436-159">**Размер**</span><span class="sxs-lookup"><span data-stu-id="a8436-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8436-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-162">Размер необработанной записи об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8436-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-163">**\_Тип события \_ SMBIOS**</span><span class="sxs-lookup"><span data-stu-id="a8436-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-164">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a8436-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-166">Тип события.</span><span class="sxs-lookup"><span data-stu-id="a8436-166">Event type.</span></span>



| <span data-ttu-id="a8436-167">Значение</span><span class="sxs-lookup"><span data-stu-id="a8436-167">Value</span></span>                                                                                                  | <span data-ttu-id="a8436-168">Значение</span><span class="sxs-lookup"><span data-stu-id="a8436-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a8436-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="a8436-170">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a8436-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="a8436-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="a8436-172">Ошибка памяти ECC с одним битом.</span><span class="sxs-lookup"><span data-stu-id="a8436-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="a8436-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="a8436-174">Ошибка множественной разрядной памяти ECC.</span><span class="sxs-lookup"><span data-stu-id="a8436-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="a8436-175"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="a8436-176">Ошибка четности памяти.</span><span class="sxs-lookup"><span data-stu-id="a8436-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="a8436-177"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="a8436-178">Время ожидания шины истекло.</span><span class="sxs-lookup"><span data-stu-id="a8436-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="a8436-179"><dt>**5.0**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="a8436-180">Проверка канала ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a8436-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="a8436-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="a8436-182">Программное Прерывание NMI.</span><span class="sxs-lookup"><span data-stu-id="a8436-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="a8436-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="a8436-184">Изменение размера записи в память.</span><span class="sxs-lookup"><span data-stu-id="a8436-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="a8436-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="a8436-186">Ошибка POST.</span><span class="sxs-lookup"><span data-stu-id="a8436-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="a8436-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="a8436-188">Ошибка четности PCI.</span><span class="sxs-lookup"><span data-stu-id="a8436-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="a8436-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="a8436-190">Системная ошибка PCI.</span><span class="sxs-lookup"><span data-stu-id="a8436-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="a8436-191"><dt>**стр**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="a8436-192">Сбой ЦП.</span><span class="sxs-lookup"><span data-stu-id="a8436-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="a8436-193"><dt>**Двенадцать**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="a8436-194">Время ожидания отказоустойчивого таймера EISA истекло.</span><span class="sxs-lookup"><span data-stu-id="a8436-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="a8436-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="a8436-196">Исправимый журнал памяти отключен.</span><span class="sxs-lookup"><span data-stu-id="a8436-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="a8436-197"><dt>**открыт**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="a8436-198">Ведение журнала отключено для определенного типа событий.</span><span class="sxs-lookup"><span data-stu-id="a8436-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="a8436-199">Слишком много ошибок одного типа получены в течение короткого промежутка времени.</span><span class="sxs-lookup"><span data-stu-id="a8436-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="a8436-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="a8436-201">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a8436-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="a8436-202"><dt>**глубин**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="a8436-203">Превышено ограничение системы (например, превышение порогового значения напряжения или температуры).</span><span class="sxs-lookup"><span data-stu-id="a8436-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="a8436-204"><dt>**широкоэкранны**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="a8436-205">Асинхронное аппаратное таймерное время истекло и выдано восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="a8436-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="a8436-206"><dt>**стр**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="a8436-207">Сведения о конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="a8436-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="a8436-208"><dt>**стр**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="a8436-209">Сведения о жестком диске.</span><span class="sxs-lookup"><span data-stu-id="a8436-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="a8436-210"><dt>**20**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="a8436-211">Система перенастроена.</span><span class="sxs-lookup"><span data-stu-id="a8436-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="a8436-212"><dt>**открыт**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="a8436-213">Неисправимая сложная ошибка ЦП.</span><span class="sxs-lookup"><span data-stu-id="a8436-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="a8436-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="a8436-215">Сброс или Очистка области журнала.</span><span class="sxs-lookup"><span data-stu-id="a8436-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="a8436-216"><dt>**выражения**</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="a8436-217">Загрузка системы.</span><span class="sxs-lookup"><span data-stu-id="a8436-217">System boot.</span></span> <span data-ttu-id="a8436-218">При реализации эта запись журнала гарантированно будет первой, записанной при любой загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="a8436-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a8436-219">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a8436-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-220">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8436-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-222">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="a8436-222">Type of event log message.</span></span> <span data-ttu-id="a8436-223">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="a8436-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="a8436-224">**\_биты проверки**</span><span class="sxs-lookup"><span data-stu-id="a8436-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8436-225">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a8436-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a8436-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8436-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8436-227">Биты проверки, используемые для указания допустимости последующих полей.</span><span class="sxs-lookup"><span data-stu-id="a8436-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="a8436-228">Значение 1 (0x1) означает, что **\_ событие SMBIOS** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="a8436-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="a8436-229">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a8436-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8436-230">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8436-230">Remarks</span></span>

<span data-ttu-id="a8436-231">Класс **мсмкаевент \_ смбиосеррор** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="a8436-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8436-232">Требования</span><span class="sxs-lookup"><span data-stu-id="a8436-232">Requirements</span></span>



| <span data-ttu-id="a8436-233">Требование</span><span class="sxs-lookup"><span data-stu-id="a8436-233">Requirement</span></span> | <span data-ttu-id="a8436-234">Значение</span><span class="sxs-lookup"><span data-stu-id="a8436-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8436-235">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8436-235">Minimum supported client</span></span><br/> | <span data-ttu-id="a8436-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8436-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a8436-237">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8436-237">Minimum supported server</span></span><br/> | <span data-ttu-id="a8436-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8436-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a8436-239">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8436-239">Namespace</span></span><br/>                | <span data-ttu-id="a8436-240">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="a8436-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a8436-241">MOF</span><span class="sxs-lookup"><span data-stu-id="a8436-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8436-242"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8436-243">DLL</span><span class="sxs-lookup"><span data-stu-id="a8436-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8436-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8436-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8436-245">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8436-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8436-246">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="a8436-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="a8436-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="a8436-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

