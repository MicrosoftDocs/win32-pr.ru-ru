---
description: '\_Класс системы CIM представляет собой операционную систему компьютера, которая состоит из программного обеспечения и микропрограммы, которые позволяют использовать оборудование компьютера.'
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: Класс CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538960"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="288a9-103">\_Класс операционной системы CIM</span><span class="sxs-lookup"><span data-stu-id="288a9-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="288a9-104">Класс **системы \_ CIM** представляет собой операционную систему компьютера, которая состоит из программного обеспечения и микропрограммы, которые позволяют использовать оборудование компьютера.</span><span class="sxs-lookup"><span data-stu-id="288a9-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="288a9-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="288a9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="288a9-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="288a9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="288a9-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="288a9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="288a9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="288a9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="288a9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="288a9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="288a9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="288a9-110">Members</span></span>

<span data-ttu-id="288a9-111">Класс **\_ операционной системы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="288a9-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="288a9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="288a9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="288a9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="288a9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="288a9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="288a9-114">Methods</span></span>

<span data-ttu-id="288a9-115">Класс **\_ операционной системы CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="288a9-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="288a9-116">Метод</span><span class="sxs-lookup"><span data-stu-id="288a9-116">Method</span></span>                                                           | <span data-ttu-id="288a9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="288a9-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="288a9-118">**Перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="288a9-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="288a9-119">Метод класса, который завершает работу системы компьютера и перезапускает его.</span><span class="sxs-lookup"><span data-stu-id="288a9-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="288a9-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="288a9-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="288a9-121">**Закрытия**</span><span class="sxs-lookup"><span data-stu-id="288a9-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="288a9-122">Метод класса, который выгружает программы и библиотеки DLL до точки, в которой можно отключить компьютер.</span><span class="sxs-lookup"><span data-stu-id="288a9-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="288a9-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="288a9-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="288a9-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="288a9-124">Properties</span></span>

<span data-ttu-id="288a9-125">Класс **\_ операционной системы CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="288a9-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="288a9-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="288a9-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="288a9-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-130">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="288a9-130">Short textual description of the object.</span></span>

<span data-ttu-id="288a9-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="288a9-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-135">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="288a9-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="288a9-136">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="288a9-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="288a9-137">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="288a9-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-138">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="288a9-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-141">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="288a9-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="288a9-142">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="288a9-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="288a9-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-146">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="288a9-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="288a9-147">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="288a9-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-148">**курренттимезоне**</span><span class="sxs-lookup"><span data-stu-id="288a9-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-149">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="288a9-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-151">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="288a9-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-152">Количество минут, в течение которых операционная система смещается с среднего времени по Гринвичу (GMT).</span><span class="sxs-lookup"><span data-stu-id="288a9-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="288a9-153">Число может быть положительным, отрицательным или нулевым.</span><span class="sxs-lookup"><span data-stu-id="288a9-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="288a9-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-157">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="288a9-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-158">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="288a9-158">Textual description of the object.</span></span>

