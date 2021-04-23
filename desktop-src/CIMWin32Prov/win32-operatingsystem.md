---
description: Представляет операционную систему на основе Windows, установленную на компьютере.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Класс Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262749"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="71fdc-103">\_Класс операционной системы Win32</span><span class="sxs-lookup"><span data-stu-id="71fdc-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="71fdc-104">[Класс WMI](../wmisdk/retrieving-a-class.md) операционной системы **Win32 \_** , представляющий собой операционную систему на основе Windows, установленную на компьютере.</span><span class="sxs-lookup"><span data-stu-id="71fdc-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="71fdc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="71fdc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71fdc-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="71fdc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71fdc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71fdc-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="71fdc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="71fdc-108">Members</span></span>

<span data-ttu-id="71fdc-109">Класс **\_ операционной системы Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="71fdc-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="71fdc-110">Методы</span><span class="sxs-lookup"><span data-stu-id="71fdc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="71fdc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="71fdc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="71fdc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="71fdc-112">Methods</span></span>

<span data-ttu-id="71fdc-113">Класс **\_ операционной системы Win32** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="71fdc-114">Метод</span><span class="sxs-lookup"><span data-stu-id="71fdc-114">Method</span></span>                                                                                     | <span data-ttu-id="71fdc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="71fdc-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71fdc-116">**Перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="71fdc-117">Завершает работу и перезапускает компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="71fdc-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="71fdc-118">**сетдатетиме**</span><span class="sxs-lookup"><span data-stu-id="71fdc-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="71fdc-119">Позволяет задать дату и время компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="71fdc-120">**Закрытия**</span><span class="sxs-lookup"><span data-stu-id="71fdc-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="71fdc-121">Выгружает программы и библиотеки DLL до точки, в которой можно отключить компьютер.</span><span class="sxs-lookup"><span data-stu-id="71fdc-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="71fdc-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="71fdc-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="71fdc-123">Предоставляет полный набор параметров завершения работы, поддерживаемых операционными системами Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="71fdc-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="71fdc-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="71fdc-125">Предоставляет тот же набор параметров завершения работы, который поддерживает метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) в **Win32 \_ операционной** системы, но также позволяет указать комментарии, причину завершения работы или время ожидания.</span><span class="sxs-lookup"><span data-stu-id="71fdc-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="71fdc-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="71fdc-126">Properties</span></span>

<span data-ttu-id="71fdc-127">Класс **\_ операционной системы Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="71fdc-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71fdc-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="71fdc-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-131">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ сведения о сопоставлении дисков \_ \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="71fdc-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-132">Имя диска, с которого запускается операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="71fdc-133">Пример: " \\ \\ \\ Harddisk0 устройства"</span><span class="sxs-lookup"><span data-stu-id="71fdc-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="71fdc-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| двбуилднумбер")</span><span class="sxs-lookup"><span data-stu-id="71fdc-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-138">Номер сборки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-138">Build number of an operating system.</span></span> <span data-ttu-id="71fdc-139">Его можно использовать для более точных сведений о версии, чем номера выпускаемой версии продукта.</span><span class="sxs-lookup"><span data-stu-id="71fdc-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="71fdc-140">Пример: "1381"</span><span class="sxs-lookup"><span data-stu-id="71fdc-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-141">**буилдтипе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-144">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| курренттипе")</span><span class="sxs-lookup"><span data-stu-id="71fdc-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-145">Тип сборки, используемой для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="71fdc-146">Примеры: "" Розничная Сборка "", "" проверенная сборка ""</span><span class="sxs-lookup"><span data-stu-id="71fdc-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-147">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="71fdc-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-150">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="71fdc-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-151">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="71fdc-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="71fdc-152">Строка включает версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-152">The string includes the operating system version.</span></span> <span data-ttu-id="71fdc-153">Например, "Microsoft Windows 7 Корпоративная".</span><span class="sxs-lookup"><span data-stu-id="71fdc-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="71fdc-154">Это свойство может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="71fdc-154">This property can be localized.</span></span>

