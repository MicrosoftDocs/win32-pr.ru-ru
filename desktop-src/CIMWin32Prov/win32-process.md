---
Description: Процесс Win32 \_&\# 32; Класс WMI представляет процесс в операционной системе.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Класс Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657201"
---
# <a name="win32_process-class"></a><span data-ttu-id="cd646-103">\_Класс процесса Win32</span><span class="sxs-lookup"><span data-stu-id="cd646-103">Win32\_Process class</span></span>

<span data-ttu-id="cd646-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ процесса Win32** представляет процесс в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cd646-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="cd646-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cd646-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="cd646-106">Общие сведения о процессах и потоках в Windows см. в разделе [процессы и потоки](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd646-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd646-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="cd646-108">Члены</span><span class="sxs-lookup"><span data-stu-id="cd646-108">Members</span></span>

<span data-ttu-id="cd646-109">Класс **\_ процесса Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd646-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="cd646-110">Методы</span><span class="sxs-lookup"><span data-stu-id="cd646-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd646-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd646-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd646-112">Методы</span><span class="sxs-lookup"><span data-stu-id="cd646-112">Methods</span></span>

<span data-ttu-id="cd646-113">Класс **\_ процесса Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cd646-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="cd646-114">Метод</span><span class="sxs-lookup"><span data-stu-id="cd646-114">Method</span></span>                                                                   | <span data-ttu-id="cd646-115">Описание</span><span class="sxs-lookup"><span data-stu-id="cd646-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd646-116">**аттачдебугжер**</span><span class="sxs-lookup"><span data-stu-id="cd646-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="cd646-117">Запускает зарегистрированный в данный момент отладчик для процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="cd646-118">**Создать**</span><span class="sxs-lookup"><span data-stu-id="cd646-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="cd646-119">Создает новый процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="cd646-120">**жетаваилаблевиртуалсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="cd646-121">Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.</span><span class="sxs-lookup"><span data-stu-id="cd646-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="cd646-122">**Windows server 2012, Windows 8, Windows 7, Windows server 2008 и Windows Vista:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="cd646-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="cd646-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="cd646-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="cd646-124">Возвращает имя пользователя и доменное имя, под которым выполняется процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="cd646-125">**жетовнерсид**</span><span class="sxs-lookup"><span data-stu-id="cd646-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="cd646-126">Возвращает идентификатор безопасности (SID) для владельца процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="cd646-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="cd646-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="cd646-128">Изменяет приоритет выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="cd646-129">**Завершение**</span><span class="sxs-lookup"><span data-stu-id="cd646-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="cd646-130">Завершает процесс и все его потоки.</span><span class="sxs-lookup"><span data-stu-id="cd646-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="cd646-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd646-131">Properties</span></span>

<span data-ttu-id="cd646-132">Класс **\_ процесса Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd646-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd646-133">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cd646-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-136">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cd646-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-137">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="cd646-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="cd646-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="cd646-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-142">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Командная строка для запуска процесса")</span><span class="sxs-lookup"><span data-stu-id="cd646-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-143">Командная строка, используемая для запуска определенного процесса, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="cd646-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd646-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-147">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="cd646-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-148">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cd646-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd646-149">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="cd646-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cd646-150">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="cd646-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-152">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd646-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-154">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="cd646-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-155">Дата начала выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-155">Date the process begins executing.</span></span>

<span data-ttu-id="cd646-156">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-157">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cd646-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-160">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="cd646-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-161">Имя класса создания для системы компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="cd646-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="cd646-162">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="cd646-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-166">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="cd646-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-167">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="cd646-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="cd646-168">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd646-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-172">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="cd646-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-173">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd646-173">Description of an object.</span></span>

