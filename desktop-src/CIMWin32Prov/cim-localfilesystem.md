---
description: Класс CIM \_ локалфилесистем представляет хранилище файлов, контролируемое компьютерной системой с помощью локальных средств (например, прямой доступ к драйверу устройства).
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: Класс CIM_LocalFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896005"
---
# <a name="cim_localfilesystem-class"></a><span data-ttu-id="47b6c-103">\_Класс CIM локалфилесистем</span><span class="sxs-lookup"><span data-stu-id="47b6c-103">CIM\_LocalFileSystem class</span></span>

<span data-ttu-id="47b6c-104">Класс **CIM \_ локалфилесистем** представляет хранилище файлов, контролируемое компьютерной системой с помощью локальных средств (например, прямой доступ к драйверу устройства).</span><span class="sxs-lookup"><span data-stu-id="47b6c-104">The **CIM\_LocalFileSystem** class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="47b6c-105">Хранилище файлов может управляться непосредственно компьютерной системой без необходимости использовать другой компьютер в качестве файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="47b6c-105">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="47b6c-106">Однако для кластерной файловой системы файловая система является локальной и, следовательно, откладывается на кластер.</span><span class="sxs-lookup"><span data-stu-id="47b6c-106">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47b6c-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="47b6c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="47b6c-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="47b6c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="47b6c-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="47b6c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="47b6c-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="47b6c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b6c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47b6c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
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

## <a name="members"></a><span data-ttu-id="47b6c-112">Члены</span><span class="sxs-lookup"><span data-stu-id="47b6c-112">Members</span></span>

<span data-ttu-id="47b6c-113">Класс **CIM \_ локалфилесистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="47b6c-113">The **CIM\_LocalFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="47b6c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="47b6c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47b6c-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="47b6c-115">Properties</span></span>

<span data-ttu-id="47b6c-116">Класс **CIM \_ локалфилесистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="47b6c-116">The **CIM\_LocalFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47b6c-117">**аваилаблеспаце**</span><span class="sxs-lookup"><span data-stu-id="47b6c-117">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-118">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="47b6c-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-120">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Раздел DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-121">Объем свободного места в байтах для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="47b6c-121">Amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="47b6c-122">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="47b6c-122">If unknown, enter 0.</span></span>

<span data-ttu-id="47b6c-123">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="47b6c-123">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="47b6c-124">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-124">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-125">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="47b6c-125">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="47b6c-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-128">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="47b6c-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-129">Размер блока файловой системы для хранения и извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="47b6c-129">Block size of the file system for data storage and retrieval.</span></span>

<span data-ttu-id="47b6c-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="47b6c-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="47b6c-131">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-131">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-132">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="47b6c-132">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-135">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="47b6c-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-136">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="47b6c-136">A short textual description of the object.</span></span>

<span data-ttu-id="47b6c-137">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-138">**касепресервед**</span><span class="sxs-lookup"><span data-stu-id="47b6c-138">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47b6c-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-141">Если **значение равно true**, регистр имен файлов сохраняется.</span><span class="sxs-lookup"><span data-stu-id="47b6c-141">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="47b6c-142">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-142">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-143">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="47b6c-143">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47b6c-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-146">**Значение true** показывает, что имена файлов с учетом регистра поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="47b6c-146">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="47b6c-147">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-147">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-148">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="47b6c-148">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-149">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="47b6c-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-151">Массив, определяющий наборы символов или кодировку, поддерживаемые файловой системой.</span><span class="sxs-lookup"><span data-stu-id="47b6c-151">Array that defines the character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="47b6c-152">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-152">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="47b6c-153">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="47b6c-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="47b6c-154">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="47b6c-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="47b6c-155">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="47b6c-155">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="47b6c-156">**Юникод** (3)</span><span class="sxs-lookup"><span data-stu-id="47b6c-156">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="47b6c-157">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="47b6c-157">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="47b6c-158">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="47b6c-158">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="47b6c-159">**Расширенный код UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="47b6c-159">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="47b6c-160">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="47b6c-160">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="47b6c-161">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="47b6c-161">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="47b6c-162">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="47b6c-162">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-165">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-166">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="47b6c-166">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="47b6c-167">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="47b6c-167">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="47b6c-168">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="47b6c-168">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="47b6c-169">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="47b6c-169">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="47b6c-170">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-170">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="47b6c-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-174">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="47b6c-174">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-175">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="47b6c-175">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="47b6c-176">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="47b6c-176">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="47b6c-177">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-177">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-178">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="47b6c-178">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-181">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="47b6c-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-182">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="47b6c-182">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="47b6c-183">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-183">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-184">**CSName**</span><span class="sxs-lookup"><span data-stu-id="47b6c-184">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-187">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="47b6c-187">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-188">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="47b6c-188">Scoping computer system's name.</span></span>

<span data-ttu-id="47b6c-189">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-189">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-190">**Описание**</span><span class="sxs-lookup"><span data-stu-id="47b6c-190">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-193">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="47b6c-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-194">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="47b6c-194">A textual description of the object.</span></span>

