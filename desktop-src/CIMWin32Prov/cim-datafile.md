---
description: '\_Класс файлов данных CIM представляет именованную коллекцию или исполняемый код. Будут возвращены только экземпляры файлов на локальных жестких дисках.'
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: Класс CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896041"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="d1cc1-104">\_Класс файлов CIM</span><span class="sxs-lookup"><span data-stu-id="d1cc1-104">CIM\_DataFile class</span></span>

<span data-ttu-id="d1cc1-105">Класс **\_ файлов данных CIM** представляет именованную коллекцию или исполняемый код.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="d1cc1-106">Будут возвращены только экземпляры файлов на локальных жестких дисках.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1cc1-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1cc1-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1cc1-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1cc1-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cc1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1cc1-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="d1cc1-112">Члены</span><span class="sxs-lookup"><span data-stu-id="d1cc1-112">Members</span></span>

<span data-ttu-id="d1cc1-113">Класс **\_ файлов данных CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1cc1-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="d1cc1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d1cc1-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1cc1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1cc1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1cc1-116">Методы</span><span class="sxs-lookup"><span data-stu-id="d1cc1-116">Methods</span></span>

<span data-ttu-id="d1cc1-117">Класс **\_ файлов данных CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="d1cc1-118">Метод</span><span class="sxs-lookup"><span data-stu-id="d1cc1-118">Method</span></span>                                                                                          | <span data-ttu-id="d1cc1-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d1cc1-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1cc1-120">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="d1cc1-121">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="d1cc1-122">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="d1cc1-123">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="d1cc1-124">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="d1cc1-125">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="d1cc1-126">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="d1cc1-127">Использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-128">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="d1cc1-129">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="d1cc1-130">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-131">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="d1cc1-132">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="d1cc1-133">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="d1cc1-134">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="d1cc1-135">**копекс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="d1cc1-136">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="d1cc1-137">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="d1cc1-138">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="d1cc1-139">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-140">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="d1cc1-141">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="d1cc1-142">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-143">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="d1cc1-144">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="d1cc1-145">Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="d1cc1-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="d1cc1-146">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="d1cc1-147">**Имени**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="d1cc1-148">Переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-149">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="d1cc1-150">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="d1cc1-151">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="d1cc1-152">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="d1cc1-153">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="d1cc1-154">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="d1cc1-155">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="d1cc1-156">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="d1cc1-157">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-158">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="d1cc1-159">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="d1cc1-160">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d1cc1-161">Реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="d1cc1-162">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1cc1-162">Properties</span></span>

<span data-ttu-id="d1cc1-163">Класс **\_ файлов данных CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1cc1-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-167">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-168">Битовая маска, представляющая права доступа, необходимые для доступа к файлу или выполнения конкретных операций над ним.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="d1cc1-169">Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="d1cc1-170">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="d1cc1-171">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="d1cc1-172">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="d1cc1-173">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="d1cc1-174">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="d1cc1-175">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="d1cc1-176">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="d1cc1-177">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="d1cc1-178">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="d1cc1-179">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="d1cc1-180">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="d1cc1-181">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="d1cc1-182">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="d1cc1-183">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="d1cc1-184">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="d1cc1-185">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1cc1-186">**Архив**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-187">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-189">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-190">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="d1cc1-191">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-192">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-195">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-196">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-196">A short textual description of the object.</span></span>

<span data-ttu-id="d1cc1-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-199">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-201">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-202">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="d1cc1-203">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-204">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-207">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-208">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="d1cc1-209">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="d1cc1-210">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="d1cc1-211">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="d1cc1-212">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-216">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-217">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-217">Name of the class.</span></span>

<span data-ttu-id="d1cc1-218">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-220">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-222">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-223">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="d1cc1-224">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-225">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-226">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-228">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-229">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-229">Class of the computer system.</span></span>

<span data-ttu-id="d1cc1-230">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-234">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-235">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-235">Name of the computer system.</span></span>

<span data-ttu-id="d1cc1-236">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-237">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-240">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-241">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-241">A textual description of the object.</span></span>

<span data-ttu-id="d1cc1-242">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-243">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-246">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-247">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="d1cc1-248">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="d1cc1-248">Example: "c:"</span></span>

<span data-ttu-id="d1cc1-249">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-250">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-253">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-254">Имя файла, совместимое с DOS.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-254">DOS-compatible file name.</span></span>

<span data-ttu-id="d1cc1-255">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="d1cc1-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="d1cc1-256">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-257">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-258">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-260">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-261">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="d1cc1-262">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-266">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-267">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="d1cc1-268">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="d1cc1-269">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="d1cc1-270">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="d1cc1-271">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-272">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-273">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-275">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-276">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="d1cc1-277">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="d1cc1-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="d1cc1-278">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-282">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-283">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-283">File name without the file name extension.</span></span> <span data-ttu-id="d1cc1-284">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="d1cc1-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="d1cc1-285">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-286">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-287">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-289">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-290">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="d1cc1-291">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d1cc1-292">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-296">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-297">Дескриптор, представляющий тип файла, указанный в свойстве **Extension** .</span><span class="sxs-lookup"><span data-stu-id="d1cc1-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="d1cc1-298">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-299">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-302">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-303">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-303">Class of the file system.</span></span>

