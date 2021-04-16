---
description: '\_Класс потока CIM представляет возможность выполнения единиц процесса или задачи в параллельном режиме. Процесс может иметь много потоков, каждый из которых является ненадежным для процесса.'
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: Класс CIM_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656086"
---
# <a name="cim_thread-class"></a><span data-ttu-id="17685-104">\_Класс потока CIM</span><span class="sxs-lookup"><span data-stu-id="17685-104">CIM\_Thread class</span></span>

<span data-ttu-id="17685-105">Класс **\_ потока CIM** представляет возможность выполнения единиц процесса или задачи в параллельном режиме.</span><span class="sxs-lookup"><span data-stu-id="17685-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="17685-106">Процесс может иметь много потоков, каждый из которых является ненадежным для процесса.</span><span class="sxs-lookup"><span data-stu-id="17685-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17685-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="17685-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17685-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17685-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17685-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="17685-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="17685-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="17685-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17685-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17685-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
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
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="17685-112">Члены</span><span class="sxs-lookup"><span data-stu-id="17685-112">Members</span></span>

<span data-ttu-id="17685-113">Класс **\_ потока CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="17685-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="17685-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="17685-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17685-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="17685-115">Properties</span></span>

<span data-ttu-id="17685-116">Класс **\_ потока CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="17685-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17685-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="17685-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="17685-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="17685-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="17685-121">Short textual description of the object.</span></span>

<span data-ttu-id="17685-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17685-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="17685-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-126">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="17685-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="17685-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="17685-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="17685-129">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="17685-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-132">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-133">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="17685-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="17685-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="17685-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-137">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-138">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="17685-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="17685-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="17685-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-142">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="17685-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="17685-143">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="17685-143">Textual description of the object.</span></span>

<span data-ttu-id="17685-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17685-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="17685-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17685-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17685-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17685-148">Указывает текущее рабочее состояние потока.</span><span class="sxs-lookup"><span data-stu-id="17685-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17685-149">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="17685-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="17685-150">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="17685-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="17685-151">**Готово** (2)</span><span class="sxs-lookup"><span data-stu-id="17685-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="17685-152">**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="17685-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="17685-153">**Заблокировано** (4)</span><span class="sxs-lookup"><span data-stu-id="17685-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="17685-154">**Блокировка приостановлена** (5)</span><span class="sxs-lookup"><span data-stu-id="17685-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="17685-155">**Приостановлено** (6)</span><span class="sxs-lookup"><span data-stu-id="17685-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17685-156">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="17685-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-159">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-160">Идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="17685-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="17685-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="17685-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-162">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="17685-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="17685-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="17685-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="17685-165">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="17685-165">Date and time the object was installed.</span></span> <span data-ttu-id="17685-166">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="17685-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="17685-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17685-168">**кернелмодетиме**</span><span class="sxs-lookup"><span data-stu-id="17685-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-169">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17685-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="17685-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-171">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="17685-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="17685-172">Время, в режиме ядра, в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="17685-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="17685-173">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="17685-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="17685-174">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="17685-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="17685-175">**Name**</span><span class="sxs-lookup"><span data-stu-id="17685-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-178">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="17685-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="17685-179">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="17685-179">Label by which the object is known.</span></span> <span data-ttu-id="17685-180">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="17685-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="17685-181">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="17685-182">**оскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="17685-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-185">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**Оскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-186">Определение области для имени класса создания операционной системы.</span><span class="sxs-lookup"><span data-stu-id="17685-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="17685-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="17685-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-190">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**OSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-191">Определение области действия имени операционной системы.</span><span class="sxs-lookup"><span data-stu-id="17685-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="17685-192">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="17685-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17685-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17685-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17685-195">Срочность выполнения потока.</span><span class="sxs-lookup"><span data-stu-id="17685-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="17685-196">Поток может иметь свой приоритет, чем его процесс-владелец.</span><span class="sxs-lookup"><span data-stu-id="17685-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="17685-197">Если эта информация недоступна для потока, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="17685-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="17685-198">**процесскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="17685-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-201">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-202">Имя класса создания процесса определения области.</span><span class="sxs-lookup"><span data-stu-id="17685-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="17685-203">**процесшандле**</span><span class="sxs-lookup"><span data-stu-id="17685-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-206">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ процесс CIM**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="17685-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17685-207">Маркер процесса определения области.</span><span class="sxs-lookup"><span data-stu-id="17685-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="17685-208">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="17685-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="17685-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17685-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-211">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="17685-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="17685-212">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="17685-212">Current status of the object.</span></span> <span data-ttu-id="17685-213">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="17685-214">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="17685-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="17685-215">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="17685-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="17685-216">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="17685-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="17685-217">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="17685-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17685-218">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="17685-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="17685-219">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="17685-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="17685-220">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="17685-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="17685-221">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="17685-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="17685-222">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="17685-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="17685-223">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="17685-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="17685-224">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="17685-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="17685-225">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="17685-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="17685-226">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="17685-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17685-227">**усермодетиме**</span><span class="sxs-lookup"><span data-stu-id="17685-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17685-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17685-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="17685-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17685-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17685-230">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="17685-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="17685-231">Время в пользовательском режиме в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="17685-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="17685-232">Если эта информация недоступна, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="17685-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="17685-233">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="17685-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17685-234">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17685-234">Remarks</span></span>

<span data-ttu-id="17685-235">Класс **\_ потока CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="17685-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="17685-236">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="17685-236">WMI does not implement this class.</span></span> <span data-ttu-id="17685-237">Классы WMI, производные **от \_ потока CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17685-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="17685-238">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="17685-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17685-239">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="17685-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17685-240">Требования</span><span class="sxs-lookup"><span data-stu-id="17685-240">Requirements</span></span>



| <span data-ttu-id="17685-241">Требование</span><span class="sxs-lookup"><span data-stu-id="17685-241">Requirement</span></span> | <span data-ttu-id="17685-242">Значение</span><span class="sxs-lookup"><span data-stu-id="17685-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17685-243">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17685-243">Minimum supported client</span></span><br/> | <span data-ttu-id="17685-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17685-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17685-245">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17685-245">Minimum supported server</span></span><br/> | <span data-ttu-id="17685-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17685-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17685-247">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17685-247">Namespace</span></span><br/>                | <span data-ttu-id="17685-248">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17685-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17685-249">MOF</span><span class="sxs-lookup"><span data-stu-id="17685-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17685-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17685-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17685-251">DLL</span><span class="sxs-lookup"><span data-stu-id="17685-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17685-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17685-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17685-253">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17685-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17685-254">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="17685-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