<span data-ttu-id="cd646-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="cd646-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-178">Квалификаторы: [**привилегии**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры справки по инструментам Win32API \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| Сзексепас"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("путь к исполняемому файлу")</span><span class="sxs-lookup"><span data-stu-id="cd646-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-179">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="cd646-180">Пример: "C: \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="cd646-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="cd646-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="cd646-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd646-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-184">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние выполнения")</span><span class="sxs-lookup"><span data-stu-id="cd646-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-185">Текущее рабочее состояние процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-185">Current operating condition of the process.</span></span>

<span data-ttu-id="cd646-186">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd646-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="cd646-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cd646-188">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="cd646-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cd646-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="cd646-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cd646-190">Другое</span><span class="sxs-lookup"><span data-stu-id="cd646-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="cd646-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Готово** (2)</span><span class="sxs-lookup"><span data-stu-id="cd646-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="cd646-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)</span><span class="sxs-lookup"><span data-stu-id="cd646-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="cd646-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Заблокировано** (4)</span><span class="sxs-lookup"><span data-stu-id="cd646-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cd646-194">Блокировано</span><span class="sxs-lookup"><span data-stu-id="cd646-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="cd646-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Блокировка приостановлена** (5)</span><span class="sxs-lookup"><span data-stu-id="cd646-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="cd646-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Приостановлено** (6)</span><span class="sxs-lookup"><span data-stu-id="cd646-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="cd646-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (7)</span><span class="sxs-lookup"><span data-stu-id="cd646-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="cd646-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (8)</span><span class="sxs-lookup"><span data-stu-id="cd646-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="cd646-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Растет** (9)</span><span class="sxs-lookup"><span data-stu-id="cd646-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd646-200">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="cd646-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-203">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span><span class="sxs-lookup"><span data-stu-id="cd646-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-204">Идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-204">Process identifier.</span></span>

