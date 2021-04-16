---
description: Поток Win32 \_&\# 8194; Класс WMI представляет поток выполнения.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Класс Win32_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650460"
---
# <a name="win32_thread-class"></a><span data-ttu-id="6e239-103">\_Класс потока Win32</span><span class="sxs-lookup"><span data-stu-id="6e239-103">Win32\_Thread class</span></span>

<span data-ttu-id="6e239-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ потока Win32** представляет поток выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e239-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="6e239-105">Хотя процесс должен иметь один поток выполнения, процесс может создавать другие потоки для параллельного выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="6e239-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="6e239-106">Потоки совместно используют среду процесса, поэтому несколько потоков в одном процессе используют меньше памяти, чем количество процессов.</span><span class="sxs-lookup"><span data-stu-id="6e239-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="6e239-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6e239-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6e239-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="6e239-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e239-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e239-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="6e239-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6e239-110">Members</span></span>

<span data-ttu-id="6e239-111">Класс **\_ потока Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6e239-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="6e239-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e239-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e239-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e239-113">Properties</span></span>

<span data-ttu-id="6e239-114">Класс **\_ потока Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6e239-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e239-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6e239-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-118">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6e239-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6e239-119">Short description of the object.</span></span>

<span data-ttu-id="6e239-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6e239-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-124">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-125">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6e239-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6e239-126">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="6e239-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6e239-127">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-128">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6e239-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-131">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-132">Имя класса создания для системы компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="6e239-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="6e239-133">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6e239-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-137">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-138">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="6e239-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="6e239-139">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-140">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e239-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-143">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6e239-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-144">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6e239-144">Description of the object.</span></span>

