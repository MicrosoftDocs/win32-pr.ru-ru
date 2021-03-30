---
description: '\_Класс файловой системы CIM представляет собой файл или набор данных, который является локальным для компьютера или удаленно подключен с файлового сервера.'
ms.assetid: 5a54ab35-b9b6-49e6-96a8-cb2820b054eb
ms.tgt_platform: multiple
title: Класс CIM_FileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSystem
- CIM_FileSystem.Caption
- CIM_FileSystem.Description
- CIM_FileSystem.InstallDate
- CIM_FileSystem.Name
- CIM_FileSystem.Status
- CIM_FileSystem.AvailableSpace
- CIM_FileSystem.BlockSize
- CIM_FileSystem.CasePreserved
- CIM_FileSystem.CaseSensitive
- CIM_FileSystem.CodeSet
- CIM_FileSystem.CompressionMethod
- CIM_FileSystem.CreationClassName
- CIM_FileSystem.CSCreationClassName
- CIM_FileSystem.CSName
- CIM_FileSystem.EncryptionMethod
- CIM_FileSystem.FileSystemSize
- CIM_FileSystem.MaxFileNameLength
- CIM_FileSystem.ReadOnly
- CIM_FileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2795e76c686e8f2bb4079aee376dae397b36f510
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896022"
---
# <a name="cim_filesystem-class"></a><span data-ttu-id="f8a31-103">\_Класс файловой системы CIM</span><span class="sxs-lookup"><span data-stu-id="f8a31-103">CIM\_FileSystem class</span></span>

<span data-ttu-id="f8a31-104">Класс **\_ файловой системы CIM** представляет собой файл или набор данных, который является локальным для компьютера или удаленно подключен с файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="f8a31-104">The **CIM\_FileSystem** class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8a31-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f8a31-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8a31-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8a31-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8a31-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f8a31-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f8a31-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f8a31-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a31-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8a31-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4DA18760-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_FileSystem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a><span data-ttu-id="f8a31-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f8a31-110">Members</span></span>

<span data-ttu-id="f8a31-111">Класс **\_ файловой системы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8a31-111">The **CIM\_FileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="f8a31-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8a31-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8a31-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8a31-113">Properties</span></span>

<span data-ttu-id="f8a31-114">Класс **\_ файловой системы CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8a31-114">The **CIM\_FileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8a31-115">**аваилаблеспаце**</span><span class="sxs-lookup"><span data-stu-id="f8a31-115">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-116">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8a31-116">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Раздел DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-119">Объем свободного места в байтах для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f8a31-119">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="f8a31-120">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="f8a31-120">If unknown, enter 0.</span></span>

<span data-ttu-id="f8a31-121">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f8a31-121">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f8a31-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8a31-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-125">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="f8a31-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-126">Размер блока файловой системы для хранения и извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="f8a31-126">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="f8a31-127">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f8a31-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-128">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f8a31-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-131">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f8a31-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-132">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f8a31-132">A short textual description of the object.</span></span>

<span data-ttu-id="f8a31-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-134">**касепресервед**</span><span class="sxs-lookup"><span data-stu-id="f8a31-134">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8a31-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-137">Если **значение равно true**, регистр имен файлов сохраняется.</span><span class="sxs-lookup"><span data-stu-id="f8a31-137">If **TRUE**, the case of file names are preserved.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-138">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="f8a31-138">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8a31-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-141">**Значение true** показывает, что имена файлов с учетом регистра поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f8a31-141">If **TRUE**, case-sensitive file names are supported.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-142">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="f8a31-142">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-143">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f8a31-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-145">Массив, определяющий наборы символов или кодировку, поддерживаемые файловой системой.</span><span class="sxs-lookup"><span data-stu-id="f8a31-145">Array that defines the character sets or encoding supported by the file system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f8a31-146">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8a31-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f8a31-147">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f8a31-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="f8a31-148">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="f8a31-148">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="f8a31-149">**Юникод** (3)</span><span class="sxs-lookup"><span data-stu-id="f8a31-149">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="f8a31-150">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="f8a31-150">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="f8a31-151">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="f8a31-151">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="f8a31-152">**Расширенный код UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="f8a31-152">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="f8a31-153">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="f8a31-153">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="f8a31-154">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="f8a31-154">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f8a31-155">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="f8a31-155">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-158">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-159">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="f8a31-159">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="f8a31-160">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="f8a31-160">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="f8a31-161">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="f8a31-161">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="f8a31-162">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="f8a31-162">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f8a31-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-166">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f8a31-166">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-167">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f8a31-167">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f8a31-168">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f8a31-168">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-169">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f8a31-169">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-172">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="f8a31-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-173">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f8a31-173">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-174">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f8a31-174">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-177">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="f8a31-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-178">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f8a31-178">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-179">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8a31-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-182">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f8a31-182">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-183">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f8a31-183">A textual description of the object.</span></span>