<span data-ttu-id="cd646-205">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="cd646-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-207">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-209">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("количество маркеров")</span><span class="sxs-lookup"><span data-stu-id="cd646-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-210">Общее число открытых дескрипторов, принадлежащих процессу.</span><span class="sxs-lookup"><span data-stu-id="cd646-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="cd646-211">**HandleCount** — это сумма дескрипторов, которые в настоящее время открыты каждым потоком в этом процессе.</span><span class="sxs-lookup"><span data-stu-id="cd646-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="cd646-212">Для проверки или изменения системных ресурсов используется маркер.</span><span class="sxs-lookup"><span data-stu-id="cd646-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="cd646-213">Каждый обработчик имеет запись в таблице, которая поддерживается внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="cd646-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="cd646-214">Записи содержат адреса ресурсов и данных для обнаружения типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd646-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd646-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-216">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd646-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-218">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="cd646-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-219">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="cd646-219">Date an object is installed.</span></span> <span data-ttu-id="cd646-220">Объект может быть установлен без значения, записываемого в это свойство.</span><span class="sxs-lookup"><span data-stu-id="cd646-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="cd646-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-222">**кернелмодетиме**</span><span class="sxs-lookup"><span data-stu-id="cd646-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-223">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-225">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("кернелмодетиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")</span><span class="sxs-lookup"><span data-stu-id="cd646-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-226">Время в режиме ядра (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="cd646-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="cd646-227">Если эта информация недоступна, используйте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="cd646-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="cd646-228">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-229">**максимумворкингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-232">Квалификаторы: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. \|Ограничения квоты H \_ \| максимумворкингсетсизе "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" максимальный размер рабочего множества "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="cd646-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-233">Максимальный размер рабочего множества процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-233">Maximum working set size of the process.</span></span> <span data-ttu-id="cd646-234">Рабочий набор процесса — это набор страниц памяти, видимых для процесса в физической оперативной памяти.</span><span class="sxs-lookup"><span data-stu-id="cd646-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="cd646-235">Эти страницы являются резидентными и доступны для использования приложением без активации ошибки страницы.</span><span class="sxs-lookup"><span data-stu-id="cd646-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="cd646-236">Пример: 1413120</span><span class="sxs-lookup"><span data-stu-id="cd646-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="cd646-237">**минимумворкингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-238">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-240">Квалификаторы: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. \|Ограничения квоты H \_ \| минимумворкингсетсизе "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" минимальный размер рабочего набора "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="cd646-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-241">Минимальный размер рабочего множества процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-241">Minimum working set size of the process.</span></span> <span data-ttu-id="cd646-242">Рабочий набор процесса — это набор страниц памяти, видимых для процесса в физической оперативной памяти.</span><span class="sxs-lookup"><span data-stu-id="cd646-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="cd646-243">Эти страницы являются резидентными и доступны для использования приложением без активации ошибки страницы.</span><span class="sxs-lookup"><span data-stu-id="cd646-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="cd646-244">Пример: 20480</span><span class="sxs-lookup"><span data-stu-id="cd646-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="cd646-245">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd646-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-248">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="cd646-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-249">Имя исполняемого файла, ответственного за процесс, эквивалентное свойству имя образа в диспетчере задач.</span><span class="sxs-lookup"><span data-stu-id="cd646-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="cd646-250">При наследовании подклассом свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="cd646-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="cd646-251">Имя жестко запрограммировано в самом приложении и не влияет на изменение имени файла.</span><span class="sxs-lookup"><span data-stu-id="cd646-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="cd646-252">Например, даже если переименовать Calc.exe, имя Calc.exe будет по-прежнему отображаться в диспетчере задач и в любых скриптах WMI, которые извлекают имя процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="cd646-253">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-254">**оскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cd646-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-257">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса операционной системы ")</span><span class="sxs-lookup"><span data-stu-id="cd646-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-258">Имя класса создания для операционной системы области.</span><span class="sxs-lookup"><span data-stu-id="cd646-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="cd646-259">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="cd646-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-263">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя операционной системы ")</span><span class="sxs-lookup"><span data-stu-id="cd646-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-264">Имя операционной системы области.</span><span class="sxs-lookup"><span data-stu-id="cd646-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="cd646-265">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-266">**осероператионкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-267">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-269">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Осероператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Счетчик других операций")</span><span class="sxs-lookup"><span data-stu-id="cd646-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-270">Количество выполненных операций ввода-вывода, которые не являются операциями чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="cd646-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="cd646-271">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-272">**осертрансферкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-273">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-275">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Осертрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("другие счетчики передач"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-276">Объем данных, передаваемых во время операций, которые не являются операциями чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="cd646-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="cd646-277">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-278">**пажефаултс**</span><span class="sxs-lookup"><span data-stu-id="cd646-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-279">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-281">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пажефаулткаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число ошибок страниц")</span><span class="sxs-lookup"><span data-stu-id="cd646-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-282">Количество ошибок страниц, создаваемых процессом.</span><span class="sxs-lookup"><span data-stu-id="cd646-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="cd646-283">Пример: 10</span><span class="sxs-lookup"><span data-stu-id="cd646-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="cd646-284">**пажефилеусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-287">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пажефилеусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("использование файла подкачки"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="cd646-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-288">Количество места в файле подкачки, которое используется процессом в данный момент.</span><span class="sxs-lookup"><span data-stu-id="cd646-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="cd646-289">Это значение согласуется со значением **VMSize** в TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="cd646-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="cd646-290">Пример: 102435</span><span class="sxs-lookup"><span data-stu-id="cd646-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="cd646-291">**парентпроцессид**</span><span class="sxs-lookup"><span data-stu-id="cd646-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-294">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Инхеритедфромуникуепроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор родительского процесса")</span><span class="sxs-lookup"><span data-stu-id="cd646-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-295">Уникальный идентификатор процесса, который создает процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="cd646-296">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="cd646-297">Возможно, процесс, идентифицированный **парентпроцессид** , завершается, поэтому **парентпроцессид** может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="cd646-298">Также возможно, что **парентпроцессид** неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="cd646-299">Свойство **CreationDate** можно использовать для определения того, был ли создан указанный родительский объект после создания процесса, представленного этим экземпляром **\_ процесса Win32** .</span><span class="sxs-lookup"><span data-stu-id="cd646-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-300">**пеакпажефилеусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-301">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-303">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеакпажефилеусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковое использование файла подкачки"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="cd646-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-304">Максимальный объем пространства файла подкачки, используемый в течение всего процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="cd646-305">Пример: 102367</span><span class="sxs-lookup"><span data-stu-id="cd646-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="cd646-306">**пеаквиртуалсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-307">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-309">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеаквиртуалсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковое использование адресного пространства виртуальной"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-310">Максимальное виртуальное адресное пространство, используемое процессом в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="cd646-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="cd646-311">Использование виртуального адресного пространства не обязательно подразумевает соответствующее использование страниц диска или основной памяти.</span><span class="sxs-lookup"><span data-stu-id="cd646-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="cd646-312">Однако виртуальное пространство ограничено, и чрезмерное использование процесса может привести к невозможности загрузки библиотек.</span><span class="sxs-lookup"><span data-stu-id="cd646-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="cd646-313">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-314">**пеакворкингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-317">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеакворкингсетсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковый размер рабочего набора"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="cd646-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-318">Пиковый размер рабочего множества процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-318">Peak working set size of a process.</span></span>