<span data-ttu-id="6e239-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-146">**елапседтиме**</span><span class="sxs-lookup"><span data-stu-id="6e239-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-147">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e239-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-149">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры данных производительности Win32API" \| [**\_ \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| перфтиме "), [**единицы**](../wmisdk/standard-qualifiers.md) (" миллисекунды ")</span><span class="sxs-lookup"><span data-stu-id="6e239-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-150">Общее время выполнения в миллисекундах, заданное для этого потока с момента его создания.</span><span class="sxs-lookup"><span data-stu-id="6e239-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="6e239-151">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="6e239-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e239-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e239-155">Текущее рабочее состояние потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="6e239-156">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e239-157">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6e239-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e239-158">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6e239-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="6e239-159">**Готово** (2)</span><span class="sxs-lookup"><span data-stu-id="6e239-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="6e239-160">**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="6e239-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="6e239-161">**Заблокировано** (4)</span><span class="sxs-lookup"><span data-stu-id="6e239-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="6e239-162">**Блокировка приостановлена** (5)</span><span class="sxs-lookup"><span data-stu-id="6e239-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="6e239-163">**Приостановлено** (6)</span><span class="sxs-lookup"><span data-stu-id="6e239-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e239-164">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="6e239-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-167">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры справки по инструментам \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")</span><span class="sxs-lookup"><span data-stu-id="6e239-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-168">Обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-168">Handle to a thread.</span></span> <span data-ttu-id="6e239-169">По умолчанию маркер имеет права полного доступа.</span><span class="sxs-lookup"><span data-stu-id="6e239-169">The handle has full access rights by default.</span></span> <span data-ttu-id="6e239-170">С правильным доступом к безопасности этот маркер можно использовать в любой функции, принимающей обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="6e239-171">В зависимости от флага наследования, указанного при создании, этот маркер может наследоваться дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="6e239-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="6e239-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6e239-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-173">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e239-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-175">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6e239-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-176">Объект был установлен.</span><span class="sxs-lookup"><span data-stu-id="6e239-176">Object was installed.</span></span> <span data-ttu-id="6e239-177">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="6e239-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6e239-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-179">**кернелмодетиме**</span><span class="sxs-lookup"><span data-stu-id="6e239-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-180">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e239-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-182">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("кернелмодетиме"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры данных производительности " \| [**\_ \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| привилежедтиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")</span><span class="sxs-lookup"><span data-stu-id="6e239-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-183">Время в режиме ядра (в единицах 100 нс).</span><span class="sxs-lookup"><span data-stu-id="6e239-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="6e239-184">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6e239-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="6e239-185">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-186">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e239-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-189">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="6e239-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-190">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="6e239-190">Label by which the object is known.</span></span> <span data-ttu-id="6e239-191">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="6e239-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6e239-192">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-193">**оскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6e239-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-196">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**Оскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-197">Имя класса создания для операционной системы области.</span><span class="sxs-lookup"><span data-stu-id="6e239-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="6e239-198">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="6e239-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-202">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**OSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-203">Имя операционной системы области.</span><span class="sxs-lookup"><span data-stu-id="6e239-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="6e239-204">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-205">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="6e239-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-206">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e239-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-208">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("приоритет"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры справки Win32API инструментов \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| тпделтапри")</span><span class="sxs-lookup"><span data-stu-id="6e239-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-209">Динамический приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="6e239-210">Каждый поток имеет динамический приоритет, который планировщик использует для определения того, какой поток следует выполнить.</span><span class="sxs-lookup"><span data-stu-id="6e239-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="6e239-211">Изначально динамический приоритет потока совпадает с его базовым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="6e239-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="6e239-212">Система может увеличить и уменьшить динамический приоритет, чтобы обеспечить его быстроту (гарантируя, что потоки не будут заниматься для процессорного времени).</span><span class="sxs-lookup"><span data-stu-id="6e239-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="6e239-213">Система не увеличивает приоритет потоков с базовым уровнем приоритета от 16 до 31.</span><span class="sxs-lookup"><span data-stu-id="6e239-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="6e239-214">Повышение динамического приоритета получают только потоки с базовым приоритетом между 0 и 15.</span><span class="sxs-lookup"><span data-stu-id="6e239-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="6e239-215">Большее число указывает на более высокие приоритеты.</span><span class="sxs-lookup"><span data-stu-id="6e239-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="6e239-216">**приоритибасе**</span><span class="sxs-lookup"><span data-stu-id="6e239-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-217">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e239-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-219">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Структура данных производительности Win32API" \| [**\_ \_ тип объекта PERF**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| перфприоритибасе ")</span><span class="sxs-lookup"><span data-stu-id="6e239-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-220">Текущий базовый приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-220">Current base priority of a thread.</span></span> <span data-ttu-id="6e239-221">Операционная система может увеличить динамический приоритет потока выше базового приоритета, если поток обрабатывает вводимые пользователем данные, или понизить его до базового приоритета, если поток становится привязанным к вычислению.</span><span class="sxs-lookup"><span data-stu-id="6e239-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="6e239-222">Свойство **приоритибасе** может иметь значение от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="6e239-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="6e239-223">**процесскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6e239-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-226">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6e239-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e239-227">Значение свойства **"процесс определения** области видимости".</span><span class="sxs-lookup"><span data-stu-id="6e239-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="6e239-228">Это свойство наследуется [**от \_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e239-229">**процесшандле**</span><span class="sxs-lookup"><span data-stu-id="6e239-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-232">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Процесшандле"), [**распространяемый**](../wmisdk/standard-qualifiers.md) ("[**\_ процесс CIM**](cim-process.md).**Handle**"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" Win32API Structures \| Help Tools \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")</span><span class="sxs-lookup"><span data-stu-id="6e239-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-233">Процесс, создавший поток.</span><span class="sxs-lookup"><span data-stu-id="6e239-233">Process that created the thread.</span></span> <span data-ttu-id="6e239-234">Содержимое этого свойства может использоваться элементами интерфейса прикладного программирования (API) Windows.</span><span class="sxs-lookup"><span data-stu-id="6e239-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="6e239-235">**стартаддресс**</span><span class="sxs-lookup"><span data-stu-id="6e239-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-236">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e239-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-238">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| объект потока WIn32API \| лпсреад \_ Start \_ подпрограмма \| лпстартаддресс")</span><span class="sxs-lookup"><span data-stu-id="6e239-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-239">Начальный адрес потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-239">Starting address of the thread.</span></span> <span data-ttu-id="6e239-240">Поскольку любое приложение с соответствующим доступом к потоку может изменить контекст потока, это значение может быть только приближением к начальному адресу потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="6e239-241">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6e239-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e239-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-244">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6e239-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-245">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6e239-245">Current status of the object.</span></span> <span data-ttu-id="6e239-246">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="6e239-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6e239-247">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="6e239-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6e239-248">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="6e239-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6e239-249">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="6e239-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6e239-250">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6e239-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6e239-251">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6e239-252">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="6e239-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6e239-253">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6e239-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6e239-254">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6e239-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6e239-255">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6e239-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e239-256">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6e239-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6e239-257">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6e239-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6e239-258">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6e239-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6e239-259">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6e239-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6e239-260">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6e239-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6e239-261">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6e239-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6e239-262">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6e239-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6e239-263">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6e239-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6e239-264">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6e239-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e239-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="6e239-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-266">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e239-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-268">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| состояние потока Win32API")</span><span class="sxs-lookup"><span data-stu-id="6e239-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-269">Текущее состояние выполнения для потока.</span><span class="sxs-lookup"><span data-stu-id="6e239-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="6e239-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Инициализировано** (0)</span><span class="sxs-lookup"><span data-stu-id="6e239-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-271">Инициализировано — он распознается микроядерей.</span><span class="sxs-lookup"><span data-stu-id="6e239-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="6e239-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Готово** (1)</span><span class="sxs-lookup"><span data-stu-id="6e239-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-273">Готово — он готов к работе на следующем доступном процессоре.</span><span class="sxs-lookup"><span data-stu-id="6e239-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="6e239-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (2)</span><span class="sxs-lookup"><span data-stu-id="6e239-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-275">Работает — он исполняется.</span><span class="sxs-lookup"><span data-stu-id="6e239-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="6e239-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="6e239-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-277">Ждущий режим — будет запущен, только один поток может находиться в этом состоянии за раз.</span><span class="sxs-lookup"><span data-stu-id="6e239-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="6e239-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (4)</span><span class="sxs-lookup"><span data-stu-id="6e239-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-279">Завершено — выполнение завершается.</span><span class="sxs-lookup"><span data-stu-id="6e239-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="6e239-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Ожидание** (5)</span><span class="sxs-lookup"><span data-stu-id="6e239-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-281">Ожидание — оно не готово для процессора, когда оно готово, оно будет перепланировано.</span><span class="sxs-lookup"><span data-stu-id="6e239-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="6e239-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Переход** (6)</span><span class="sxs-lookup"><span data-stu-id="6e239-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-283">Переход — поток ожидает ресурсы, отличные от процессора,</span><span class="sxs-lookup"><span data-stu-id="6e239-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e239-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (7)</span><span class="sxs-lookup"><span data-stu-id="6e239-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-285">Неизвестно — состояние потока неизвестно.</span><span class="sxs-lookup"><span data-stu-id="6e239-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6e239-286">**среадваитреасон**</span><span class="sxs-lookup"><span data-stu-id="6e239-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-287">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e239-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-289">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| Причина ожидания потока Win32API")</span><span class="sxs-lookup"><span data-stu-id="6e239-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-290">Причина, по которой поток находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="6e239-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="6e239-291">Это значение допустимо только в том случае, если для **элемента "5** " задано значение "переход" (6).</span><span class="sxs-lookup"><span data-stu-id="6e239-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="6e239-292">Пары событий позволяют обмениваться данными с защищенными подсистемами.</span><span class="sxs-lookup"><span data-stu-id="6e239-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="6e239-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span><span class="sxs-lookup"><span data-stu-id="6e239-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="6e239-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Фрипаже** (1)</span><span class="sxs-lookup"><span data-stu-id="6e239-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6e239-295">фрипаже</span><span class="sxs-lookup"><span data-stu-id="6e239-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="6e239-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pageing** (2)</span><span class="sxs-lookup"><span data-stu-id="6e239-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="6e239-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**Пулаллокатион** (3)</span><span class="sxs-lookup"><span data-stu-id="6e239-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="6e239-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**Ексекутионделай** (4)</span><span class="sxs-lookup"><span data-stu-id="6e239-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="6e239-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Фрипаже** (5)</span><span class="sxs-lookup"><span data-stu-id="6e239-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="6e239-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pageing** (6)</span><span class="sxs-lookup"><span data-stu-id="6e239-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="6e239-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span><span class="sxs-lookup"><span data-stu-id="6e239-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="6e239-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Фрипаже** (8)</span><span class="sxs-lookup"><span data-stu-id="6e239-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="6e239-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pageing** (9)</span><span class="sxs-lookup"><span data-stu-id="6e239-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="6e239-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**Пулаллокатион** (10)</span><span class="sxs-lookup"><span data-stu-id="6e239-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="6e239-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**Ексекутионделай** (11)</span><span class="sxs-lookup"><span data-stu-id="6e239-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="6e239-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**Фрипаже** (12)</span><span class="sxs-lookup"><span data-stu-id="6e239-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="6e239-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Pageing** (13)</span><span class="sxs-lookup"><span data-stu-id="6e239-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="6e239-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**Евентпаирхигх** (14)</span><span class="sxs-lookup"><span data-stu-id="6e239-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="6e239-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**Евентпаирлов** (15)</span><span class="sxs-lookup"><span data-stu-id="6e239-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="6e239-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**Лпкрецеиве** (16)</span><span class="sxs-lookup"><span data-stu-id="6e239-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="6e239-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**Лпкрепли** (17)</span><span class="sxs-lookup"><span data-stu-id="6e239-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="6e239-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**Виртуалмемори** (18)</span><span class="sxs-lookup"><span data-stu-id="6e239-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="6e239-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Выстр** . (19)</span><span class="sxs-lookup"><span data-stu-id="6e239-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e239-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (20)</span><span class="sxs-lookup"><span data-stu-id="6e239-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e239-315">**усермодетиме**</span><span class="sxs-lookup"><span data-stu-id="6e239-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e239-316">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e239-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e239-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e239-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e239-318">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("усермодетиме"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API" \| структуры данных производительности " \| [**\_ \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| усертиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")</span><span class="sxs-lookup"><span data-stu-id="6e239-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="6e239-319">Время в пользовательском режиме, в 100 наносекундах.</span><span class="sxs-lookup"><span data-stu-id="6e239-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="6e239-320">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6e239-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="6e239-321">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e239-322">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e239-322">Remarks</span></span>

<span data-ttu-id="6e239-323">Класс **\_ потока Win32** является производным от [**\_ потока CIM**](cim-thread.md).</span><span class="sxs-lookup"><span data-stu-id="6e239-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="6e239-324">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="6e239-324">**Overview**</span></span>

<span data-ttu-id="6e239-325">Для повседневного мониторинга обычно бывает немало причин получить подробный список потоков и связанных с ними свойств.</span><span class="sxs-lookup"><span data-stu-id="6e239-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="6e239-326">Компьютеры создают и удаляют тысячи потоков в течение дня, а некоторые из этих операций создания и удаления важны для любого, кроме разработчика, который написал программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="6e239-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="6e239-327">Однако при устранении проблем с приложением отслеживание отдельных потоков процесса позволяет выяснить, когда создаются потоки и когда они будут уничтожены.</span><span class="sxs-lookup"><span data-stu-id="6e239-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="6e239-328">Поскольку потоки, которые были созданы, но не уничтожены, вызывают утечку памяти, отслеживание отдельных потоков может быть полезной информацией для специалистов службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="6e239-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="6e239-329">Аналогично, определение приоритетов потоков может помочь в определении потоков, которые, в случае ненормального высокого приоритета, загружают циклы ЦП, необходимые другим потокам и другим процессам.</span><span class="sxs-lookup"><span data-stu-id="6e239-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="6e239-330">**Использование \_ потока Win32**</span><span class="sxs-lookup"><span data-stu-id="6e239-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="6e239-331">Как подразумевается в предыдущем блоке синтаксиса, класс **\_ потока Win32** не сообщает имя процесса, в котором выполняется каждый поток.</span><span class="sxs-lookup"><span data-stu-id="6e239-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="6e239-332">Вместо этого он сообщает идентификатор процесса, в котором выполняется поток.</span><span class="sxs-lookup"><span data-stu-id="6e239-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="6e239-333">Чтобы получить имя процесса и список всех его потоков, сценарий должен:</span><span class="sxs-lookup"><span data-stu-id="6e239-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="6e239-334">Подключитесь к классу [**\_ процесса Win32**](win32-process.md) и возвратите список процессов и идентификаторы их процессов.</span><span class="sxs-lookup"><span data-stu-id="6e239-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="6e239-335">Временно Храните эти сведения в объекте Array или Dictionary.</span><span class="sxs-lookup"><span data-stu-id="6e239-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="6e239-336">Для каждого идентификатора процесса верните список потоков для этого процесса, а затем отобразите имя процесса и список потоков.</span><span class="sxs-lookup"><span data-stu-id="6e239-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="6e239-337">Примеры</span><span class="sxs-lookup"><span data-stu-id="6e239-337">Examples</span></span>

<span data-ttu-id="6e239-338">Следующий пример сценария VBScript наблюдает за потоками, выполняемыми на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6e239-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="6e239-339">Требования</span><span class="sxs-lookup"><span data-stu-id="6e239-339">Requirements</span></span>



| <span data-ttu-id="6e239-340">Требование</span><span class="sxs-lookup"><span data-stu-id="6e239-340">Requirement</span></span> | <span data-ttu-id="6e239-341">Значение</span><span class="sxs-lookup"><span data-stu-id="6e239-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e239-342">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e239-342">Minimum supported client</span></span><br/> | <span data-ttu-id="6e239-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e239-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e239-344">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e239-344">Minimum supported server</span></span><br/> | <span data-ttu-id="6e239-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e239-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e239-346">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e239-346">Namespace</span></span><br/>                | <span data-ttu-id="6e239-347">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6e239-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e239-348">MOF</span><span class="sxs-lookup"><span data-stu-id="6e239-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e239-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e239-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e239-350">DLL</span><span class="sxs-lookup"><span data-stu-id="6e239-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e239-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e239-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e239-352">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e239-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e239-353">**\_Поток CIM**</span><span class="sxs-lookup"><span data-stu-id="6e239-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="6e239-354">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="6e239-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
