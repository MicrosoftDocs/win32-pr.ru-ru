---
description: '\_Класс процессов CIM представляет отдельный экземпляр выполняющейся программы. Пользователь обычно видит процесс как приложение или задачу.'
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: Класс CIM_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990770"
---
# <a name="cim_process-class"></a><span data-ttu-id="88751-104">\_Класс процессов CIM</span><span class="sxs-lookup"><span data-stu-id="88751-104">CIM\_Process class</span></span>

<span data-ttu-id="88751-105">Класс **\_ процессов CIM** представляет отдельный экземпляр выполняющейся программы.</span><span class="sxs-lookup"><span data-stu-id="88751-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="88751-106">Пользователь обычно видит процесс как приложение или задачу.</span><span class="sxs-lookup"><span data-stu-id="88751-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="88751-107">Процесс определяется рабочей областью ресурсов памяти и выделенными для нее параметрами среды.</span><span class="sxs-lookup"><span data-stu-id="88751-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="88751-108">В многозадачной системе Рабочая область предотвращает проникновение ресурсов другими процессами.</span><span class="sxs-lookup"><span data-stu-id="88751-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="88751-109">Кроме того, процесс может выполняться как несколько потоков, которые выполняются в одной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="88751-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88751-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="88751-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88751-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88751-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88751-112">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="88751-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="88751-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="88751-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88751-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88751-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="88751-115">Члены</span><span class="sxs-lookup"><span data-stu-id="88751-115">Members</span></span>

<span data-ttu-id="88751-116">Класс **\_ процесса CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88751-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="88751-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="88751-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88751-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="88751-118">Properties</span></span>

<span data-ttu-id="88751-119">Класс **\_ процесса CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="88751-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88751-120">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="88751-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-123">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="88751-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="88751-124">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88751-124">Short textual description of the object.</span></span>

<span data-ttu-id="88751-125">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88751-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88751-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-129">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="88751-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-130">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="88751-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88751-131">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="88751-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="88751-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="88751-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88751-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88751-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-135">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="88751-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="88751-136">Время начала выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="88751-137">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="88751-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-140">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="88751-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-141">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="88751-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="88751-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="88751-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-145">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="88751-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-146">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="88751-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="88751-147">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88751-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-150">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="88751-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="88751-151">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88751-151">Textual description of the object.</span></span>

<span data-ttu-id="88751-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88751-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="88751-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88751-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88751-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-156">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние выполнения")</span><span class="sxs-lookup"><span data-stu-id="88751-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="88751-157">Текущее рабочее состояние процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88751-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="88751-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88751-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="88751-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="88751-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Готово** (2)</span><span class="sxs-lookup"><span data-stu-id="88751-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="88751-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="88751-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="88751-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Заблокировано** (4)</span><span class="sxs-lookup"><span data-stu-id="88751-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="88751-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Блокировка приостановлена** (5)</span><span class="sxs-lookup"><span data-stu-id="88751-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88751-164">Блокировка приостановлена</span><span class="sxs-lookup"><span data-stu-id="88751-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="88751-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Приостановлено** (6)</span><span class="sxs-lookup"><span data-stu-id="88751-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="88751-166">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="88751-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="88751-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (7)</span><span class="sxs-lookup"><span data-stu-id="88751-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="88751-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (8)</span><span class="sxs-lookup"><span data-stu-id="88751-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="88751-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Растет** (9)</span><span class="sxs-lookup"><span data-stu-id="88751-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88751-170">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="88751-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-173">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="88751-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="88751-174">Идентифицирует процесс.</span><span class="sxs-lookup"><span data-stu-id="88751-174">Identifies the process.</span></span> <span data-ttu-id="88751-175">Идентификатор процесса — это тип обработчика процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="88751-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88751-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-177">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88751-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88751-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-179">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="88751-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="88751-180">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="88751-180">Date and time the object was installed.</span></span> <span data-ttu-id="88751-181">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="88751-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="88751-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88751-183">**кернелмодетиме**</span><span class="sxs-lookup"><span data-stu-id="88751-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-184">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88751-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88751-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-186">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("время модели ядра"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунд")</span><span class="sxs-lookup"><span data-stu-id="88751-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="88751-187">Время в режиме ядра (в единицах 100 нс).</span><span class="sxs-lookup"><span data-stu-id="88751-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="88751-188">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="88751-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="88751-189">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="88751-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88751-190">**Name**</span><span class="sxs-lookup"><span data-stu-id="88751-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-193">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="88751-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-194">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="88751-194">Label by which the object is known.</span></span> <span data-ttu-id="88751-195">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="88751-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="88751-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88751-197">**оскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="88751-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-200">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса операционной системы ")</span><span class="sxs-lookup"><span data-stu-id="88751-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-201">Определение области для имени класса создания операционной системы.</span><span class="sxs-lookup"><span data-stu-id="88751-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="88751-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="88751-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-205">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя операционной системы ")</span><span class="sxs-lookup"><span data-stu-id="88751-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="88751-206">Определение области действия имени операционной системы.</span><span class="sxs-lookup"><span data-stu-id="88751-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="88751-207">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="88751-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88751-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88751-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-210">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("приоритет")</span><span class="sxs-lookup"><span data-stu-id="88751-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="88751-211">Срочность или важность выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="88751-212">Если для процесса не определен приоритет, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="88751-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="88751-213">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88751-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88751-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88751-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-216">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="88751-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="88751-217">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88751-217">Current status of the object.</span></span>