<span data-ttu-id="d1cc1-304">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-305">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-308">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-309">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-309">Name of the file system.</span></span>

<span data-ttu-id="d1cc1-310">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-311">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-314">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-315">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="d1cc1-316">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-318">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-320">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-321">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-321">Indicates when the object was installed.</span></span> <span data-ttu-id="d1cc1-322">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1cc1-323">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-324">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-325">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-327">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-328">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="d1cc1-329">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d1cc1-330">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-331">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-332">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-334">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-335">Дата и время последнего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="d1cc1-336">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-338">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-340">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-341">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="d1cc1-342">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-343">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-346">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-347">Строка производителя из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-348">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-351">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-352">Свойство Name — это строка, представляющая унаследованное имя, которое служит ключом экземпляра логического файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="d1cc1-353">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-353">Full path names should be provided.</span></span>

<span data-ttu-id="d1cc1-354">Пример: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="d1cc1-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="d1cc1-355">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-356">**Путь**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-357">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-359">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-360">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="d1cc1-361">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="d1cc1-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="d1cc1-362">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-363">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-364">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-366">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-367">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="d1cc1-368">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-369">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-372">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-373">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1cc1-374">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1cc1-375">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1cc1-376">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1cc1-377">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="d1cc1-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1cc1-378">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1cc1-379">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1cc1-380">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1cc1-381">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d1cc1-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1cc1-382">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1cc1-383">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1cc1-384">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d1cc1-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1cc1-385">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1cc1-386">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1cc1-387">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1cc1-388">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1cc1-389">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1cc1-390">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1cc1-391">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1cc1-392">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1cc1-393">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1cc1-394">**Система**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-395">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-397">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-398">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="d1cc1-399">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-400">**Version**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-403">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-404">Строка версии из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="d1cc1-405">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1cc1-406">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1cc1-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1cc1-408">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="d1cc1-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="d1cc1-409">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="d1cc1-410">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1cc1-411">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1cc1-411">Remarks</span></span>

<span data-ttu-id="d1cc1-412">Класс **CIM- \_ файла** является производным от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="d1cc1-413">WMI реализует класс **\_ файлов данных CIM** и все его методы.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="d1cc1-414">Класс **\_ файлов CIM** является динамическим классом.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="d1cc1-415">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d1cc1-416">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="d1cc1-417">Из-за соображений безопасности Инструментарий WMI напрямую не поддерживает вызов удаленного компьютера и сообщает ему о необходимости копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="d1cc1-418">Однако можно использовать соответствующий язык программирования для вызова FTP или Robocopy, например.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="d1cc1-419">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1cc1-419">Examples</span></span>

<span data-ttu-id="d1cc1-420">В следующем [примере кода](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) центра сценариев используется класс **\_ файлов данных CIM** в составе приложения большего размера для создания отчетов среды Exchange с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="d1cc1-421">Пример кода " [найти файлы с помощью WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) " в коллекции TechNet **использует \_ файл CIM** для поиска одного или нескольких файлов на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="d1cc1-422">В следующем образце кода VBS описывается выполнение стандартного поиска с помощью подстановочных знаков для файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="d1cc1-423">Обратите внимание, что разделители обратной косой черты должны быть экранированы другой обратной косой чертой ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="d1cc1-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="d1cc1-424">Кроме того, при использовании "**CIM \_ File**".**FileName**. в предложении WHERE процесс Wmiprvse будет проверять все каталоги на любом доступном устройстве хранения.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="d1cc1-425">Это может занять некоторое время, особенно если вы сопоставили удаленные общие папки и можете активировать предупреждения антивирусного по.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="d1cc1-426">Следующий фрагмент кода ограничивает диапазон поиска конкретным диском, путем и расширением файла.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="d1cc1-427">Следующий пример кода PowerShell извлекает одно значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="d1cc1-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="d1cc1-428">Требования</span><span class="sxs-lookup"><span data-stu-id="d1cc1-428">Requirements</span></span>



| <span data-ttu-id="d1cc1-429">Требование</span><span class="sxs-lookup"><span data-stu-id="d1cc1-429">Requirement</span></span> | <span data-ttu-id="d1cc1-430">Значение</span><span class="sxs-lookup"><span data-stu-id="d1cc1-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cc1-431">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1cc1-431">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cc1-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1cc1-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1cc1-433">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1cc1-433">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cc1-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1cc1-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1cc1-435">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1cc1-435">Namespace</span></span><br/>                | <span data-ttu-id="d1cc1-436">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1cc1-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1cc1-437">MOF</span><span class="sxs-lookup"><span data-stu-id="d1cc1-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1cc1-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1cc1-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1cc1-439">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cc1-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1cc1-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cc1-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cc1-441">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1cc1-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cc1-442">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="d1cc1-443">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="d1cc1-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="d1cc1-444">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="d1cc1-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