<span data-ttu-id="cd646-319">Пример: 1413120</span><span class="sxs-lookup"><span data-stu-id="cd646-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="cd646-320">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="cd646-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-323">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("приоритет"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| басеприорити"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("приоритет")</span><span class="sxs-lookup"><span data-stu-id="cd646-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-324">Планирование приоритета процесса в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cd646-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="cd646-325">Чем выше значение, тем выше приоритет, получаемый процессом.</span><span class="sxs-lookup"><span data-stu-id="cd646-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="cd646-326">Значения приоритета могут находиться в диапазоне от 0 (ноль), который является наименьшим приоритетом до 31, что является высшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cd646-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="cd646-327">Пример: 7</span><span class="sxs-lookup"><span data-stu-id="cd646-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="cd646-328">**приватепажекаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-329">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-331">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Приватепажекаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число частных страниц")</span><span class="sxs-lookup"><span data-stu-id="cd646-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-332">Текущее количество выделенных страниц, которые доступны только для процесса, представленного этим экземпляром **\_ процесса Win32** .</span><span class="sxs-lookup"><span data-stu-id="cd646-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="cd646-333">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-334">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="cd646-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-337">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структуры потоков \| [**\_ сведения о процессе**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| Двпроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор процесса")</span><span class="sxs-lookup"><span data-stu-id="cd646-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-338">Числовой идентификатор, используемый для различения одного процесса от другого.</span><span class="sxs-lookup"><span data-stu-id="cd646-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="cd646-339">Процессидс действительны из времени создания процесса до завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="cd646-340">После завершения работы этот же числовой идентификатор можно применить к новому процессу.</span><span class="sxs-lookup"><span data-stu-id="cd646-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="cd646-341">Это означает, что нельзя использовать только ProcessID для мониторинга определенного процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="cd646-342">Например, приложение может иметь идентификатор процесса 7, а затем завершиться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cd646-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="cd646-343">При запуске нового процесса новому процессу может быть назначен идентификатор процесса 7.</span><span class="sxs-lookup"><span data-stu-id="cd646-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="cd646-344">Сценарий, проверенный только для указанного ProcessID, может быть «обманным», чтобы подумать о том, что исходное приложение все еще запущено.</span><span class="sxs-lookup"><span data-stu-id="cd646-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-345">**куотанонпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-346">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-348">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотанонпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("квота использования невыгружаемого пула")</span><span class="sxs-lookup"><span data-stu-id="cd646-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-349">Квота объема использования невыгружаемого пула для процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="cd646-350">Пример: 15</span><span class="sxs-lookup"><span data-stu-id="cd646-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="cd646-351">**куотапажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-352">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-354">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("квота на использование выгружаемого пула")</span><span class="sxs-lookup"><span data-stu-id="cd646-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-355">Объем использования выгружаемого пула для процесса в квоте.</span><span class="sxs-lookup"><span data-stu-id="cd646-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="cd646-356">Пример: 22</span><span class="sxs-lookup"><span data-stu-id="cd646-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="cd646-357">**куотапеакнонпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-358">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-360">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапеакнонпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Пиковая квота использования невыгружаемого пула")</span><span class="sxs-lookup"><span data-stu-id="cd646-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-361">Пиковая квота использования невыгружаемого пула для процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="cd646-362">Пример: 31</span><span class="sxs-lookup"><span data-stu-id="cd646-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="cd646-363">**куотапеакпажедпулусаже**</span><span class="sxs-lookup"><span data-stu-id="cd646-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-364">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-366">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапеакпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Пиковая квота использования выгружаемого пула")</span><span class="sxs-lookup"><span data-stu-id="cd646-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-367">Пиковая квота использования выгружаемого пула для процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="cd646-368">Пример: 31</span><span class="sxs-lookup"><span data-stu-id="cd646-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="cd646-369">**реадоператионкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-370">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-372">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Реадоператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число операций чтения")</span><span class="sxs-lookup"><span data-stu-id="cd646-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-373">Число выполненных операций чтения.</span><span class="sxs-lookup"><span data-stu-id="cd646-373">Number of read operations performed.</span></span>