<span data-ttu-id="47b6c-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-196">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="47b6c-196">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-199">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-200">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="47b6c-200">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="47b6c-201">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="47b6c-201">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="47b6c-202">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="47b6c-202">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="47b6c-203">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="47b6c-203">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="47b6c-204">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-204">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-205">**филесистемсизе**</span><span class="sxs-lookup"><span data-stu-id="47b6c-205">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-206">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="47b6c-206">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-208">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="47b6c-208">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-209">Размер файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="47b6c-209">Size of the file system, in bytes.</span></span> <span data-ttu-id="47b6c-210">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="47b6c-210">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="47b6c-211">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="47b6c-211">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="47b6c-212">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-212">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-213">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="47b6c-213">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-214">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="47b6c-214">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-216">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-217">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="47b6c-217">Indicates when the object was installed.</span></span> <span data-ttu-id="47b6c-218">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="47b6c-218">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="47b6c-219">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-219">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-220">**максфиленамеленгс**</span><span class="sxs-lookup"><span data-stu-id="47b6c-220">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47b6c-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-223">Максимальная длина имени файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="47b6c-223">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="47b6c-224">Значение 0 (ноль) указывает на отсутствие ограничения на длину имени файла.</span><span class="sxs-lookup"><span data-stu-id="47b6c-224">A value of 0 (zero) indicates that there is no limit to the file name length.</span></span>

<span data-ttu-id="47b6c-225">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-225">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-226">**Name**</span><span class="sxs-lookup"><span data-stu-id="47b6c-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-229">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="47b6c-229">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-230">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="47b6c-230">Label by which the object is known.</span></span> <span data-ttu-id="47b6c-231">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="47b6c-231">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="47b6c-232">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-233">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="47b6c-233">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-234">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="47b6c-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-236">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсакцесс ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-236">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-237">Если **значение — true**, файловая система предназначена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="47b6c-237">If **TRUE**, the file system is designated as read only.</span></span>

<span data-ttu-id="47b6c-238">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-238">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-239">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="47b6c-239">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-242">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсмаунтпоинт ")</span><span class="sxs-lookup"><span data-stu-id="47b6c-242">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-243">Имя пути или другие сведения, определяющие корень файловой системы.</span><span class="sxs-lookup"><span data-stu-id="47b6c-243">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="47b6c-244">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-244">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="47b6c-245">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="47b6c-245">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47b6c-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="47b6c-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="47b6c-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47b6c-248">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="47b6c-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="47b6c-249">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="47b6c-249">String that indicates the current status of the object.</span></span> <span data-ttu-id="47b6c-250">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="47b6c-250">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="47b6c-251">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="47b6c-251">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="47b6c-252">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="47b6c-252">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="47b6c-253">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="47b6c-253">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="47b6c-254">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="47b6c-254">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="47b6c-255">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="47b6c-255">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="47b6c-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="47b6c-257">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="47b6c-257">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="47b6c-258">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="47b6c-258">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="47b6c-259">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="47b6c-259">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="47b6c-260">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="47b6c-260">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="47b6c-261">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="47b6c-261">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="47b6c-262">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="47b6c-262">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="47b6c-263">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="47b6c-263">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="47b6c-264">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="47b6c-264">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="47b6c-265">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="47b6c-265">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="47b6c-266">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="47b6c-266">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="47b6c-267">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="47b6c-267">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="47b6c-268">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="47b6c-268">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="47b6c-269">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="47b6c-269">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="47b6c-270"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="47b6c-270"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="47b6c-271">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47b6c-271">Remarks</span></span>

<span data-ttu-id="47b6c-272">Класс **CIM \_ локалфилесистем** является производным от [**\_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="47b6c-272">The **CIM\_LocalFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="47b6c-273">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="47b6c-273">WMI does not implement this class.</span></span>

<span data-ttu-id="47b6c-274">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="47b6c-274">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="47b6c-275">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="47b6c-275">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b6c-276">Требования</span><span class="sxs-lookup"><span data-stu-id="47b6c-276">Requirements</span></span>



| <span data-ttu-id="47b6c-277">Требование</span><span class="sxs-lookup"><span data-stu-id="47b6c-277">Requirement</span></span> | <span data-ttu-id="47b6c-278">Значение</span><span class="sxs-lookup"><span data-stu-id="47b6c-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47b6c-279">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47b6c-279">Minimum supported client</span></span><br/> | <span data-ttu-id="47b6c-280">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47b6c-280">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47b6c-281">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47b6c-281">Minimum supported server</span></span><br/> | <span data-ttu-id="47b6c-282">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47b6c-282">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47b6c-283">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47b6c-283">Namespace</span></span><br/>                | <span data-ttu-id="47b6c-284">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="47b6c-284">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47b6c-285">MOF</span><span class="sxs-lookup"><span data-stu-id="47b6c-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47b6c-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47b6c-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47b6c-287">DLL</span><span class="sxs-lookup"><span data-stu-id="47b6c-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47b6c-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47b6c-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47b6c-289">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47b6c-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b6c-290">**\_Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="47b6c-290">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