<span data-ttu-id="288a9-159">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-160">**Распределяемый**</span><span class="sxs-lookup"><span data-stu-id="288a9-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-161">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="288a9-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="288a9-163">Если **значение равно true**, операционная система распространяется на несколько узлов системы компьютера, которые должны быть сгруппированы в кластер.</span><span class="sxs-lookup"><span data-stu-id="288a9-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-164">**фрифисикалмемори**</span><span class="sxs-lookup"><span data-stu-id="288a9-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-165">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-167">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-168">Количество килобайтов физической памяти, неиспользуемое и доступное в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="288a9-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="288a9-169">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-170">**фриспацеинпагингфилес**</span><span class="sxs-lookup"><span data-stu-id="288a9-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-171">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-173">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Параметры системной памяти DMTF \| 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="288a9-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-174">Число килобайтов, которые могут быть сопоставлены с файлами подкачки операционной системы, не вызывая переход на другие страницы. Значение 0 указывает, что файлы подкачки отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="288a9-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="288a9-175">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-176">**фривиртуалмемори**</span><span class="sxs-lookup"><span data-stu-id="288a9-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-177">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-179">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-180">Количество килобайтов виртуальной памяти, неиспользуемое и доступное в данный момент.</span><span class="sxs-lookup"><span data-stu-id="288a9-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="288a9-181">Например, это можно рассчитать, добавив объем свободной оперативной памяти к объему свободного места на пейджер (то есть добавив свойства **фрифисикалмемори** и **фриспацеинпагингфилес** ).</span><span class="sxs-lookup"><span data-stu-id="288a9-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="288a9-182">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="288a9-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-184">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="288a9-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-186">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="288a9-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-187">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="288a9-187">Date and time the object was installed.</span></span> <span data-ttu-id="288a9-188">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="288a9-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="288a9-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="288a9-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-191">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="288a9-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="288a9-193">Время последней загрузки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="288a9-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="288a9-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-195">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="288a9-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-197">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. В файле IETF \| Host-Resources-MIB. хрсистемдате "," MIF. \|Общие сведения о DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="288a9-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-198">Понятие локальной даты и времени суток операционной системы.</span><span class="sxs-lookup"><span data-stu-id="288a9-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-199">**макснумберофпроцессес**</span><span class="sxs-lookup"><span data-stu-id="288a9-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-200">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="288a9-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-202">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистеммакспроцессес ")</span><span class="sxs-lookup"><span data-stu-id="288a9-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-203">Максимальное число контекстов процессов, которое может поддерживать операционная система.</span><span class="sxs-lookup"><span data-stu-id="288a9-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="288a9-204">Если фиксированного максимума нет, значение должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="288a9-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="288a9-205">В системах с фиксированным максимальным значением этот объект может помочь в диагностике сбоев, возникающих при достижении максимального значения.</span><span class="sxs-lookup"><span data-stu-id="288a9-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="288a9-206">Если значение неизвестно, введите-1.</span><span class="sxs-lookup"><span data-stu-id="288a9-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-207">**макспроцессмеморисизе**</span><span class="sxs-lookup"><span data-stu-id="288a9-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-208">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-210">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-211">Максимальный объем памяти в килобайтах, который может быть выделен процессу.</span><span class="sxs-lookup"><span data-stu-id="288a9-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="288a9-212">Для операционных систем без виртуальной памяти это значение обычно равно общему объему физической памяти, за вычетом памяти, используемой BIOS и операционной системой.</span><span class="sxs-lookup"><span data-stu-id="288a9-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="288a9-213">Для некоторых операционных систем это значение может быть бесконечным, в этом случае следует указать 0.</span><span class="sxs-lookup"><span data-stu-id="288a9-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="288a9-214">В других случаях это значение может быть константой, например 2 ГБ или 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="288a9-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="288a9-215">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-216">**Name**</span><span class="sxs-lookup"><span data-stu-id="288a9-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-219">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="288a9-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-220">Ключ экземпляра операционной системы в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="288a9-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="288a9-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-222">**нумберофлиценседусерс**</span><span class="sxs-lookup"><span data-stu-id="288a9-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-223">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="288a9-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="288a9-225">Число пользовательских лицензий для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="288a9-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="288a9-226">Если значение не ограничено, введите 0, если неизвестно, введите-1.</span><span class="sxs-lookup"><span data-stu-id="288a9-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-227">**нумберофпроцессес**</span><span class="sxs-lookup"><span data-stu-id="288a9-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-228">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="288a9-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-230">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемпроцессес ")</span><span class="sxs-lookup"><span data-stu-id="288a9-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-231">Количество контекстов процессов, загруженных или выполняемых в операционной системе в данный момент.</span><span class="sxs-lookup"><span data-stu-id="288a9-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-232">**нумберофусерс**</span><span class="sxs-lookup"><span data-stu-id="288a9-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-233">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="288a9-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-235">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемнумусерс ")</span><span class="sxs-lookup"><span data-stu-id="288a9-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-236">Число пользовательских сеансов, для которых операционная система в настоящее время хранит сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="288a9-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="288a9-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="288a9-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="288a9-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-240">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**система \_ CIM**".**Осертипедескриптион**")</span><span class="sxs-lookup"><span data-stu-id="288a9-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-241">Тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="288a9-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="288a9-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="288a9-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="288a9-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="288a9-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="288a9-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="288a9-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-245">MacOS</span><span class="sxs-lookup"><span data-stu-id="288a9-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="288a9-246"><span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)</span><span class="sxs-lookup"><span data-stu-id="288a9-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-247">АТРИ UNIX</span><span class="sxs-lookup"><span data-stu-id="288a9-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="288a9-248"><span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)</span><span class="sxs-lookup"><span data-stu-id="288a9-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="288a9-249"><span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)</span><span class="sxs-lookup"><span data-stu-id="288a9-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="288a9-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="288a9-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="288a9-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)</span><span class="sxs-lookup"><span data-stu-id="288a9-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-252">Открытые виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="288a9-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="288a9-253"><span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)</span><span class="sxs-lookup"><span data-stu-id="288a9-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="288a9-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="288a9-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="288a9-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="288a9-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="288a9-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="288a9-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="288a9-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="288a9-258"><span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)</span><span class="sxs-lookup"><span data-stu-id="288a9-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="288a9-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)</span><span class="sxs-lookup"><span data-stu-id="288a9-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-260">Виртуальная машина Майкрософт (VM) для Java</span><span class="sxs-lookup"><span data-stu-id="288a9-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="288a9-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="288a9-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="288a9-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="288a9-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="288a9-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="288a9-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="288a9-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="288a9-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="288a9-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="288a9-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="288a9-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="288a9-268"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="288a9-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="288a9-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="288a9-270"><span id="WINCE"></span><span id="wince"></span>**Wince** (19)</span><span class="sxs-lookup"><span data-stu-id="288a9-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="288a9-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="288a9-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="288a9-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-273">НКР 3000</span><span class="sxs-lookup"><span data-stu-id="288a9-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="288a9-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="288a9-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="288a9-275"><span id="OSF"></span><span id="osf"></span>**Использование** (22)</span><span class="sxs-lookup"><span data-stu-id="288a9-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="288a9-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="288a9-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="288a9-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Зависящая от UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="288a9-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="288a9-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="288a9-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="288a9-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)</span><span class="sxs-lookup"><span data-stu-id="288a9-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="288a9-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)</span><span class="sxs-lookup"><span data-stu-id="288a9-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="288a9-281"><span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)</span><span class="sxs-lookup"><span data-stu-id="288a9-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="288a9-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="288a9-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="288a9-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)</span><span class="sxs-lookup"><span data-stu-id="288a9-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="288a9-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="288a9-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="288a9-285"><span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)</span><span class="sxs-lookup"><span data-stu-id="288a9-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-286">Серия</span><span class="sxs-lookup"><span data-stu-id="288a9-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="288a9-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)</span><span class="sxs-lookup"><span data-stu-id="288a9-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-288">Сдвоенная НСК</span><span class="sxs-lookup"><span data-stu-id="288a9-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="288a9-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)</span><span class="sxs-lookup"><span data-stu-id="288a9-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-290">Удвоить NT</span><span class="sxs-lookup"><span data-stu-id="288a9-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="288a9-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="288a9-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="288a9-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="288a9-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="288a9-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="288a9-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)</span><span class="sxs-lookup"><span data-stu-id="288a9-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="288a9-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="288a9-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="288a9-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="288a9-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="288a9-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Интерактивная UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="288a9-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="288a9-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)</span><span class="sxs-lookup"><span data-stu-id="288a9-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-299">ОС BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="288a9-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="288a9-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="288a9-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="288a9-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)</span><span class="sxs-lookup"><span data-stu-id="288a9-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="288a9-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)</span><span class="sxs-lookup"><span data-stu-id="288a9-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="288a9-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="288a9-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="288a9-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="288a9-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)</span><span class="sxs-lookup"><span data-stu-id="288a9-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="288a9-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)</span><span class="sxs-lookup"><span data-stu-id="288a9-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="288a9-307"><span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)</span><span class="sxs-lookup"><span data-stu-id="288a9-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="288a9-308"><span id="EPOC"></span><span id="epoc"></span>**Епок** (49)</span><span class="sxs-lookup"><span data-stu-id="288a9-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="288a9-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)</span><span class="sxs-lookup"><span data-stu-id="288a9-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="288a9-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)</span><span class="sxs-lookup"><span data-stu-id="288a9-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="288a9-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="288a9-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="288a9-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)</span><span class="sxs-lookup"><span data-stu-id="288a9-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="288a9-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="288a9-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="288a9-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="288a9-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="288a9-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)</span><span class="sxs-lookup"><span data-stu-id="288a9-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="288a9-316">ОС Palm</span><span class="sxs-lookup"><span data-stu-id="288a9-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="288a9-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)</span><span class="sxs-lookup"><span data-stu-id="288a9-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="288a9-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="288a9-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="288a9-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)</span><span class="sxs-lookup"><span data-stu-id="288a9-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="288a9-320"><span id="OS_390"></span><span id="os_390"></span>**ОС/390** (60)</span><span class="sxs-lookup"><span data-stu-id="288a9-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="288a9-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="288a9-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="288a9-322"><span id="TPF"></span><span id="tpf"></span>**ТПФ** (62)</span><span class="sxs-lookup"><span data-stu-id="288a9-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="288a9-323">**осертипедескриптион**</span><span class="sxs-lookup"><span data-stu-id="288a9-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-326">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**модель \_ CIM**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="288a9-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-327">Описывает производителя и тип операционной системы, если свойство **OSType** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="288a9-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="288a9-328">Формат строки, вставляемой в **осертипедескриптион** , должен быть аналогичен строкам **значений** , определенным для **OSType**.</span><span class="sxs-lookup"><span data-stu-id="288a9-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="288a9-329">Для этого свойства следует задать значение null, если **OSType** имеет значение, отличное от 1 (одно).</span><span class="sxs-lookup"><span data-stu-id="288a9-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-330">**сизесторединпагингфилес**</span><span class="sxs-lookup"><span data-stu-id="288a9-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-331">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Параметры системной памяти DMTF \| 001,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="288a9-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-334">Количество килобайтов, которые могут храниться в файлах подкачки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="288a9-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="288a9-335">Это число не представляет фактический физический размер файла подкачки на диске.</span><span class="sxs-lookup"><span data-stu-id="288a9-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="288a9-336">Значение 0 (ноль) указывает, что файлы подкачки отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="288a9-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="288a9-337">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-338">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="288a9-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-341">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="288a9-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-342">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="288a9-342">Current status of the object.</span></span>

