---
description: Класс CIM \_ LogicalFile представляет именованную коллекцию данных, которая может быть исполняемым кодом, расположенным в файловой системе в экстенте хранения.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: Класс CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655738"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="6d9ad-103">\_Класс CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="6d9ad-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="6d9ad-104">Класс **CIM \_ LogicalFile** представляет именованную коллекцию данных, которая может быть исполняемым кодом, расположенным в файловой системе в экстенте хранения.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d9ad-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6d9ad-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6d9ad-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6d9ad-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9ad-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d9ad-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="6d9ad-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6d9ad-110">Members</span></span>

<span data-ttu-id="6d9ad-111">Класс **CIM \_ LogicalFile** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d9ad-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="6d9ad-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6d9ad-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d9ad-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d9ad-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d9ad-114">Методы</span><span class="sxs-lookup"><span data-stu-id="6d9ad-114">Methods</span></span>

<span data-ttu-id="6d9ad-115">Класс **CIM \_ LogicalFile** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="6d9ad-116">Метод</span><span class="sxs-lookup"><span data-stu-id="6d9ad-116">Method</span></span>                                                                                             | <span data-ttu-id="6d9ad-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6d9ad-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d9ad-118">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="6d9ad-119">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6d9ad-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6d9ad-121">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="6d9ad-122">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6d9ad-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6d9ad-124">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="6d9ad-125">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="6d9ad-127">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="6d9ad-128">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-129">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="6d9ad-130">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="6d9ad-131">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6d9ad-132">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6d9ad-133">**копекс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="6d9ad-134">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6d9ad-135">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6d9ad-136">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="6d9ad-137">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-138">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6d9ad-139">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="6d9ad-140">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-141">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6d9ad-142">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="6d9ad-143">Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="6d9ad-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="6d9ad-144">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="6d9ad-145">**Имени**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="6d9ad-146">Переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-147">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6d9ad-148">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="6d9ad-149">Получает владение логическим файлом (или каталогом), указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-150">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="6d9ad-151">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="6d9ad-152">Получает владение логическим файлом (или каталогом), указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-153">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="6d9ad-154">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="6d9ad-155">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-156">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="6d9ad-157">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="6d9ad-158">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6d9ad-159">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="6d9ad-160">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d9ad-160">Properties</span></span>

<span data-ttu-id="6d9ad-161">Класс **CIM \_ LogicalFile** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d9ad-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-165">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-166">Битовая маска, представляющая права доступа, необходимые для доступа к файлу или выполнения конкретных операций над ним.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="6d9ad-167">Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="6d9ad-168">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6d9ad-169">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6d9ad-170">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6d9ad-171">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6d9ad-172">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6d9ad-173">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6d9ad-174">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6d9ad-175">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6d9ad-176">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6d9ad-177">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6d9ad-178">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6d9ad-179">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6d9ad-180">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6d9ad-181">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6d9ad-182">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d9ad-183">**Архив**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-186">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-187">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-188">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-191">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-192">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-192">A short textual description of the object.</span></span>

<span data-ttu-id="6d9ad-193">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-195">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-197">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-198">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-199">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-202">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-203">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6d9ad-204">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6d9ad-205">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6d9ad-206">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-210">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-211">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-213">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-215">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-216">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-217">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-220">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-221">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-225">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-226">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-227">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-230">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-231">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-231">A textual description of the object.</span></span>

<span data-ttu-id="6d9ad-232">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-233">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-236">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-237">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="6d9ad-238">Это свойство наследуется от **CIM \_ LogicalFile**. Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="6d9ad-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-239">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-242">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-243">Имя файла, совместимое с DOS.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-243">DOS-compatible file name.</span></span> <span data-ttu-id="6d9ad-244">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="6d9ad-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-245">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-246">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-248">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-249">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-253">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-254">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6d9ad-255">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6d9ad-256">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6d9ad-257">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-258">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-261">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-262">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="6d9ad-263">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="6d9ad-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-267">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-268">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-268">File name without the file name extension.</span></span> <span data-ttu-id="6d9ad-269">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="6d9ad-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-270">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-271">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-273">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-274">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="6d9ad-275">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-279">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-280">Дескриптор, представляющий тип файла, указанный в свойстве **Extension** .</span><span class="sxs-lookup"><span data-stu-id="6d9ad-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-281">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-284">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-285">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-286">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-289">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-290">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-291">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-292">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-294">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-295">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-297">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-299">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-300">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-300">Indicates when the object was installed.</span></span> <span data-ttu-id="6d9ad-301">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6d9ad-302">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-303">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-304">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-306">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-307">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="6d9ad-308">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-309">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-310">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-312">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-313">Дата и время последнего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-315">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-317">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-318">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-322">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-323">Свойство Name — это строка, представляющая унаследованное имя, которое служит ключом экземпляра логического файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="6d9ad-324">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-324">Full path names should be provided.</span></span> <span data-ttu-id="6d9ad-325">Пример: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="6d9ad-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-326">**Путь**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-329">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-330">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="6d9ad-331">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="6d9ad-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-332">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-333">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-335">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-336">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-337">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-340">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-341">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="6d9ad-342">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6d9ad-343">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6d9ad-344">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6d9ad-345">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="6d9ad-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6d9ad-346">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6d9ad-347">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6d9ad-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6d9ad-349">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6d9ad-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6d9ad-350">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6d9ad-351">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6d9ad-352">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6d9ad-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6d9ad-353">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6d9ad-354">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6d9ad-355">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6d9ad-356">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6d9ad-357">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6d9ad-358">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6d9ad-359">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6d9ad-360">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6d9ad-361">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d9ad-362">**Система**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-363">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-365">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-366">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="6d9ad-367">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9ad-368">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d9ad-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9ad-370">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="6d9ad-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="6d9ad-371">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d9ad-372">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d9ad-372">Remarks</span></span>

<span data-ttu-id="6d9ad-373">Класс **CIM \_ LogicalFile** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="6d9ad-374">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-374">WMI does not implement this class.</span></span> <span data-ttu-id="6d9ad-375">Классы, производные от **CIM \_ LogicalFile**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6d9ad-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6d9ad-376">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6d9ad-377">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6d9ad-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9ad-378">Требования</span><span class="sxs-lookup"><span data-stu-id="6d9ad-378">Requirements</span></span>



| <span data-ttu-id="6d9ad-379">Требование</span><span class="sxs-lookup"><span data-stu-id="6d9ad-379">Requirement</span></span> | <span data-ttu-id="6d9ad-380">Значение</span><span class="sxs-lookup"><span data-stu-id="6d9ad-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9ad-381">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d9ad-381">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9ad-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d9ad-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d9ad-383">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d9ad-383">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9ad-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d9ad-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d9ad-385">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d9ad-385">Namespace</span></span><br/>                | <span data-ttu-id="6d9ad-386">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6d9ad-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d9ad-387">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9ad-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9ad-388"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d9ad-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d9ad-389">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9ad-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9ad-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9ad-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9ad-391">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d9ad-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9ad-392">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="6d9ad-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