<span data-ttu-id="f8a31-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-185">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f8a31-185">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-188">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-189">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="f8a31-189">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="f8a31-190">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="f8a31-190">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="f8a31-191">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="f8a31-191">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="f8a31-192">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="f8a31-192">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-193">**филесистемсизе**</span><span class="sxs-lookup"><span data-stu-id="f8a31-193">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-194">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8a31-194">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-196">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="f8a31-196">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-197">Размер файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="f8a31-197">Size of the file system, in bytes.</span></span> <span data-ttu-id="f8a31-198">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f8a31-198">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="f8a31-199">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f8a31-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8a31-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-201">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8a31-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-203">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-204">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="f8a31-204">Indicates when the object was installed.</span></span> <span data-ttu-id="f8a31-205">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f8a31-205">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f8a31-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-207">**максфиленамеленгс**</span><span class="sxs-lookup"><span data-stu-id="f8a31-207">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a31-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-210">Максимальная длина имени файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="f8a31-210">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="f8a31-211">Значение 0 (ноль) указывает на отсутствие ограничения на длину имени файла.</span><span class="sxs-lookup"><span data-stu-id="f8a31-211">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-212">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8a31-212">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-215">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f8a31-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-216">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f8a31-216">Label by which the object is known.</span></span> <span data-ttu-id="f8a31-217">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f8a31-217">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f8a31-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-219">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f8a31-219">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-220">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8a31-220">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-222">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсакцесс ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-223">Если **значение — true**, файловая система предназначена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8a31-223">If **TRUE**, the file system is designated as read only.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-224">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="f8a31-224">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-227">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсмаунтпоинт ")</span><span class="sxs-lookup"><span data-stu-id="f8a31-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-228">Имя пути или другие сведения, определяющие корень файловой системы.</span><span class="sxs-lookup"><span data-stu-id="f8a31-228">Path name or other information that defines the root of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="f8a31-229">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f8a31-229">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8a31-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8a31-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8a31-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8a31-232">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f8a31-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f8a31-233">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f8a31-233">String that indicates the current status of the object.</span></span> <span data-ttu-id="f8a31-234">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="f8a31-234">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f8a31-235">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="f8a31-235">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f8a31-236">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="f8a31-236">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f8a31-237">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="f8a31-237">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f8a31-238">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="f8a31-238">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f8a31-239">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f8a31-239">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f8a31-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f8a31-241">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f8a31-241">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f8a31-242">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f8a31-242">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f8a31-243">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f8a31-243">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f8a31-244">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f8a31-244">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f8a31-245">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f8a31-245">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f8a31-246">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f8a31-246">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f8a31-247">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f8a31-247">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f8a31-248">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f8a31-248">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f8a31-249">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f8a31-249">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f8a31-250">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f8a31-250">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f8a31-251">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f8a31-251">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f8a31-252">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f8a31-252">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f8a31-253">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f8a31-253">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="f8a31-254"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f8a31-254"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f8a31-255">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8a31-255">Remarks</span></span>

<span data-ttu-id="f8a31-256">Класс **\_ файловой системы CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8a31-256">The **CIM\_FileSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f8a31-257">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f8a31-257">WMI does not implement this class.</span></span>

<span data-ttu-id="f8a31-258">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8a31-258">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8a31-259">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f8a31-259">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a31-260">Требования</span><span class="sxs-lookup"><span data-stu-id="f8a31-260">Requirements</span></span>



| <span data-ttu-id="f8a31-261">Требование</span><span class="sxs-lookup"><span data-stu-id="f8a31-261">Requirement</span></span> | <span data-ttu-id="f8a31-262">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a31-262">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a31-263">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8a31-263">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a31-264">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8a31-264">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8a31-265">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8a31-265">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a31-266">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8a31-266">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8a31-267">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8a31-267">Namespace</span></span><br/>                | <span data-ttu-id="f8a31-268">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f8a31-268">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8a31-269">MOF</span><span class="sxs-lookup"><span data-stu-id="f8a31-269">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8a31-270"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8a31-270"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8a31-271">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a31-271">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a31-272"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8a31-272"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a31-273">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8a31-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a31-274">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f8a31-274">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