<span data-ttu-id="88751-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="88751-219">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="88751-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88751-220">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="88751-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88751-221">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="88751-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88751-222">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="88751-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88751-223">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="88751-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="88751-224">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="88751-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88751-225">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="88751-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88751-226">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="88751-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="88751-227">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="88751-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88751-228">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="88751-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="88751-229">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="88751-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88751-230">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="88751-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="88751-231">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="88751-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88751-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="88751-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-233">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88751-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88751-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-235">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата завершения")</span><span class="sxs-lookup"><span data-stu-id="88751-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="88751-236">Время остановки или завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="88751-237">**усермодетиме**</span><span class="sxs-lookup"><span data-stu-id="88751-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-238">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88751-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88751-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-240">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("время в пользовательском режиме"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="88751-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="88751-241">Время в пользовательском режиме, в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="88751-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="88751-242">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="88751-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="88751-243">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="88751-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88751-244">**воркингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="88751-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88751-245">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88751-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88751-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88751-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88751-247">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер рабочего множества"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="88751-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88751-248">Объем памяти в байтах, который должен эффективно выполняться процессом для операционной системы, использующей управление памятью на основе страниц.</span><span class="sxs-lookup"><span data-stu-id="88751-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="88751-249">Если в системе недостаточно памяти (меньше размера рабочего набора), пробуксовка происходит.</span><span class="sxs-lookup"><span data-stu-id="88751-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="88751-250">Если размер рабочего набора неизвестен, используйте **значение NULL** или 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="88751-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="88751-251">Если предоставлены данные рабочего набора, можно отслеживать эти сведения, чтобы понять, как изменяются требования к памяти для процесса.</span><span class="sxs-lookup"><span data-stu-id="88751-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="88751-252">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="88751-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88751-253">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88751-253">Remarks</span></span>

<span data-ttu-id="88751-254">Класс **\_ процесса CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88751-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="88751-255">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="88751-255">WMI does not implement this class.</span></span> <span data-ttu-id="88751-256">Сведения о классах WMI, производных от **\_ процесса CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="88751-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="88751-257">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="88751-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88751-258">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="88751-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88751-259">Требования</span><span class="sxs-lookup"><span data-stu-id="88751-259">Requirements</span></span>



| <span data-ttu-id="88751-260">Требование</span><span class="sxs-lookup"><span data-stu-id="88751-260">Requirement</span></span> | <span data-ttu-id="88751-261">Значение</span><span class="sxs-lookup"><span data-stu-id="88751-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88751-262">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88751-262">Minimum supported client</span></span><br/> | <span data-ttu-id="88751-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88751-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88751-264">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88751-264">Minimum supported server</span></span><br/> | <span data-ttu-id="88751-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88751-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88751-266">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88751-266">Namespace</span></span><br/>                | <span data-ttu-id="88751-267">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88751-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88751-268">MOF</span><span class="sxs-lookup"><span data-stu-id="88751-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88751-269"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88751-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88751-270">DLL</span><span class="sxs-lookup"><span data-stu-id="88751-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88751-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88751-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88751-272">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88751-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88751-273">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="88751-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

