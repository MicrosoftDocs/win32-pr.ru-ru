---
description: '\_Файл подкачки Win32&\# 32; Класс WMI представляет файл, используемый для обработки обмена файлами виртуальной памяти в системе Win32. Этот класс не рекомендуется к использованию.'
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Класс Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656011"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="a9cb7-104">\_Класс файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="a9cb7-104">Win32\_PageFile class</span></span>

<span data-ttu-id="a9cb7-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ файла подкачки Win32** представляет файл, используемый для обработки страничной замены файла виртуальной памяти в системе Win32.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="a9cb7-106">Этот класс не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-106">This class has been deprecated.</span></span>

<span data-ttu-id="a9cb7-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a9cb7-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9cb7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9cb7-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="a9cb7-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a9cb7-110">Members</span></span>

<span data-ttu-id="a9cb7-111">Класс **\_ файла подкачки Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="a9cb7-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a9cb7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9cb7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9cb7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9cb7-114">Методы</span><span class="sxs-lookup"><span data-stu-id="a9cb7-114">Methods</span></span>

<span data-ttu-id="a9cb7-115">Класс **\_ файла подкачки Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="a9cb7-116">Метод</span><span class="sxs-lookup"><span data-stu-id="a9cb7-116">Method</span></span>                                                                                            | <span data-ttu-id="a9cb7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a9cb7-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9cb7-118">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="a9cb7-119">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a9cb7-120">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="a9cb7-121">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a9cb7-122">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="a9cb7-123">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a9cb7-124">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="a9cb7-125">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a9cb7-126">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="a9cb7-127">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="a9cb7-128">**копекс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="a9cb7-129">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром FileName.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a9cb7-130">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="a9cb7-131">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="a9cb7-132">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="a9cb7-133">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="a9cb7-134">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="a9cb7-135">Метод класса, определяющий, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом *разрешения* , не только для объекта File, но и для общего ресурса, в котором находится файл или каталог (если он находится в общей папке).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="a9cb7-136">**Имени**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="a9cb7-137">Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="a9cb7-138">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="a9cb7-139">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="a9cb7-140">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="a9cb7-141">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="a9cb7-142">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="a9cb7-143">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a9cb7-144">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="a9cb7-145">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="a9cb7-146">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9cb7-146">Properties</span></span>