<span data-ttu-id="288a9-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="288a9-344">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="288a9-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="288a9-345">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="288a9-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="288a9-346">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="288a9-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="288a9-347">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="288a9-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="288a9-348">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="288a9-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="288a9-349">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="288a9-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="288a9-350">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="288a9-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="288a9-351">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="288a9-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="288a9-352">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="288a9-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="288a9-353">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="288a9-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="288a9-354">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="288a9-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="288a9-355">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="288a9-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="288a9-356">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="288a9-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="288a9-357">**тоталсвапспацесизе**</span><span class="sxs-lookup"><span data-stu-id="288a9-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-358">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-360">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-361">Общий объем области подкачки, в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="288a9-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="288a9-362">Это значение может быть равно null (не указано), если пространство подкачки не отличается от файлов страниц.</span><span class="sxs-lookup"><span data-stu-id="288a9-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="288a9-363">Однако некоторые операционные системы отличают эти понятия.</span><span class="sxs-lookup"><span data-stu-id="288a9-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="288a9-364">Например, все процессы могут быть "переключены" в UNIX, когда список свободных страниц опускается и остается ниже заданного значения.</span><span class="sxs-lookup"><span data-stu-id="288a9-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="288a9-365">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-366">**тоталвиртуалмеморисизе**</span><span class="sxs-lookup"><span data-stu-id="288a9-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-367">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-369">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-370">Объем виртуальной памяти в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="288a9-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="288a9-371">Например, вычислите это, добавив общий объем ОЗУ к объему пространства для разбиения на страницы (т. е. добавить объем памяти, выданный компьютером или агрегированный системой, в свойство **сизесторединпагингфилес** .</span><span class="sxs-lookup"><span data-stu-id="288a9-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="288a9-372">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-373">**тоталвисиблемеморисизе**</span><span class="sxs-lookup"><span data-stu-id="288a9-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-374">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="288a9-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-376">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="288a9-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-377">Общий объем физической памяти в килобайтах, доступный операционной системе.</span><span class="sxs-lookup"><span data-stu-id="288a9-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="288a9-378">Это значение не обязательно указывает на истинный объем физической памяти, но сообщает операционной системе, как она доступна.</span><span class="sxs-lookup"><span data-stu-id="288a9-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="288a9-379">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="288a9-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="288a9-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="288a9-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="288a9-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="288a9-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="288a9-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="288a9-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="288a9-383">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Операционная система DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="288a9-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="288a9-384">Версия операции.</span><span class="sxs-lookup"><span data-stu-id="288a9-384">Version of the operation.</span></span>

<span data-ttu-id="288a9-385">Версия операции должна быть в одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="288a9-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="288a9-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="288a9-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="288a9-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="288a9-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="288a9-388">Комментарии</span><span class="sxs-lookup"><span data-stu-id="288a9-388">Remarks</span></span>

<span data-ttu-id="288a9-389">Класс **\_ операционной системы CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="288a9-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="288a9-390">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="288a9-390">WMI does not implement this class.</span></span> <span data-ttu-id="288a9-391">Сведения о классах WMI, которые являются производными от CIM, см. в разделе [Классы Win32](win32-provider.md). **\_**</span><span class="sxs-lookup"><span data-stu-id="288a9-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="288a9-392">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="288a9-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="288a9-393">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="288a9-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="288a9-394">Требования</span><span class="sxs-lookup"><span data-stu-id="288a9-394">Requirements</span></span>



| <span data-ttu-id="288a9-395">Требование</span><span class="sxs-lookup"><span data-stu-id="288a9-395">Requirement</span></span> | <span data-ttu-id="288a9-396">Значение</span><span class="sxs-lookup"><span data-stu-id="288a9-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="288a9-397">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="288a9-397">Minimum supported client</span></span><br/> | <span data-ttu-id="288a9-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="288a9-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="288a9-399">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="288a9-399">Minimum supported server</span></span><br/> | <span data-ttu-id="288a9-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="288a9-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="288a9-401">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="288a9-401">Namespace</span></span><br/>                | <span data-ttu-id="288a9-402">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="288a9-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="288a9-403">MOF</span><span class="sxs-lookup"><span data-stu-id="288a9-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="288a9-404"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="288a9-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="288a9-405">DLL</span><span class="sxs-lookup"><span data-stu-id="288a9-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="288a9-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="288a9-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="288a9-407">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="288a9-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288a9-408">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="288a9-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