<span data-ttu-id="71fdc-155">**Windows Vista и Windows 7:** Это свойство может содержать конечные символы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="71fdc-156">Например, для получения сведений с помощью этого свойства может потребоваться строка "Microsoft Windows 7 Корпоративная" (конечная область).</span><span class="sxs-lookup"><span data-stu-id="71fdc-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="71fdc-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-158">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="71fdc-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-161">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ идефаултансикодепаже")</span><span class="sxs-lookup"><span data-stu-id="71fdc-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-162">Значение кодовой страницы, используемой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="71fdc-162">Code page value an operating system uses.</span></span> <span data-ttu-id="71fdc-163">Кодовая страница содержит таблицу символов, которую операционная система использует для преобразования строк для разных языков.</span><span class="sxs-lookup"><span data-stu-id="71fdc-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="71fdc-164">В Американский национальный институт стандартов (ANSI) (ANSI) перечислены значения, представляющие определенные кодовые страницы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="71fdc-165">Если операционная система не использует кодовую страницу ANSI, для этого элемента устанавливается значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="71fdc-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="71fdc-166">Для определения значения кодовой страницы в строке **набора кода** может использоваться не более шести символов.</span><span class="sxs-lookup"><span data-stu-id="71fdc-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="71fdc-167">Пример: "1255"</span><span class="sxs-lookup"><span data-stu-id="71fdc-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="71fdc-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-171">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| язык \_ икаунтри")</span><span class="sxs-lookup"><span data-stu-id="71fdc-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-172">Код для страны или региона, который использует операционная система.</span><span class="sxs-lookup"><span data-stu-id="71fdc-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="71fdc-173">Значения основаны на международных префиксах телефонных номеров, которые также называются кодами страны и региона IBM.</span><span class="sxs-lookup"><span data-stu-id="71fdc-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="71fdc-174">Это свойство может использовать не более шести символов для определения значения кода страны или региона.</span><span class="sxs-lookup"><span data-stu-id="71fdc-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="71fdc-175">Пример: "1" (США)</span><span class="sxs-lookup"><span data-stu-id="71fdc-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71fdc-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-179">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71fdc-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-180">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71fdc-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="71fdc-181">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="71fdc-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="71fdc-182">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-183">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="71fdc-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-186">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71fdc-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-187">Имя класса создания для системы компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="71fdc-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="71fdc-188">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="71fdc-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-192">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **сзксдверсион**")</span><span class="sxs-lookup"><span data-stu-id="71fdc-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-193">Строка **, заканчивающаяся нулем и** указывающая на последний пакет обновления, установленный на компьютере.</span><span class="sxs-lookup"><span data-stu-id="71fdc-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="71fdc-194">Если пакет обновления не установлен, строка имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="71fdc-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="71fdc-195">Пример: "пакет обновления 3"</span><span class="sxs-lookup"><span data-stu-id="71fdc-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="71fdc-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-199">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="71fdc-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-200">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="71fdc-201">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-202">**курренттимезоне**</span><span class="sxs-lookup"><span data-stu-id="71fdc-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-203">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="71fdc-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-205">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="71fdc-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-206">Число (в минутах), в течение которого операционная система смещается от среднего времени по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="71fdc-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="71fdc-207">Число может быть положительным, отрицательным или нулевым.</span><span class="sxs-lookup"><span data-stu-id="71fdc-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="71fdc-208">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-209">**Датаексекутионпревентион \_ 32BitApplications**</span><span class="sxs-lookup"><span data-stu-id="71fdc-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-210">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-212">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-213">Если функция предотвращения выполнения данных доступна, это свойство указывает, что эта функция настроена для работы в 32-разрядных приложениях, если **значение true**.</span><span class="sxs-lookup"><span data-stu-id="71fdc-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="71fdc-214">На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище [данные конфигурации загрузки (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) , а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="71fdc-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-215">**Датаексекутионпревентион \_ доступно**</span><span class="sxs-lookup"><span data-stu-id="71fdc-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-218">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-219">Предотвращение выполнения данных — это аппаратная функция для предотвращения атак переполнения буфера путем остановки выполнения кода на страницах памяти типа данных.</span><span class="sxs-lookup"><span data-stu-id="71fdc-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="71fdc-220">Если **значение — true**, эта функция доступна.</span><span class="sxs-lookup"><span data-stu-id="71fdc-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="71fdc-221">На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище BCD, а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="71fdc-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-222">**\_Драйверы датаексекутионпревентион**</span><span class="sxs-lookup"><span data-stu-id="71fdc-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-223">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-225">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-226">Если функция предотвращения выполнения данных доступна, это свойство указывает, что эта функция настроена для работы с драйверами, если имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="71fdc-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="71fdc-227">На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище BCD, а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="71fdc-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-228">**Датаексекутионпревентион \_ суппортполици**</span><span class="sxs-lookup"><span data-stu-id="71fdc-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-229">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71fdc-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-231">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-232">Указывает, какой параметр предотвращения выполнения данных (DEP) применяется.</span><span class="sxs-lookup"><span data-stu-id="71fdc-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="71fdc-233">Параметр DEP определяет степень применения DEP к 32-разрядным приложениям в системе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="71fdc-234">Функция DEP всегда применяется к ядру Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="71fdc-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Всегда выкл** . (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-236">Функция DEP отключена для всех 32-разрядных приложений на компьютере без исключений.</span><span class="sxs-lookup"><span data-stu-id="71fdc-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="71fdc-237">Этот параметр недоступен для пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="71fdc-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="71fdc-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-239">Функция DEP включена для всех 32-разрядных приложений на компьютере.</span><span class="sxs-lookup"><span data-stu-id="71fdc-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="71fdc-240">Этот параметр недоступен для пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="71fdc-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="71fdc-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Согласие на участие** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-242">Функция DEP включена для ограниченного числа двоичных файлов, ядра и всех служб на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="71fdc-243">Однако он по умолчанию отключен для всех 32-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="71fdc-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="71fdc-244">Пользователь или администратор должен явно выбрать параметр **Always on** или **отказаться от согласия** , прежде чем DEP можно будет применить к 32-разрядным приложениям.</span><span class="sxs-lookup"><span data-stu-id="71fdc-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="71fdc-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Отказ от участия** (3)</span><span class="sxs-lookup"><span data-stu-id="71fdc-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-246">Функция DEP включена по умолчанию для всех 32-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="71fdc-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="71fdc-247">Пользователь или администратор может явно удалить поддержку 32-разрядного приложения, добавив приложение в список исключений.</span><span class="sxs-lookup"><span data-stu-id="71fdc-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-248">**Отладка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-249">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-251">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ Debug")</span><span class="sxs-lookup"><span data-stu-id="71fdc-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-252">Операционная система — это проверенная (Отладка) сборка.</span><span class="sxs-lookup"><span data-stu-id="71fdc-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="71fdc-253">Если **значение — true**, устанавливается версия отладки.</span><span class="sxs-lookup"><span data-stu-id="71fdc-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="71fdc-254">Проверенные сборки предоставляют проверку ошибок, проверку аргументов и код отладки системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="71fdc-255">Дополнительный код в проверяемом двоичном файле создает сообщение об ошибке отладчика ядра и разбивается на отладчик.</span><span class="sxs-lookup"><span data-stu-id="71fdc-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="71fdc-256">Это позволяет немедленно определить причину ошибки и ее расположение.</span><span class="sxs-lookup"><span data-stu-id="71fdc-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="71fdc-257">На производительность может повлиять в проверенной сборке из-за дополнительного выполняемого кода.</span><span class="sxs-lookup"><span data-stu-id="71fdc-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-258">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71fdc-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-260">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="71fdc-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-261">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Описание"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-262">Описание операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-262">Description of the Windows operating system.</span></span> <span data-ttu-id="71fdc-263">Некоторые пользовательские интерфейсы, например, позволяющие изменять это описание, ограничивают его длину до 48 символов.</span><span class="sxs-lookup"><span data-stu-id="71fdc-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-264">**Распределяемый**</span><span class="sxs-lookup"><span data-stu-id="71fdc-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-265">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-267">Если **значение равно true**, операционная система распространяется на несколько узлов системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="71fdc-268">В этом случае эти узлы должны быть сгруппированы как кластер.</span><span class="sxs-lookup"><span data-stu-id="71fdc-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="71fdc-269">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="71fdc-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-271">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-273">Уровень шифрования для безопасных транзакций: 40-разрядная, 128-разрядная или *n*-разрядная.</span><span class="sxs-lookup"><span data-stu-id="71fdc-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="71fdc-274">**40-разрядная** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="71fdc-275">**128-разрядная** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="71fdc-276">**n-разрядная** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-277">**фореграундаппликатионбуст**</span><span class="sxs-lookup"><span data-stu-id="71fdc-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-278">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71fdc-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-279">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="71fdc-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-280">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ приоритиконтрол \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="71fdc-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-281">Повышение приоритета назначается для приложения переднего плана.</span><span class="sxs-lookup"><span data-stu-id="71fdc-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="71fdc-282">Повышение производительности приложения реализуется путем предоставления приложению дополнительных срезов времени выполнения (длина тактовой задержки).</span><span class="sxs-lookup"><span data-stu-id="71fdc-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="71fdc-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-284">Система увеличивает тактовую длину на 6.</span><span class="sxs-lookup"><span data-stu-id="71fdc-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="71fdc-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Минимум** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-286">Система увеличивает тактовую длину на 12.</span><span class="sxs-lookup"><span data-stu-id="71fdc-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="71fdc-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-288">Система увеличивает тактовую длину на 18.</span><span class="sxs-lookup"><span data-stu-id="71fdc-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-289">**фрифисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="71fdc-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-290">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-292">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-293">Число (в килобайтах) физической памяти, неиспользуемой и доступной в данный момент.</span><span class="sxs-lookup"><span data-stu-id="71fdc-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="71fdc-294">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-295">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-296">**фриспацеинпагингфилес**</span><span class="sxs-lookup"><span data-stu-id="71fdc-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-297">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-299">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Параметры системной памяти DMTF \| 001,4 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-300">Число (в килобайтах), которое можно сопоставить с файлами подкачки операционной системы, не заставляя другие страницы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="71fdc-301">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-302">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-303">**фривиртуалмемори**</span><span class="sxs-lookup"><span data-stu-id="71fdc-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-304">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-306">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-307">Число (в килобайтах) виртуальной памяти, неиспользуемой и доступной в данный момент.</span><span class="sxs-lookup"><span data-stu-id="71fdc-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="71fdc-308">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-309">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71fdc-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-311">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71fdc-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-313">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-314">Объект Date установлен.</span><span class="sxs-lookup"><span data-stu-id="71fdc-314">Date object was installed.</span></span> <span data-ttu-id="71fdc-315">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="71fdc-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="71fdc-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-317">**ларжесистемкаче**</span><span class="sxs-lookup"><span data-stu-id="71fdc-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-318">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-320">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="71fdc-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-321">Это свойство устарело и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71fdc-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="71fdc-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Оптимизировать для приложений** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-323">Оптимизируйте память для приложений.</span><span class="sxs-lookup"><span data-stu-id="71fdc-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="71fdc-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Оптимизировать для производительности системы** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-325">Оптимизируйте память для повышения производительности системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="71fdc-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-327">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71fdc-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-329">Дата и время последнего перезапуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="71fdc-330">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="71fdc-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-332">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71fdc-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-334">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. В файле IETF \| Host-Resources-MIB. хрсистемдате "," MIF. \|Общие сведения о DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-335">Версия операционной системы для локальной даты и времени суток.</span><span class="sxs-lookup"><span data-stu-id="71fdc-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="71fdc-336">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-337">**Локаль**</span><span class="sxs-lookup"><span data-stu-id="71fdc-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-340">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| язык \_ илангуаже")</span><span class="sxs-lookup"><span data-stu-id="71fdc-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-341">Идентификатор языка, используемый операционной системой.</span><span class="sxs-lookup"><span data-stu-id="71fdc-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="71fdc-342">Идентификатор языка — это стандартное Международный цифровой сокращенный номер страны или региона.</span><span class="sxs-lookup"><span data-stu-id="71fdc-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="71fdc-343">Каждый язык имеет уникальный идентификатор языка (LANGID), 16-разрядное значение, состоящее из основного идентификатора языка и вторичного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="71fdc-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-344">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="71fdc-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-347">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-348">Имя производителя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="71fdc-349">Для систем на основе Windows это значение равно «Корпорация Майкрософт».</span><span class="sxs-lookup"><span data-stu-id="71fdc-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-350">**макснумберофпроцессес**</span><span class="sxs-lookup"><span data-stu-id="71fdc-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-351">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-353">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистеммакспроцессес ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-354">Максимальное число контекстов процессов, которое может поддерживать операционная система.</span><span class="sxs-lookup"><span data-stu-id="71fdc-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="71fdc-355">Значение по умолчанию, заданное поставщиком, — 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="71fdc-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="71fdc-356">Если фиксированного максимума нет, значение должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="71fdc-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="71fdc-357">В системах с фиксированным максимальным значением этот объект может помочь в диагностике сбоев, возникающих при достижении максимального значения (если неизвестно, введите 4294967295 (0xFFFFFFFF)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="71fdc-358">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-359">**макспроцессмеморисизе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-360">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-362">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-363">Максимальное число (в килобайтах) памяти, которое может быть выделено процессу.</span><span class="sxs-lookup"><span data-stu-id="71fdc-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="71fdc-364">Для операционных систем без виртуальной памяти обычно это значение равно общему объему физической памяти за вычетом памяти, используемой BIOS и операционной системой.</span><span class="sxs-lookup"><span data-stu-id="71fdc-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="71fdc-365">Для некоторых операционных систем это значение может быть бесконечным, в этом случае следует указать 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="71fdc-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="71fdc-366">В других случаях это значение может быть константой, например 2G или 4G.</span><span class="sxs-lookup"><span data-stu-id="71fdc-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="71fdc-367">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-368">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-369">**муилангуажес**</span><span class="sxs-lookup"><span data-stu-id="71fdc-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-370">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="71fdc-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-372">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-373">Языки многоязыкового интерфейса пользователя (MUI Pack), установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="71fdc-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="71fdc-374">Например, "en-US".</span><span class="sxs-lookup"><span data-stu-id="71fdc-374">For example, "en-us".</span></span> <span data-ttu-id="71fdc-375">Языки пакета MUI — это файлы ресурсов, которые можно установить в английской версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="71fdc-376">При установке пакета MUI можно изменить язык пользовательского интерфейса на один из поддерживаемых языков 33.</span><span class="sxs-lookup"><span data-stu-id="71fdc-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-377">**Name**</span><span class="sxs-lookup"><span data-stu-id="71fdc-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-378">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-380">Экземпляр операционной системы в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="71fdc-381">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-382">**нумберофлиценседусерс**</span><span class="sxs-lookup"><span data-stu-id="71fdc-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-383">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-385">Число пользовательских лицензий для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="71fdc-386">Если значение не ограничено, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="71fdc-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="71fdc-387">Если значение неизвестно, введите-1.</span><span class="sxs-lookup"><span data-stu-id="71fdc-387">If unknown, enter -1.</span></span>

<span data-ttu-id="71fdc-388">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-389">**нумберофпроцессес**</span><span class="sxs-lookup"><span data-stu-id="71fdc-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-390">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-392">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемпроцессес ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-393">Количество контекстов процессов, загруженных или выполняемых в операционной системе в данный момент.</span><span class="sxs-lookup"><span data-stu-id="71fdc-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="71fdc-394">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-395">**нумберофусерс**</span><span class="sxs-lookup"><span data-stu-id="71fdc-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-396">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-398">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемнумусерс ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-399">Число пользовательских сеансов, для которых в настоящее время хранятся сведения о состоянии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="71fdc-400">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-401">**оператингсистемску**</span><span class="sxs-lookup"><span data-stu-id="71fdc-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-402">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-404">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-405">Номер SKU для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="71fdc-406">Эти значения совпадают с константами \**Product \_ \** _, определенными в Winnt. h, которые используются с функцией [_ *жетпродуктинфо* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="71fdc-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="71fdc-407">В следующем списке перечислены возможные значения номера SKU.</span><span class="sxs-lookup"><span data-stu-id="71fdc-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="71fdc-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Продукт \_ Не ОПРЕДЕЛЕНо** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-409">Не определено.</span><span class="sxs-lookup"><span data-stu-id="71fdc-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="71fdc-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Продукт \_ ULTIMATE** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-411">Ultimate Edition, например Windows Vista Ultimate.</span><span class="sxs-lookup"><span data-stu-id="71fdc-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="71fdc-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Продукт \_ ДОМАШНяя \_ Базовая** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-413">Выпуск Home Basic</span><span class="sxs-lookup"><span data-stu-id="71fdc-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="71fdc-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Продукт \_ ДОМАШНяя \_ Расширенная** (3)</span><span class="sxs-lookup"><span data-stu-id="71fdc-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-415">Выпуск Home Premium</span><span class="sxs-lookup"><span data-stu-id="71fdc-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="71fdc-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Продукт \_ ENTERPRISE** (4)</span><span class="sxs-lookup"><span data-stu-id="71fdc-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-417">Выпуск Enterprise</span><span class="sxs-lookup"><span data-stu-id="71fdc-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="71fdc-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Продукт \_ Бизнес** (6)</span><span class="sxs-lookup"><span data-stu-id="71fdc-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="71fdc-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Продукт \_ Стандартный \_ сервер** (7)</span><span class="sxs-lookup"><span data-stu-id="71fdc-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-421">Windows Server Standard Edition (Установка возможностей рабочего стола)</span><span class="sxs-lookup"><span data-stu-id="71fdc-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="71fdc-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Продукт \_ Сервер DATACENTER \_ Server** (8)</span><span class="sxs-lookup"><span data-stu-id="71fdc-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-423">Windows Server Datacenter Edition (Установка возможностей рабочего стола)</span><span class="sxs-lookup"><span data-stu-id="71fdc-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="71fdc-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Продукт \_ \_Сервер смаллбусинесс** (9)</span><span class="sxs-lookup"><span data-stu-id="71fdc-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-425">Выпуск Small Business Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="71fdc-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Продукт \_ \_Сервер предприятия** (10)</span><span class="sxs-lookup"><span data-stu-id="71fdc-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-427">Выпуск Enterprise Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="71fdc-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Продукт \_ НАЧАЛЬная** (11)</span><span class="sxs-lookup"><span data-stu-id="71fdc-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="71fdc-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Продукт \_ Ядро DATACENTER \_ Server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="71fdc-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-431">Выпуск Datacenter Server Core</span><span class="sxs-lookup"><span data-stu-id="71fdc-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="71fdc-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Продукт \_ STANDARD \_ Server \_ Core** (13)</span><span class="sxs-lookup"><span data-stu-id="71fdc-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-433">Выпуск Standard Server Core</span><span class="sxs-lookup"><span data-stu-id="71fdc-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="71fdc-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Продукт \_ ENTERPRISE \_ Server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="71fdc-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-435">Выпуск Enterprise Server Core</span><span class="sxs-lookup"><span data-stu-id="71fdc-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="71fdc-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Продукт \_ ВЕБ- \_ сервер** (17)</span><span class="sxs-lookup"><span data-stu-id="71fdc-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-437">Выпуск Web Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="71fdc-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Продукт \_ ДОМАШНИЙ \_ сервер** (19)</span><span class="sxs-lookup"><span data-stu-id="71fdc-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-439">Выпуск Home Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="71fdc-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Продукт \_ \_Сервер Storage Express \_ Server** (20)</span><span class="sxs-lookup"><span data-stu-id="71fdc-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-441">Выпуск Storage Express Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="71fdc-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Продукт \_ \_Стандартный \_ сервер хранилища** (21)</span><span class="sxs-lookup"><span data-stu-id="71fdc-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-443">Windows Storage Server Standard Edition (Установка возможностей рабочего стола)</span><span class="sxs-lookup"><span data-stu-id="71fdc-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="71fdc-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Продукт \_ STORAGE \_ Workgroup \_ Server** (22)</span><span class="sxs-lookup"><span data-stu-id="71fdc-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-445">Windows Storage Server Workgroup Edition (Установка возможностей рабочего стола)</span><span class="sxs-lookup"><span data-stu-id="71fdc-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="71fdc-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Продукт \_ \_Сервер хранилища Enterprise \_ Server** (23)</span><span class="sxs-lookup"><span data-stu-id="71fdc-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-447">Выпуск хранилища Enterprise Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="71fdc-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Продукт \_ СЕРВЕР \_ для \_ смаллбусинесс** (24)</span><span class="sxs-lookup"><span data-stu-id="71fdc-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-449">Сервер для Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="71fdc-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Продукт \_ СМАЛЛБУСИНЕСС \_ Server \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="71fdc-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-451">Выпуск Small Business Server Premium</span><span class="sxs-lookup"><span data-stu-id="71fdc-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="71fdc-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Продукт \_ Корпоративный \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="71fdc-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-453">Windows Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="71fdc-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Продукт \_ ULTIMATE \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="71fdc-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-455">Выпуск Windows Ultimate</span><span class="sxs-lookup"><span data-stu-id="71fdc-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="71fdc-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Продукт \_ \_ \_ Ядро веб-сервера** (29)</span><span class="sxs-lookup"><span data-stu-id="71fdc-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-457">Выпуск Windows Server Web Server (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="71fdc-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Продукт \_ Стандартный \_ сервер \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="71fdc-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-459">Windows Server Standard Edition без Hyper-V</span><span class="sxs-lookup"><span data-stu-id="71fdc-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="71fdc-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Продукт \_ DATACENTER \_ Server \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="71fdc-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-461">Windows Server Datacenter Edition без Hyper-V (полная установка)</span><span class="sxs-lookup"><span data-stu-id="71fdc-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="71fdc-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Продукт \_ ENTERPRISE \_ Server \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="71fdc-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-463">Windows Server Enterprise Edition без Hyper-V (полная установка)</span><span class="sxs-lookup"><span data-stu-id="71fdc-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="71fdc-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Продукт \_ Ядро DATACENTER \_ Server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="71fdc-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-465">Windows Server Datacenter Edition без Hyper-V (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="71fdc-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Продукт \_ STANDARD \_ Server \_ Core \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="71fdc-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-467">Windows Server Standard Edition без Hyper-V (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="71fdc-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Продукт \_ ENTERPRISE \_ Server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="71fdc-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-469">Windows Server Enterprise Edition без Hyper-V (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="71fdc-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Продукт \_ HYPERV** (42)</span><span class="sxs-lookup"><span data-stu-id="71fdc-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="71fdc-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Продукт \_ STORAGE \_ Express \_ Server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="71fdc-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-473">Storage Server Express Edition (Установка Server Core)</span><span class="sxs-lookup"><span data-stu-id="71fdc-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="71fdc-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Продукт \_ ХРАНИЛИЩЕ \_ Standard \_ Server \_ Core** (44)</span><span class="sxs-lookup"><span data-stu-id="71fdc-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-475">Storage Server Standard Edition (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="71fdc-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Продукт \_ ХРАНИЛИЩЕ \_ Server Workgroup, \_ \_ ядро** (45)</span><span class="sxs-lookup"><span data-stu-id="71fdc-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-477">Storage Server Workgroup Edition (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="71fdc-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Продукт \_ \_ \_ \_ Ядро хранилища ENTERPRISE Server** (46)</span><span class="sxs-lookup"><span data-stu-id="71fdc-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-479">Storage Server Workgroup Edition (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="71fdc-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Продукт \_ Профессиональная** (48)</span><span class="sxs-lookup"><span data-stu-id="71fdc-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-481">Windows Professional</span><span class="sxs-lookup"><span data-stu-id="71fdc-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="71fdc-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Продукт \_ \_ \_ Сервер решений SB** (50)</span><span class="sxs-lookup"><span data-stu-id="71fdc-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-483">Windows Server Essentials (Установка возможностей рабочего стола)</span><span class="sxs-lookup"><span data-stu-id="71fdc-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="71fdc-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Продукт \_ СМАЛЛБУСИНЕСС \_ Server \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="71fdc-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-485">Small Business Server Premium (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="71fdc-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Продукт \_ Сервер КЛАСТЕРов версии \_ \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="71fdc-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-487">Windows Compute Cluster Server без Hyper-V</span><span class="sxs-lookup"><span data-stu-id="71fdc-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="71fdc-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Продукт \_ ЯДЕРная \_ ARM** (97)</span><span class="sxs-lookup"><span data-stu-id="71fdc-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="71fdc-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="71fdc-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Продукт \_ ЯДРО** (101)</span><span class="sxs-lookup"><span data-stu-id="71fdc-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-491">Домашняя страница Windows</span><span class="sxs-lookup"><span data-stu-id="71fdc-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="71fdc-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Продукт \_ Профессиональная \_ WMC** (103)</span><span class="sxs-lookup"><span data-stu-id="71fdc-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-493">Windows Professional с Media Center</span><span class="sxs-lookup"><span data-stu-id="71fdc-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="71fdc-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Продукт \_ Мобильные \_ ядра** (104)</span><span class="sxs-lookup"><span data-stu-id="71fdc-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="71fdc-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="71fdc-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Продукт \_ ИОТУАП** (123)</span><span class="sxs-lookup"><span data-stu-id="71fdc-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-497">Основные компоненты Windows IoT (Интернет вещей)</span><span class="sxs-lookup"><span data-stu-id="71fdc-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="71fdc-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Продукт \_ \_Nano \_ Server datacenter** (143)</span><span class="sxs-lookup"><span data-stu-id="71fdc-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-499">Windows Server Datacenter Edition (установка Nano Server)</span><span class="sxs-lookup"><span data-stu-id="71fdc-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="71fdc-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Продукт \_ Стандартный \_ Nano \_ SERVER** (144)</span><span class="sxs-lookup"><span data-stu-id="71fdc-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-501">Windows Server Standard Edition (установка Nano Server)</span><span class="sxs-lookup"><span data-stu-id="71fdc-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="71fdc-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Продукт \_ Ядро DATACENTER \_ WS \_ Server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="71fdc-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-503">Windows Server Datacenter Edition (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="71fdc-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Продукт \_ СТАНДАРТНОЕ \_ \_ \_ ядро WS Server** (148)</span><span class="sxs-lookup"><span data-stu-id="71fdc-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-505">Windows Server Standard Edition (установка основных серверных компонентов)</span><span class="sxs-lookup"><span data-stu-id="71fdc-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-506">**Организация**</span><span class="sxs-lookup"><span data-stu-id="71fdc-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-507">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-508">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-509">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="71fdc-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-510">Название компании для зарегистрированного пользователя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="71fdc-511">Пример: "Корпорация Майкрософт"</span><span class="sxs-lookup"><span data-stu-id="71fdc-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="71fdc-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-513">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-515">Архитектура операционной системы, в отличие от процессора.</span><span class="sxs-lookup"><span data-stu-id="71fdc-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="71fdc-516">Это свойство может быть локализовано.</span><span class="sxs-lookup"><span data-stu-id="71fdc-516">This property can be localized.</span></span>

<span data-ttu-id="71fdc-517">Пример: 32-bit</span><span class="sxs-lookup"><span data-stu-id="71fdc-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="71fdc-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-519">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-520">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-521">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| умолчанию панель управления" язык и \\ \\ \\ \\ региональные \| стандарты ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-522">Языковая версия установленной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-522">Language version of the operating system installed.</span></span> <span data-ttu-id="71fdc-523">В следующем списке перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="71fdc-523">The following list lists the possible values.</span></span> <span data-ttu-id="71fdc-524">Пример: 0x0807 (немецкий, Швейцария).</span><span class="sxs-lookup"><span data-stu-id="71fdc-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="71fdc-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-526">Арабский</span><span class="sxs-lookup"><span data-stu-id="71fdc-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="71fdc-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-528">Китайский (упрощенное письмо) — Китай</span><span class="sxs-lookup"><span data-stu-id="71fdc-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="71fdc-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-530">Английский</span><span class="sxs-lookup"><span data-stu-id="71fdc-530">English</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="71fdc-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-532">Арабский — Саудовская Аравия</span><span class="sxs-lookup"><span data-stu-id="71fdc-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="71fdc-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-534">Болгарский</span><span class="sxs-lookup"><span data-stu-id="71fdc-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="71fdc-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-536">Каталонский</span><span class="sxs-lookup"><span data-stu-id="71fdc-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="71fdc-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-538">Китайский (традиционное письмо) — Тайвань</span><span class="sxs-lookup"><span data-stu-id="71fdc-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="71fdc-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-540">Чешский</span><span class="sxs-lookup"><span data-stu-id="71fdc-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="71fdc-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-542">Датский</span><span class="sxs-lookup"><span data-stu-id="71fdc-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="71fdc-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-544">Немецкий (Германия)</span><span class="sxs-lookup"><span data-stu-id="71fdc-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="71fdc-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-546">Греческий</span><span class="sxs-lookup"><span data-stu-id="71fdc-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-547">1033 (0x409)</span><span class="sxs-lookup"><span data-stu-id="71fdc-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-548">Английский — США</span><span class="sxs-lookup"><span data-stu-id="71fdc-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-549">1034 (0x40A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-550">Испанский — традиционная сортировка</span><span class="sxs-lookup"><span data-stu-id="71fdc-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-551">1035 (0x40B)</span><span class="sxs-lookup"><span data-stu-id="71fdc-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-552">Финский</span><span class="sxs-lookup"><span data-stu-id="71fdc-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-553">1036 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-554">Французский (Франция)</span><span class="sxs-lookup"><span data-stu-id="71fdc-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-555">1037 (0x40D)</span><span class="sxs-lookup"><span data-stu-id="71fdc-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-556">Иврит</span><span class="sxs-lookup"><span data-stu-id="71fdc-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-557">1038 (0x40E)</span><span class="sxs-lookup"><span data-stu-id="71fdc-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-558">Венгерский</span><span class="sxs-lookup"><span data-stu-id="71fdc-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-559">1039 (0x40F)</span><span class="sxs-lookup"><span data-stu-id="71fdc-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-560">Исландский</span><span class="sxs-lookup"><span data-stu-id="71fdc-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="71fdc-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-562">Итальянский (Италия)</span><span class="sxs-lookup"><span data-stu-id="71fdc-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="71fdc-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-564">Японский</span><span class="sxs-lookup"><span data-stu-id="71fdc-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="71fdc-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-566">Корейский</span><span class="sxs-lookup"><span data-stu-id="71fdc-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="71fdc-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-568">Голландский (Нидерланды)</span><span class="sxs-lookup"><span data-stu-id="71fdc-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="71fdc-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-570">Норвежский — букмол</span><span class="sxs-lookup"><span data-stu-id="71fdc-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="71fdc-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-572">Польский</span><span class="sxs-lookup"><span data-stu-id="71fdc-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="71fdc-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-574">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="71fdc-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="71fdc-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="71fdc-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="71fdc-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-578">Румынский</span><span class="sxs-lookup"><span data-stu-id="71fdc-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="71fdc-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-580">русском языке</span><span class="sxs-lookup"><span data-stu-id="71fdc-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-582">Хорватский</span><span class="sxs-lookup"><span data-stu-id="71fdc-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-583">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="71fdc-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-584">Словацкий</span><span class="sxs-lookup"><span data-stu-id="71fdc-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-585">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-586">Албанский</span><span class="sxs-lookup"><span data-stu-id="71fdc-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-587">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="71fdc-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-588">Шведский</span><span class="sxs-lookup"><span data-stu-id="71fdc-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-589">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="71fdc-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-590">Тайский</span><span class="sxs-lookup"><span data-stu-id="71fdc-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-591">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="71fdc-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-592">Турецкий</span><span class="sxs-lookup"><span data-stu-id="71fdc-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="71fdc-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-594">Урду</span><span class="sxs-lookup"><span data-stu-id="71fdc-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="71fdc-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-596">Индонезийский</span><span class="sxs-lookup"><span data-stu-id="71fdc-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="71fdc-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-598">Украинский</span><span class="sxs-lookup"><span data-stu-id="71fdc-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="71fdc-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-600">Белорусский</span><span class="sxs-lookup"><span data-stu-id="71fdc-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="71fdc-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-602">Словенский</span><span class="sxs-lookup"><span data-stu-id="71fdc-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="71fdc-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-604">Эстонский</span><span class="sxs-lookup"><span data-stu-id="71fdc-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-605">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="71fdc-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-606">Латышский</span><span class="sxs-lookup"><span data-stu-id="71fdc-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="71fdc-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-608">Литовский</span><span class="sxs-lookup"><span data-stu-id="71fdc-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="71fdc-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-610">Персидский</span><span class="sxs-lookup"><span data-stu-id="71fdc-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-611">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-612">Вьетнамский</span><span class="sxs-lookup"><span data-stu-id="71fdc-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-613">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="71fdc-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-614">Баскский</span><span class="sxs-lookup"><span data-stu-id="71fdc-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-615">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="71fdc-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-616">Сербский</span><span class="sxs-lookup"><span data-stu-id="71fdc-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-617">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="71fdc-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-618">Македонский (Северная Македония)</span><span class="sxs-lookup"><span data-stu-id="71fdc-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="71fdc-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-620">суту</span><span class="sxs-lookup"><span data-stu-id="71fdc-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="71fdc-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-622">Тсонга</span><span class="sxs-lookup"><span data-stu-id="71fdc-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="71fdc-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-624">тсвана</span><span class="sxs-lookup"><span data-stu-id="71fdc-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="71fdc-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-626">Коса</span><span class="sxs-lookup"><span data-stu-id="71fdc-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="71fdc-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-628">Зулу</span><span class="sxs-lookup"><span data-stu-id="71fdc-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="71fdc-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-630">Африкаанс</span><span class="sxs-lookup"><span data-stu-id="71fdc-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-631">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="71fdc-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-632">Фарерского</span><span class="sxs-lookup"><span data-stu-id="71fdc-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="71fdc-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="71fdc-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-635">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-636">Мальтийский</span><span class="sxs-lookup"><span data-stu-id="71fdc-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-637">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-638">Шотландский гэльский (Великобритания)</span><span class="sxs-lookup"><span data-stu-id="71fdc-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-639">1085 (0x43D)</span><span class="sxs-lookup"><span data-stu-id="71fdc-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-640">Идиш</span><span class="sxs-lookup"><span data-stu-id="71fdc-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-641">1086 (со значением 0x43e)</span><span class="sxs-lookup"><span data-stu-id="71fdc-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-642">Малайский — Малайзия</span><span class="sxs-lookup"><span data-stu-id="71fdc-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="71fdc-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-644">Арабский — Ирак</span><span class="sxs-lookup"><span data-stu-id="71fdc-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="71fdc-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-646">Китайский (упрощенное письмо) — КНР</span><span class="sxs-lookup"><span data-stu-id="71fdc-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="71fdc-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-648">Немецкий — Швейцария</span><span class="sxs-lookup"><span data-stu-id="71fdc-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="71fdc-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-650">Английский — Великобритания</span><span class="sxs-lookup"><span data-stu-id="71fdc-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-651">2058 (0x80)</span><span class="sxs-lookup"><span data-stu-id="71fdc-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-652">Испанский — Мексика</span><span class="sxs-lookup"><span data-stu-id="71fdc-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-653">2060 (0x80C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-654">Французский — Бельгия</span><span class="sxs-lookup"><span data-stu-id="71fdc-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="71fdc-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-656">Итальянский — Швейцария</span><span class="sxs-lookup"><span data-stu-id="71fdc-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="71fdc-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-658">Голландский — Бельгия</span><span class="sxs-lookup"><span data-stu-id="71fdc-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="71fdc-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-660">Норвежский — нюнорск</span><span class="sxs-lookup"><span data-stu-id="71fdc-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="71fdc-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-662">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="71fdc-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="71fdc-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-664">Румынский — Молдова</span><span class="sxs-lookup"><span data-stu-id="71fdc-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="71fdc-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-666">Русский — Молдова</span><span class="sxs-lookup"><span data-stu-id="71fdc-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-667">2074 (0x81A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-668">Сербский — латиница</span><span class="sxs-lookup"><span data-stu-id="71fdc-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-669">2077 (0x81D)</span><span class="sxs-lookup"><span data-stu-id="71fdc-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-670">Шведский — Финляндия</span><span class="sxs-lookup"><span data-stu-id="71fdc-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-671">3073 (0xC01)</span><span class="sxs-lookup"><span data-stu-id="71fdc-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-672">Арабский — Египет</span><span class="sxs-lookup"><span data-stu-id="71fdc-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-673">3076 (0xC04)</span><span class="sxs-lookup"><span data-stu-id="71fdc-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-674">Китайский (традиционное письмо) — Гонконг Гонконг</span><span class="sxs-lookup"><span data-stu-id="71fdc-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-675">3079 (0xC07)</span><span class="sxs-lookup"><span data-stu-id="71fdc-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-676">Немецкий — Австрия</span><span class="sxs-lookup"><span data-stu-id="71fdc-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-677">3081 (0xC09)</span><span class="sxs-lookup"><span data-stu-id="71fdc-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-678">Английский — Австралия</span><span class="sxs-lookup"><span data-stu-id="71fdc-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-679">3082 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-680">Испанский — Международная сортировка</span><span class="sxs-lookup"><span data-stu-id="71fdc-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-681">3084 (0xC0C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-682">Французский — Канада</span><span class="sxs-lookup"><span data-stu-id="71fdc-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-683">3098 (0xC1A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-684">Сербский — кириллица</span><span class="sxs-lookup"><span data-stu-id="71fdc-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="71fdc-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-686">Арабский — Ливия</span><span class="sxs-lookup"><span data-stu-id="71fdc-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="71fdc-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-688">Китайский (упрощенное письмо) — Сингапур</span><span class="sxs-lookup"><span data-stu-id="71fdc-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="71fdc-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-690">Немецкий — Люксембург</span><span class="sxs-lookup"><span data-stu-id="71fdc-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="71fdc-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-692">Английский — Канада</span><span class="sxs-lookup"><span data-stu-id="71fdc-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-693">4106 (0x100A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-694">Испанский — Гватемала</span><span class="sxs-lookup"><span data-stu-id="71fdc-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-695">4108 (0x100C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-696">Французский — Швейцария</span><span class="sxs-lookup"><span data-stu-id="71fdc-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="71fdc-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-698">Арабский — Алжир</span><span class="sxs-lookup"><span data-stu-id="71fdc-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="71fdc-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-700">Немецкий — Лихтенштейн</span><span class="sxs-lookup"><span data-stu-id="71fdc-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="71fdc-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-702">Английский — Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="71fdc-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-703">5130 (0x140A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-704">Испанский — Коста-Рика</span><span class="sxs-lookup"><span data-stu-id="71fdc-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-705">5132 (0x140C)</span><span class="sxs-lookup"><span data-stu-id="71fdc-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-706">Французский — Люксембург</span><span class="sxs-lookup"><span data-stu-id="71fdc-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="71fdc-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-708">Арабский — Марокко</span><span class="sxs-lookup"><span data-stu-id="71fdc-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="71fdc-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-710">Английский — Ирландия</span><span class="sxs-lookup"><span data-stu-id="71fdc-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-711">6154 (0x180A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-712">Испанский — Панама</span><span class="sxs-lookup"><span data-stu-id="71fdc-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-713">7169 (0x1C01)</span><span class="sxs-lookup"><span data-stu-id="71fdc-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-714">Арабский — Тунис</span><span class="sxs-lookup"><span data-stu-id="71fdc-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-715">7177 (0x1C09)</span><span class="sxs-lookup"><span data-stu-id="71fdc-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-716">Английский — Южная Африка</span><span class="sxs-lookup"><span data-stu-id="71fdc-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-717">7178 (0x1C0A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-718">Испанский — Доминиканская Республика</span><span class="sxs-lookup"><span data-stu-id="71fdc-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="71fdc-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-720">Арабский — Оман</span><span class="sxs-lookup"><span data-stu-id="71fdc-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="71fdc-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-722">Английский — Ямайка</span><span class="sxs-lookup"><span data-stu-id="71fdc-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-723">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-724">Испанский — Венесуэла</span><span class="sxs-lookup"><span data-stu-id="71fdc-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="71fdc-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-726">Арабский — Йемен</span><span class="sxs-lookup"><span data-stu-id="71fdc-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-727">9226 (0x240A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-728">Испанский — Колумбия</span><span class="sxs-lookup"><span data-stu-id="71fdc-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="71fdc-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-730">Арабский — Сирия</span><span class="sxs-lookup"><span data-stu-id="71fdc-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="71fdc-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-732">Английский — Белиз</span><span class="sxs-lookup"><span data-stu-id="71fdc-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-733">10250 (0x280A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-734">Испанский — Перу</span><span class="sxs-lookup"><span data-stu-id="71fdc-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-735">11265 (0x2C01)</span><span class="sxs-lookup"><span data-stu-id="71fdc-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-736">Арабский — Иордания</span><span class="sxs-lookup"><span data-stu-id="71fdc-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-737">11273 (0x2C09)</span><span class="sxs-lookup"><span data-stu-id="71fdc-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-738">Английский — Тринидад</span><span class="sxs-lookup"><span data-stu-id="71fdc-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-739">11274 (0x2C0A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-740">Испанский — Аргентина</span><span class="sxs-lookup"><span data-stu-id="71fdc-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="71fdc-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-742">Арабский — Ливан</span><span class="sxs-lookup"><span data-stu-id="71fdc-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-743">12298 (0x300A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-744">Испанский — Эквадор</span><span class="sxs-lookup"><span data-stu-id="71fdc-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="71fdc-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-746">Арабский — Кувейт</span><span class="sxs-lookup"><span data-stu-id="71fdc-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-747">13322 (0x340A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-748">Испанский — Чили</span><span class="sxs-lookup"><span data-stu-id="71fdc-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="71fdc-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-750">Арабский — ОАЭ</span><span class="sxs-lookup"><span data-stu-id="71fdc-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-751">14346 (0x380A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-752">Испанский — Уругвай</span><span class="sxs-lookup"><span data-stu-id="71fdc-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-753">15361 (0x3C01)</span><span class="sxs-lookup"><span data-stu-id="71fdc-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-754">Арабский — Бахрейн</span><span class="sxs-lookup"><span data-stu-id="71fdc-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-755">15370 (0x3C0A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-756">Испанский — Парагвай</span><span class="sxs-lookup"><span data-stu-id="71fdc-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="71fdc-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-758">Арабский — Катар</span><span class="sxs-lookup"><span data-stu-id="71fdc-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-759">16394 (0x400A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-760">Испанский — Боливия</span><span class="sxs-lookup"><span data-stu-id="71fdc-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-761">17418 (0x440A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-762">Испанский — Эль-Сальвадор</span><span class="sxs-lookup"><span data-stu-id="71fdc-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-763">18442 (0x480A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-764">Испанский — Гондурас</span><span class="sxs-lookup"><span data-stu-id="71fdc-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-765">19466 (0x4C0A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-766">Испанский — Никарагуа</span><span class="sxs-lookup"><span data-stu-id="71fdc-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-767">20490 (0x500A)</span><span class="sxs-lookup"><span data-stu-id="71fdc-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-768">Испанский — Пуэрто-Рико</span><span class="sxs-lookup"><span data-stu-id="71fdc-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="71fdc-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-770">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-771">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-772">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Продуктоптионс \| продуктсуите"), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("Малый бизнес", "предприятие", "BackOffice", "коммуникационный сервер", "сервер терминалов", "Малый бизнес (ограниченный)", "Embedded NT", "центр обработки данных")</span><span class="sxs-lookup"><span data-stu-id="71fdc-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-773">Установленные и лицензированные дополнения системных продуктов в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="71fdc-774">Например, значение 146 (0x92) для **оспродуктсуите** указывает Enterprise, службы терминалов и центр обработки данных (биты 1, 4 и семь наборов).</span><span class="sxs-lookup"><span data-stu-id="71fdc-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="71fdc-775">В следующем списке перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="71fdc-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="71fdc-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-777">Microsoft Small Business Server был установлен, но может быть обновлен до другой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-778">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-779">Установлена ОС Windows Server 2008 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="71fdc-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="71fdc-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-781">Устанавливаются компоненты Windows BackOffice.</span><span class="sxs-lookup"><span data-stu-id="71fdc-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="71fdc-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-783">Коммуникационный сервер установлен.</span><span class="sxs-lookup"><span data-stu-id="71fdc-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="71fdc-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-785">Службы терминалов установлены.</span><span class="sxs-lookup"><span data-stu-id="71fdc-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="71fdc-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-787">Microsoft Small Business Server устанавливается с помощью клиентской лицензии с лицензией.</span><span class="sxs-lookup"><span data-stu-id="71fdc-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="71fdc-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-789">Установлена система Windows Embedded.</span><span class="sxs-lookup"><span data-stu-id="71fdc-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="71fdc-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-791">Установлен выпуск Datacenter.</span><span class="sxs-lookup"><span data-stu-id="71fdc-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="71fdc-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-793">Службы терминалов установлены, но поддерживается только один интерактивный сеанс.</span><span class="sxs-lookup"><span data-stu-id="71fdc-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="71fdc-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-795">Установлен Windows Home Edition.</span><span class="sxs-lookup"><span data-stu-id="71fdc-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="71fdc-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-797">Установлен выпуск Web Server.</span><span class="sxs-lookup"><span data-stu-id="71fdc-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="71fdc-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-799">Установлен выпуск Storage Server.</span><span class="sxs-lookup"><span data-stu-id="71fdc-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="71fdc-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-801">Установлен выпуск Compute Cluster Edition.</span><span class="sxs-lookup"><span data-stu-id="71fdc-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="71fdc-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-803">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71fdc-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-804">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-805">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**система \_ CIM**](cim-operatingsystem.md)".**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="71fdc-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-806">Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-806">Type of operating system.</span></span> <span data-ttu-id="71fdc-807">В следующем списке указаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="71fdc-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="71fdc-808">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71fdc-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71fdc-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="71fdc-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-812">МАКРОКОМАНД</span><span class="sxs-lookup"><span data-stu-id="71fdc-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="71fdc-813"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="71fdc-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="71fdc-814"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="71fdc-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="71fdc-815"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="71fdc-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="71fdc-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="71fdc-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="71fdc-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="71fdc-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="71fdc-818"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="71fdc-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="71fdc-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="71fdc-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="71fdc-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="71fdc-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="71fdc-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="71fdc-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="71fdc-822"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="71fdc-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="71fdc-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="71fdc-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="71fdc-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="71fdc-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="71fdc-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="71fdc-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="71fdc-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="71fdc-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="71fdc-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="71fdc-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="71fdc-828"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="71fdc-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="71fdc-829"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="71fdc-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="71fdc-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="71fdc-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="71fdc-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="71fdc-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="71fdc-832"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="71fdc-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="71fdc-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="71fdc-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="71fdc-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="71fdc-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="71fdc-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="71fdc-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="71fdc-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="71fdc-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="71fdc-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="71fdc-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="71fdc-838"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="71fdc-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="71fdc-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="71fdc-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="71fdc-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="71fdc-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="71fdc-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="71fdc-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="71fdc-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="71fdc-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="71fdc-843"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="71fdc-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="71fdc-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="71fdc-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="71fdc-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="71fdc-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="71fdc-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="71fdc-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="71fdc-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="71fdc-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="71fdc-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="71fdc-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="71fdc-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="71fdc-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="71fdc-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="71fdc-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="71fdc-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="71fdc-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="71fdc-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="71fdc-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="71fdc-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="71fdc-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="71fdc-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="71fdc-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="71fdc-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="71fdc-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="71fdc-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="71fdc-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="71fdc-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="71fdc-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="71fdc-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="71fdc-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="71fdc-859"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="71fdc-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="71fdc-860"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="71fdc-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="71fdc-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="71fdc-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="71fdc-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="71fdc-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="71fdc-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="71fdc-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="71fdc-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="71fdc-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="71fdc-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="71fdc-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="71fdc-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="71fdc-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="71fdc-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="71fdc-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="71fdc-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="71fdc-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="71fdc-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="71fdc-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="71fdc-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="71fdc-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="71fdc-871"><span id="OS_390"></span><span id="os_390"></span>**ОС/390** (60)</span><span class="sxs-lookup"><span data-stu-id="71fdc-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="71fdc-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="71fdc-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="71fdc-873"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (62)</span><span class="sxs-lookup"><span data-stu-id="71fdc-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-874">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="71fdc-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-875">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-876">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-877">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**модель \_ CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="71fdc-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-878">Дополнительное описание текущей версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="71fdc-879">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-880">**паинаблед**</span><span class="sxs-lookup"><span data-stu-id="71fdc-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-881">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-882">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-883">При **значении true** расширения физических адресов (PAE) включаются операционной системой, работающей на процессорах Intel.</span><span class="sxs-lookup"><span data-stu-id="71fdc-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="71fdc-884">PAE позволяет приложениям обращаться к более чем 4 ГБ физической памяти.</span><span class="sxs-lookup"><span data-stu-id="71fdc-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="71fdc-885">При включении PAE операционная система использует линейное преобразование адресов трех уровней, а не два уровня.</span><span class="sxs-lookup"><span data-stu-id="71fdc-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="71fdc-886">Предоставление приложению большего объема физической памяти снижает необходимость перекачки памяти в файл подкачки и повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="71fdc-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="71fdc-887">Чтобы включить, PAE, используйте параметр "/PAE" в файле Boot.ini.</span><span class="sxs-lookup"><span data-stu-id="71fdc-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="71fdc-888">Дополнительные сведения о расширении физических адресов см. в разделе <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="71fdc-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-889">**плуспродуктид**</span><span class="sxs-lookup"><span data-stu-id="71fdc-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-890">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-891">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-892">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="71fdc-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="71fdc-893">ProductId ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-894">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71fdc-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-895">**плусверсионнумбер**</span><span class="sxs-lookup"><span data-stu-id="71fdc-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-896">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-897">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-898">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="71fdc-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="71fdc-899">VersionNumber ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-900">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71fdc-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-901">**портаблеоператингсистем**</span><span class="sxs-lookup"><span data-stu-id="71fdc-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-902">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-903">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-904">Указывает, загружена ли операционная система с внешнего USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="71fdc-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="71fdc-905">Если значение равно true, операционная система обнаружила, что она загружается на поддерживаемом локально подключенном запоминающем устройстве.</span><span class="sxs-lookup"><span data-stu-id="71fdc-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="71fdc-906">**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="71fdc-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-907">**Источник**</span><span class="sxs-lookup"><span data-stu-id="71fdc-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-908">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71fdc-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-909">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-910">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="71fdc-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-911">Указывает, является ли это основной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="71fdc-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-912">**продукттипе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-913">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-914">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-915">Дополнительные сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="71fdc-916">**Рабочая станция** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="71fdc-917">**Контроллер домена** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="71fdc-918">**Сервер** (3)</span><span class="sxs-lookup"><span data-stu-id="71fdc-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-919">**куантумленгс**</span><span class="sxs-lookup"><span data-stu-id="71fdc-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-920">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71fdc-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-921">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="71fdc-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-922">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ приоритиконтрол \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="71fdc-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-923">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="71fdc-923">Not supported</span></span>

<span data-ttu-id="71fdc-924">\* \* Windows Server 2008 и Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="71fdc-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="71fdc-925">Свойство **куантумленгс** определяет число тактов часов в такте.</span><span class="sxs-lookup"><span data-stu-id="71fdc-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="71fdc-926">Такт — это единица времени выполнения, которую планировщик может предоставить приложению, прежде чем переходить к другим приложениям.</span><span class="sxs-lookup"><span data-stu-id="71fdc-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="71fdc-927">Когда поток запускается в течение одного такта, ядро загружает его и перемещает в конец очереди для приложений с равными приоритетами.</span><span class="sxs-lookup"><span data-stu-id="71fdc-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="71fdc-928">Фактическая длина такта потока различается на разных платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="71fdc-929">Только для Windows NT и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="71fdc-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="71fdc-930">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="71fdc-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71fdc-931">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="71fdc-932">**Один такт** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="71fdc-933">**Два кванта** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-934">**куантумтипе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-935">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71fdc-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-936">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="71fdc-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-937">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="71fdc-937">Not supported</span></span>

<span data-ttu-id="71fdc-938">\* \* Windows Server 2008 и Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="71fdc-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="71fdc-939">Свойство **куантумтипе** указывает либо фиксированные, либо такты переменной длины.</span><span class="sxs-lookup"><span data-stu-id="71fdc-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="71fdc-940">Windows по умолчанию использует такты переменной длины, где приложение переднего плана имеет более длительный такт, чем фоновые приложения.</span><span class="sxs-lookup"><span data-stu-id="71fdc-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="71fdc-941">Windows Server по умолчанию принимает такты фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="71fdc-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="71fdc-942">Такт — это единица времени выполнения, которую планировщик может предоставить приложению перед переключением на другое приложение.</span><span class="sxs-lookup"><span data-stu-id="71fdc-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="71fdc-943">Когда поток запускается в течение одного такта, ядро загружает его и перемещает в конец очереди для приложений с равными приоритетами.</span><span class="sxs-lookup"><span data-stu-id="71fdc-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="71fdc-944">Фактическая длина такта потока различается на разных платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="71fdc-945">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="71fdc-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71fdc-946">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71fdc-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="71fdc-947">**Исправлено** (1)</span><span class="sxs-lookup"><span data-stu-id="71fdc-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="71fdc-948">**Переменная** (2)</span><span class="sxs-lookup"><span data-stu-id="71fdc-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-949">**регистередусер**</span><span class="sxs-lookup"><span data-stu-id="71fdc-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-950">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-951">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-952">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| регистередовнер")</span><span class="sxs-lookup"><span data-stu-id="71fdc-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-953">Имя зарегистрированного пользователя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="71fdc-954">Пример: "Бен Смит"</span><span class="sxs-lookup"><span data-stu-id="71fdc-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-955">**Номер**</span><span class="sxs-lookup"><span data-stu-id="71fdc-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-956">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-957">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-958">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="71fdc-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-959">Серийный идентификационный номер продукта операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="71fdc-960">Пример: "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="71fdc-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-961">**сервицепаккмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="71fdc-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-962">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71fdc-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-963">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-964">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **всервицепаккмажор**")</span><span class="sxs-lookup"><span data-stu-id="71fdc-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-965">Основной номер версии пакета обновления, установленного в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="71fdc-966">Если пакет обновления не установлен, значение равно 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="71fdc-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-967">**сервицепаккминорверсион**</span><span class="sxs-lookup"><span data-stu-id="71fdc-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-968">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71fdc-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-969">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-970">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **всервицепаккминор**")</span><span class="sxs-lookup"><span data-stu-id="71fdc-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-971">Дополнительный номер версии пакета обновления, установленного в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="71fdc-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="71fdc-972">Если пакет обновления не установлен, значение равно 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="71fdc-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-973">**сизесторединпагингфилес**</span><span class="sxs-lookup"><span data-stu-id="71fdc-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-974">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-975">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-976">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Параметры системной памяти DMTF \| 001,3 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="71fdc-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-977">Общее число килобайтов, которые могут храниться в файлах подкачки операционной системы — 0 (ноль) указывает на отсутствие файлов подкачки.</span><span class="sxs-lookup"><span data-stu-id="71fdc-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="71fdc-978">Имейте в виду, что это число не представляет фактический физический размер файла подкачки на диске.</span><span class="sxs-lookup"><span data-stu-id="71fdc-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="71fdc-979">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-980">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-981">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="71fdc-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-982">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-983">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-984">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="71fdc-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-985">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="71fdc-985">Current status of the object.</span></span> <span data-ttu-id="71fdc-986">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="71fdc-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="71fdc-987">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например, жесткий диск с поддержкой SMART может работать правильно, но прогнозирует сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="71fdc-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="71fdc-988">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="71fdc-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71fdc-989">Состояние службы применяется к административной работе, например к зеркальному переносу диска, перезагрузке списка разрешений пользователя или другой административной работе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71fdc-990">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="71fdc-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71fdc-991">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71fdc-992">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="71fdc-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71fdc-993">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="71fdc-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71fdc-994">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="71fdc-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71fdc-995">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="71fdc-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71fdc-996">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="71fdc-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71fdc-997">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="71fdc-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71fdc-998">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="71fdc-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71fdc-999">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="71fdc-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71fdc-1000">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71fdc-1001">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71fdc-1002">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71fdc-1003">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-1004">**суитемаск**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1005">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1006">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1007">Квалификаторы: [**битовые карты**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**Битвалуес**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, BackOffice Edition", "Windows Server, Communications Edition", "службы терминалов Microsoft", "Windows Server, малый бизнес-выпуск ограничен", "Windows Embedded", "Windows Server, Datacenter Edition", "один пользователь", "Windows Home Edition", "Windows Server, Web Edition")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1008">Битовые флаги, которые обозначают наборы продуктов, доступные в системе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="71fdc-1009">Например, чтобы указать как личное, так и BackOffice, задайте для **суитемаск** значение `4 | 512` или `516` .</span><span class="sxs-lookup"><span data-stu-id="71fdc-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="71fdc-1010">1</span><span class="sxs-lookup"><span data-stu-id="71fdc-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1011">Малый бизнес</span><span class="sxs-lookup"><span data-stu-id="71fdc-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1012">2</span><span class="sxs-lookup"><span data-stu-id="71fdc-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="71fdc-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1014">4</span><span class="sxs-lookup"><span data-stu-id="71fdc-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="71fdc-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1016">8</span><span class="sxs-lookup"><span data-stu-id="71fdc-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1017">Коммуникации</span><span class="sxs-lookup"><span data-stu-id="71fdc-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1018">16</span><span class="sxs-lookup"><span data-stu-id="71fdc-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1019">Службы терминалов</span><span class="sxs-lookup"><span data-stu-id="71fdc-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1020">32</span><span class="sxs-lookup"><span data-stu-id="71fdc-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1021">Ограничено малым предприятием</span><span class="sxs-lookup"><span data-stu-id="71fdc-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1022">64</span><span class="sxs-lookup"><span data-stu-id="71fdc-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1023">Выпуск Embedded</span><span class="sxs-lookup"><span data-stu-id="71fdc-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1024">128</span><span class="sxs-lookup"><span data-stu-id="71fdc-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1026">256</span><span class="sxs-lookup"><span data-stu-id="71fdc-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1027">Один пользователь</span><span class="sxs-lookup"><span data-stu-id="71fdc-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1028">512</span><span class="sxs-lookup"><span data-stu-id="71fdc-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1029">Выпуск Home Edition</span><span class="sxs-lookup"><span data-stu-id="71fdc-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1030">1024</span><span class="sxs-lookup"><span data-stu-id="71fdc-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="71fdc-1031">Выпуск Web Server</span><span class="sxs-lookup"><span data-stu-id="71fdc-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71fdc-1032">**системдевице**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1033">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1034">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1035">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции реестра Win32API \| [**жетприватепрофилестринг**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| paths \| целевое устройство")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1036">Раздел физического диска, на котором установлена операционная система.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1037">**системдиректори**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1038">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1039">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1040">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| системные информационные функции [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="71fdc-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1041">Системный каталог операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1041">System directory of the operating system.</span></span>

<span data-ttu-id="71fdc-1042">Пример: "C: \\ Windows \\ System32"</span><span class="sxs-lookup"><span data-stu-id="71fdc-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1044">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1045">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1046">Буква диска, на котором находится операционная система.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="71fdc-1047">Пример: "C:"</span><span class="sxs-lookup"><span data-stu-id="71fdc-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1048">**тоталсвапспацесизе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1049">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1050">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1051">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1052">Общий объем области подкачки в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="71fdc-1053">Это значение может быть **равно NULL** (не указано), если область подкачки не отличается от файлов страниц.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="71fdc-1054">Однако некоторые операционные системы отличают эти понятия.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="71fdc-1055">Например, в UNIX все процессы могут быть переключены, если список свободных страниц опускается и остается ниже заданного значения.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="71fdc-1056">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-1057">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1058">**тоталвиртуалмеморисизе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1059">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1060">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1061">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1062">Число (в килобайтах) виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="71fdc-1063">Например, это можно рассчитать, добавив общий объем ОЗУ к объему пространства для разбиения на страницы, то есть добавив объем памяти, выданный компьютером или агрегированный системой, в свойство **сизесторединпагингфилес**.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="71fdc-1064">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-1065">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1066">**тоталвисиблемеморисизе**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1067">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1068">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1069">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1070">Общий объем физической памяти, доступной операционной системе, в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="71fdc-1071">Это значение не обязательно указывает на истинный объем физической памяти, но сообщает операционной системе, как она доступна.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="71fdc-1072">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="71fdc-1073">Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1074">**Version**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1075">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1076">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1077">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("версия"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API Structured Information Structures \| \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| двмажорверсион, двминорверсион")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1078">Номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1078">Version number of the operating system.</span></span>

<span data-ttu-id="71fdc-1079">Пример: "4,0"</span><span class="sxs-lookup"><span data-stu-id="71fdc-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="71fdc-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fdc-1081">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1082">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71fdc-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fdc-1083">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| системные информационные функции \| [**жетвиндовсдиректори**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span><span class="sxs-lookup"><span data-stu-id="71fdc-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="71fdc-1084">Каталог операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="71fdc-1085">Пример: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="71fdc-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71fdc-1086">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71fdc-1086">Remarks</span></span>

<span data-ttu-id="71fdc-1087">Класс **Win32 \_ операционной** системы является производным [**от \_ модели CIM**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="71fdc-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="71fdc-1088">Любая операционная система, которая может быть установлена на компьютере под управлением операционной системы Windows, является потомком или членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="71fdc-1089">**Win32 \_ Операционная** система — это одноэлементный класс.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="71fdc-1090">Чтобы получить единственный экземпляр, используйте "@" для ключа.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="71fdc-1091">В отличие от большинства других классов WMI, создаваемых MgmtClassGen, метод **. CreateInstance**() возвратит пустой объект **операционной** системы.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="71fdc-1092">Поэтому, если вы используете C \# с MgmtClassGen, можно использовать следующий код:</span><span class="sxs-lookup"><span data-stu-id="71fdc-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="71fdc-1093">Примеры</span><span class="sxs-lookup"><span data-stu-id="71fdc-1093">Examples</span></span>

<span data-ttu-id="71fdc-1094">Пример на языке VBScript, который получает данные о операционной системе и процессоре из [**Win32 \_ ComputerSystem**](win32-computersystem.md), [**\_ процессора Win32**](win32-processor.md)и Win32 Operating, можно найти в примерах, посвященных [**\_ процессору Win32**](win32-processor.md) . **\_**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="71fdc-1095">В разделе [Создание отчетов о среде Exchange с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell в коллекции TechNet используется класс **\_ операционной системы Win32** для создания отчетов среды Exchange.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="71fdc-1096">Пример " [Получение времени работы сервера с помощью WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) " в коллекции TechNet использует свойство **LastBootupTime** , чтобы определить, как долго работает сервер.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="71fdc-1097">В этом примере также используется параметр timeout, чтобы предотвратить зависание вызова WMI.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="71fdc-1098">Пример кода VBScript для надстройки [WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс операционной системы **Win32 \_** для получения сведений о ОС с нескольких удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="71fdc-1099">Следующий скрипт получает экземпляры **Win32 \_ операционной** системы в пространстве имен root CIMv2 по умолчанию \\ , а затем отображает сведения об операционной системе.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="71fdc-1100">В следующем образце кода PowerShell отображаются все рабочие сведения о текущей ОС.</span><span class="sxs-lookup"><span data-stu-id="71fdc-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="71fdc-1101">Требования</span><span class="sxs-lookup"><span data-stu-id="71fdc-1101">Requirements</span></span>



| <span data-ttu-id="71fdc-1102">Требование</span><span class="sxs-lookup"><span data-stu-id="71fdc-1102">Requirement</span></span> | <span data-ttu-id="71fdc-1103">Значение</span><span class="sxs-lookup"><span data-stu-id="71fdc-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71fdc-1104">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71fdc-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="71fdc-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71fdc-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71fdc-1106">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71fdc-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="71fdc-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71fdc-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71fdc-1108">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71fdc-1108">Namespace</span></span><br/>                | <span data-ttu-id="71fdc-1109">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="71fdc-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71fdc-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="71fdc-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71fdc-1111"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71fdc-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71fdc-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="71fdc-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71fdc-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71fdc-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71fdc-1114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71fdc-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fdc-1115">**Операционная система CIM \_**</span><span class="sxs-lookup"><span data-stu-id="71fdc-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="71fdc-1116">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="71fdc-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="71fdc-1117">Задачи WMI: операционные системы</span><span class="sxs-lookup"><span data-stu-id="71fdc-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="71fdc-1118">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="71fdc-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="71fdc-1119">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="71fdc-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