<span data-ttu-id="a9cb7-147">Класс **\_ файла подкачки Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9cb7-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-151">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-152">Битовая маска, представляющая права доступа, необходимые для доступа к файлу или выполнения конкретных операций над ним.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="a9cb7-153">Значения см. в разделе [**константы прав доступа к файлам и каталогам**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="a9cb7-154">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a9cb7-155">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="a9cb7-156">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a9cb7-157">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="a9cb7-158">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="a9cb7-159">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="a9cb7-160">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="a9cb7-161">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="a9cb7-162">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="a9cb7-163">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="a9cb7-164">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="a9cb7-165">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="a9cb7-166">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="a9cb7-167">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="a9cb7-168">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9cb7-169">**Архив**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-172">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-173">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="a9cb7-174">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-175">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-178">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-179">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-179">A short textual description of the object.</span></span>

<span data-ttu-id="a9cb7-180">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-182">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-184">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-185">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="a9cb7-186">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-187">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-190">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-191">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a9cb7-192">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="a9cb7-193">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="a9cb7-194">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="a9cb7-195">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-199">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-200">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-200">Name of the class.</span></span>

<span data-ttu-id="a9cb7-201">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-203">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-205">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-206">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="a9cb7-207">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-208">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-211">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-212">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-212">Class of the computer system.</span></span>

<span data-ttu-id="a9cb7-213">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-217">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-218">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-218">Name of the computer system.</span></span>

<span data-ttu-id="a9cb7-219">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-220">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-223">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-224">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-224">A textual description of the object.</span></span>

<span data-ttu-id="a9cb7-225">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-226">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-229">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("диск")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-230">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="a9cb7-231">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a9cb7-232">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="a9cb7-232">Example: "c:"</span></span>

<span data-ttu-id="a9cb7-233">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-234">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-237">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-238">Имя файла, совместимое с DOS.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-238">DOS-compatible file name.</span></span>

<span data-ttu-id="a9cb7-239">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="a9cb7-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="a9cb7-240">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-241">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-242">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-244">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-245">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="a9cb7-246">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-250">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-251">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="a9cb7-252">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="a9cb7-253">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="a9cb7-254">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="a9cb7-255">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-256">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-259">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-260">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="a9cb7-261">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="a9cb7-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="a9cb7-262">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-266">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-267">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-267">File name without the file name extension.</span></span> <span data-ttu-id="a9cb7-268">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="a9cb7-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="a9cb7-269">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-270">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-271">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-273">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("размер"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-274">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="a9cb7-275">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="a9cb7-276">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-280">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-281">Дескриптор, представляющий тип файла, указанный в свойстве **Extension** .</span><span class="sxs-lookup"><span data-stu-id="a9cb7-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="a9cb7-282">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-284">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-286">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| дваваилпажефиле"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-287">Место, доступное в файле подкачки.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-287">Space available in the paging file.</span></span> <span data-ttu-id="a9cb7-288">Операционная система может увеличить файл подкачки по мере необходимости, вплоть до ограничения, наложенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="a9cb7-289">Это свойство показывает разницу между размером текущей выделенной памяти и текущим размером файла подкачки. Он не показывает самый крупный возможный размер файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-290">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-293">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-294">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-294">Class of the file system.</span></span>

<span data-ttu-id="a9cb7-295">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-296">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-299">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-300">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-300">Name of the file system.</span></span>

<span data-ttu-id="a9cb7-301">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-302">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-303">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-305">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-306">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="a9cb7-307">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-308">**инитиалсизе**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-309">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-311">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ управления \\ \\ \\ \\ памятью диспетчер сеансов \| пагингфилес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-312">Начальный размер файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-314">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-316">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-317">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-317">Indicates when the object was installed.</span></span> <span data-ttu-id="a9cb7-318">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a9cb7-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-320">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-321">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-323">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-324">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="a9cb7-325">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="a9cb7-326">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-327">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-328">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-330">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-331">Дата и время последнего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="a9cb7-332">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-334">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-336">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-337">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="a9cb7-338">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-339">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-342">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-343">Строка производителя из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="a9cb7-344">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-346">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-348">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| двтоталпажефиле"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-349">Максимальный размер файла подкачки, заданный пользователем.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="a9cb7-350">Операционная система не позволит файлу подкачки превысить это ограничение.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-351">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-354">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**переопределять**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**нткуерисистеминформатион**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| системпажефилеинформатион \| пажефиленаме")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-355">Имя файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-355">Name of the page file.</span></span>

<span data-ttu-id="a9cb7-356">Пример: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="a9cb7-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-357">**Путь**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-360">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("путь")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-361">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="a9cb7-362">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="a9cb7-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="a9cb7-363">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-364">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-365">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-367">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-368">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="a9cb7-369">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-370">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-373">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-374">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="a9cb7-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a9cb7-376">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a9cb7-377">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a9cb7-378">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a9cb7-379">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9cb7-380">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a9cb7-381">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a9cb7-382">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a9cb7-383">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a9cb7-384">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a9cb7-385">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a9cb7-386">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a9cb7-387">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a9cb7-388">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9cb7-389">**Система**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-390">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-392">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-393">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="a9cb7-394">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-398">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("версия")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-399">Строка версии из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="a9cb7-400">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9cb7-401">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9cb7-402">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9cb7-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9cb7-404">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="a9cb7-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="a9cb7-405">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="a9cb7-406">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9cb7-407">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9cb7-407">Remarks</span></span>

<span data-ttu-id="a9cb7-408">Класс **\_ файла подкачки Win32** является производным от [**\_ каталога CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="a9cb7-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a9cb7-409">Примеры</span><span class="sxs-lookup"><span data-stu-id="a9cb7-409">Examples</span></span>

<span data-ttu-id="a9cb7-410">В следующем образце кода VBScript показано, как получить статистику файла **\_ подкачки** из экземпляров файла данных Win32.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="a9cb7-411">В следующем образце кода Perl показано, как извлекать статистику файлов **\_ подкачки из экземпляров файлового файла Win32**.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="a9cb7-412">Требования</span><span class="sxs-lookup"><span data-stu-id="a9cb7-412">Requirements</span></span>



| <span data-ttu-id="a9cb7-413">Требование</span><span class="sxs-lookup"><span data-stu-id="a9cb7-413">Requirement</span></span> | <span data-ttu-id="a9cb7-414">Значение</span><span class="sxs-lookup"><span data-stu-id="a9cb7-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9cb7-415">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9cb7-415">Minimum supported client</span></span><br/> | <span data-ttu-id="a9cb7-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9cb7-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9cb7-417">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9cb7-417">Minimum supported server</span></span><br/> | <span data-ttu-id="a9cb7-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9cb7-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9cb7-419">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9cb7-419">Namespace</span></span><br/>                | <span data-ttu-id="a9cb7-420">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a9cb7-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9cb7-421">MOF</span><span class="sxs-lookup"><span data-stu-id="a9cb7-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9cb7-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9cb7-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9cb7-423">DLL</span><span class="sxs-lookup"><span data-stu-id="a9cb7-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9cb7-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9cb7-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9cb7-425">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9cb7-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9cb7-426">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="a9cb7-427">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="a9cb7-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