<span data-ttu-id="cd646-374">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-375">**реадтрансферкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-376">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-378">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Реадтрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число передач чтения"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-379">Объем считанных данных.</span><span class="sxs-lookup"><span data-stu-id="cd646-379">Amount of data read.</span></span>

<span data-ttu-id="cd646-380">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="cd646-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-382">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-384">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесс состояние \| процесса \_ системы \_ \| SessionID"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор сеанса")</span><span class="sxs-lookup"><span data-stu-id="cd646-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-385">Уникальный идентификатор, создаваемый операционной системой при создании сеанса.</span><span class="sxs-lookup"><span data-stu-id="cd646-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="cd646-386">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="cd646-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-387">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="cd646-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-390">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="cd646-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-391">Это свойство не реализовано и не заполняется ни одним экземпляром этого класса.</span><span class="sxs-lookup"><span data-stu-id="cd646-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="cd646-392">Всегда имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd646-392">It is always **NULL**.</span></span>

<span data-ttu-id="cd646-393">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cd646-394">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="cd646-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cd646-395">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="cd646-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cd646-396">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="cd646-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cd646-397">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="cd646-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd646-398">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="cd646-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cd646-399">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="cd646-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cd646-400">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="cd646-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cd646-401">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="cd646-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cd646-402">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="cd646-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cd646-403">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="cd646-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cd646-404">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="cd646-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cd646-405">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="cd646-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cd646-406">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="cd646-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd646-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="cd646-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-408">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd646-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-410">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Дата завершения")</span><span class="sxs-lookup"><span data-stu-id="cd646-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-411">Процесс остановлен или прерван.</span><span class="sxs-lookup"><span data-stu-id="cd646-411">Process was stopped or terminated.</span></span> <span data-ttu-id="cd646-412">Чтобы получить время завершения, необходимо удерживать маркер процесса открытым.</span><span class="sxs-lookup"><span data-stu-id="cd646-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="cd646-413">В противном случае это свойство возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd646-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="cd646-414">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="cd646-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-416">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd646-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-418">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число потоков")</span><span class="sxs-lookup"><span data-stu-id="cd646-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-419">Число активных потоков в процессе.</span><span class="sxs-lookup"><span data-stu-id="cd646-419">Number of active threads in a process.</span></span> <span data-ttu-id="cd646-420">Инструкция — это базовая единица выполнения в процессоре, а поток — это объект, выполняющий инструкцию.</span><span class="sxs-lookup"><span data-stu-id="cd646-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="cd646-421">Каждый выполняющийся процесс имеет по крайней мере один поток.</span><span class="sxs-lookup"><span data-stu-id="cd646-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="cd646-422">**усермодетиме**</span><span class="sxs-lookup"><span data-stu-id="cd646-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-423">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-425">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("усермодетиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")</span><span class="sxs-lookup"><span data-stu-id="cd646-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-426">Время в пользовательском режиме, в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="cd646-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="cd646-427">Если эта информация недоступна, используйте значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="cd646-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="cd646-428">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-429">**виртуалсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-430">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-432">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Виртуалсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("использование виртуального адресного пространства"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-433">Текущий размер виртуального адресного пространства, используемого процессом, а не физическая или виртуальная память, фактически используемая процессом.</span><span class="sxs-lookup"><span data-stu-id="cd646-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="cd646-434">Использование виртуального адресного пространства не обязательно подразумевает соответствующее использование страниц диска или основной памяти.</span><span class="sxs-lookup"><span data-stu-id="cd646-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="cd646-435">Виртуальное пространство, конечное, и слишком много, процесс может не суметь загрузить библиотеки.</span><span class="sxs-lookup"><span data-stu-id="cd646-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="cd646-436">Это значение согласуется с тем, что отображается в Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="cd646-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="cd646-437">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="cd646-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd646-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-441">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и функции потока \| Жетпроцессверсион"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("версия Windows")</span><span class="sxs-lookup"><span data-stu-id="cd646-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-442">Версия Windows, в которой выполняется процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="cd646-443">Пример: 4,0</span><span class="sxs-lookup"><span data-stu-id="cd646-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="cd646-444">**воркингсетсизе**</span><span class="sxs-lookup"><span data-stu-id="cd646-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-445">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-447">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("размер рабочего множества"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-448">Объем памяти в байтах, который должен эффективно выполняться процессом — для операционной системы, использующей управление памятью на основе страниц.</span><span class="sxs-lookup"><span data-stu-id="cd646-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="cd646-449">Если в системе недостаточно памяти (меньше размера рабочего набора), пробуксовка происходит.</span><span class="sxs-lookup"><span data-stu-id="cd646-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="cd646-450">Если размер рабочего набора неизвестен, используйте **значение NULL** или 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="cd646-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="cd646-451">Если предоставлены данные рабочего набора, можно отслеживать эти сведения, чтобы понять, как изменяются требования к памяти для процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="cd646-452">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="cd646-453">Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-454">**вритеоператионкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-455">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-457">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Вритеоператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число операций записи")</span><span class="sxs-lookup"><span data-stu-id="cd646-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-458">Число выполненных операций записи.</span><span class="sxs-lookup"><span data-stu-id="cd646-458">Number of write operations performed.</span></span>

<span data-ttu-id="cd646-459">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd646-460">**вритетрансферкаунт**</span><span class="sxs-lookup"><span data-stu-id="cd646-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd646-461">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd646-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd646-462">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd646-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd646-463">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Вритетрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число передач записи"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="cd646-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cd646-464">Объем записанных данных.</span><span class="sxs-lookup"><span data-stu-id="cd646-464">Amount of data written.</span></span>

<span data-ttu-id="cd646-465">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd646-466">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd646-466">Remarks</span></span>

<span data-ttu-id="cd646-467">Класс **\_ процесса Win32** является производным от [**\_ процесса CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="cd646-468">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="cd646-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="cd646-469">Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="cd646-470">Обзор</span><span class="sxs-lookup"><span data-stu-id="cd646-470">Overview</span></span>

<span data-ttu-id="cd646-471">Процессы лежат практически на всех компьютерах, происходящих на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd646-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="cd646-472">На самом деле, основная причина большинства проблем с компьютером может быть отслежена на процессах. Например, на компьютере может быть запущено слишком много процессов (и зависит от ограниченного набора ресурсов), или же один процесс может использовать больше ресурсов, чем общий ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd646-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="cd646-473">Эти факторы важны для того, чтобы следить за процессами, выполняемыми на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd646-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="cd646-474">Наблюдение за процессом, главное действие в управлении процессами, позволяет определить, что компьютер действительно делает, какие приложения работают и каким образом влияют изменения в вычислительной среде.</span><span class="sxs-lookup"><span data-stu-id="cd646-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="cd646-475">Мониторинг процесса</span><span class="sxs-lookup"><span data-stu-id="cd646-475">Monitoring a Process</span></span>

<span data-ttu-id="cd646-476">Мониторинг процессов на регулярной основе помогает убедиться, что компьютер работает с пиковой эффективностью и что он выполняет свои задачи надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cd646-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="cd646-477">Например, мониторинг процессов позволяет немедленно получить уведомления о любом приложении, которое перестало отвечать, а затем выполнить действия по завершению этого процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="cd646-478">Кроме того, мониторинг процессов позволяет выявление проблем до их возникновения.</span><span class="sxs-lookup"><span data-stu-id="cd646-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="cd646-479">Например, при многократной проверке объема памяти, используемой процессом, можно выявлять утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="cd646-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="cd646-480">Затем можно остановить процесс, чтобы приложение аномального использовало всю доступную память и переведет компьютер в остановленное расположение.</span><span class="sxs-lookup"><span data-stu-id="cd646-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="cd646-481">Мониторинг процессов также помогает минимизировать перерывы, вызванные запланированными простои для обновления и обслуживания.</span><span class="sxs-lookup"><span data-stu-id="cd646-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="cd646-482">Например, проверка состояния приложения базы данных, выполняющегося на клиентских компьютерах, позволяет определить влияние перевода базы данных в режим «вне сети» для обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="cd646-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="cd646-483">Наблюдение за доступностью процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-483">Monitoring process availability.</span></span> <span data-ttu-id="cd646-484">Измеряет процент времени, в течение которого доступен процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="cd646-485">Доступность обычно отслеживается с помощью простой проверки, которая сообщает, работает ли процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="cd646-486">Отслеживая результаты каждой пробы, можно вычислить доступность процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="cd646-487">Например, процесс, проверенный 100 раз и отвечающий на 95 из этих событий, имеет уровень доступности 95%.</span><span class="sxs-lookup"><span data-stu-id="cd646-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="cd646-488">Этот тип мониторинга обычно зарезервирован для баз данных, почтовых программ и других приложений, которые должны выполняться в любое время.</span><span class="sxs-lookup"><span data-stu-id="cd646-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="cd646-489">Он не подходит для программ обработки текста, электронных таблиц или других приложений, которые обычно запускаются и останавливаются несколько раз в день.</span><span class="sxs-lookup"><span data-stu-id="cd646-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="cd646-490">Для настройки процесса можно создать экземпляр класса [**Win32 \_ процессстартуп**](win32-processstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="cd646-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="cd646-491">Производительность процесса можно отслеживать с помощью класса [**\_ \_ \_ процесса Win32 перфформаттеддата PERFPROC**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) и объекта обновления WMI, например [**свбемрефрешер**](../wmisdk/swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="cd646-492">Дополнительные сведения см. в разделе [наблюдение за данными производительности](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cd646-493">Примеры</span><span class="sxs-lookup"><span data-stu-id="cd646-493">Examples</span></span>

<span data-ttu-id="cd646-494">В [списке свойств классов WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) . пример кода PowerShell в коллекции TechNet описывается класс **\_ процесса Win32** и результаты выводятся в формате Excel.</span><span class="sxs-lookup"><span data-stu-id="cd646-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="cd646-495">Процесс [завершения процесса на нескольких серверах](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) прерывает процесс, выполняющийся на одном или нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="cd646-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="cd646-496">В примере в разделе [вызов метода поставщика](../wmisdk/example--calling-a-provider-method.md) код использует C++ для вызова **\_ процесса Win32** для создания процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="cd646-497">Доступность — это простейшая форма мониторинга процессов. при таком подходе вы просто убедитесь, что процесс выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd646-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="cd646-498">При наблюдении за доступностью процессов обычно извлекается список процессов, запущенных на компьютере, а затем проверяется, активен ли конкретный процесс.</span><span class="sxs-lookup"><span data-stu-id="cd646-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="cd646-499">Если процесс активен, он считается доступным.</span><span class="sxs-lookup"><span data-stu-id="cd646-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="cd646-500">Если процесс неактивен, он недоступен.</span><span class="sxs-lookup"><span data-stu-id="cd646-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="cd646-501">Следующий пример сценария VBScript отслеживает доступность процесса, проверяя список запущенных на компьютере процессов и выдавая уведомление, если процесс Database.exe не найден.</span><span class="sxs-lookup"><span data-stu-id="cd646-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="cd646-502">Следующий пример VBScript отслеживает создание процессов с помощью временного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="cd646-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="cd646-503">Следующая команда VBScript отслеживает сведения о производительности процесса.</span><span class="sxs-lookup"><span data-stu-id="cd646-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="cd646-504">В следующем примере кода VBScript показано, как получить сведения о владельце каждого процесса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd646-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="cd646-505">Этот сценарий можно использовать для получения данных с удаленного компьютера, например, чтобы определить, какие пользователи имеют процессы, выполняющие сервер терминалов, подставьте имя удаленного компьютера для "." в первой строке.</span><span class="sxs-lookup"><span data-stu-id="cd646-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="cd646-506">Кроме того, необходимо быть администратором на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd646-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="cd646-507">В следующем примере кода VBScript показано, как получить сеанс входа, связанный с выполняющимся процессом.</span><span class="sxs-lookup"><span data-stu-id="cd646-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="cd646-508">Процесс должен выполняться Notepad.exe перед запуском скрипта.</span><span class="sxs-lookup"><span data-stu-id="cd646-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="cd646-509">В примере находятся экземпляры [**Win32 \_ LogonSession**](win32-logonsession.md) , связанные с **\_ процессом Win32** , который представляет Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="cd646-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="cd646-510">[**Win32 \_ Сессионпроцесс**](win32-sessionprocess.md) указывается в качестве класса ассоциации.</span><span class="sxs-lookup"><span data-stu-id="cd646-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="cd646-511">Дополнительные сведения см. в разделе [соединители оператора.](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cd646-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="cd646-512">Требования</span><span class="sxs-lookup"><span data-stu-id="cd646-512">Requirements</span></span>



| <span data-ttu-id="cd646-513">Требование</span><span class="sxs-lookup"><span data-stu-id="cd646-513">Requirement</span></span> | <span data-ttu-id="cd646-514">Значение</span><span class="sxs-lookup"><span data-stu-id="cd646-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd646-515">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd646-515">Minimum supported client</span></span><br/> | <span data-ttu-id="cd646-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd646-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd646-517">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd646-517">Minimum supported server</span></span><br/> | <span data-ttu-id="cd646-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd646-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd646-519">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd646-519">Namespace</span></span><br/>                | <span data-ttu-id="cd646-520">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cd646-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd646-521">MOF</span><span class="sxs-lookup"><span data-stu-id="cd646-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd646-522"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd646-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd646-523">DLL</span><span class="sxs-lookup"><span data-stu-id="cd646-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd646-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd646-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd646-525">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd646-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd646-526">**\_Процесс CIM**</span><span class="sxs-lookup"><span data-stu-id="cd646-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="cd646-527">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="cd646-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="cd646-528">Задачи WMI: процессы</span><span class="sxs-lookup"><span data-stu-id="cd646-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
