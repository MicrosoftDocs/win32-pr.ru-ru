---
description: '&Win32 \_ шорткутфиле \# 32; Класс WMI представляет файлы, которые являются ярлыками для других файлов, каталогов и команд.'
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Класс Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656051"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="6e9dc-103">\_Класс Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="6e9dc-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="6e9dc-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ шорткутфиле для Win32** представляет файлы, которые являются ярлыками для других файлов, каталогов и команд.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="6e9dc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6e9dc-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e9dc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
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
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="6e9dc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6e9dc-108">Members</span></span>

<span data-ttu-id="6e9dc-109">Класс **Win32 \_ шорткутфиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6e9dc-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="6e9dc-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6e9dc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6e9dc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e9dc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6e9dc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6e9dc-112">Methods</span></span>

<span data-ttu-id="6e9dc-113">Класс **Win32 \_ шорткутфиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="6e9dc-114">Метод</span><span class="sxs-lookup"><span data-stu-id="6e9dc-114">Method</span></span>                                                                                                | <span data-ttu-id="6e9dc-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6e9dc-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e9dc-116">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="6e9dc-117">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6e9dc-118">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="6e9dc-119">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6e9dc-120">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="6e9dc-121">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6e9dc-122">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="6e9dc-123">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6e9dc-124">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="6e9dc-125">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="6e9dc-126">**копекс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="6e9dc-127">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="6e9dc-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="6e9dc-128">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="6e9dc-129">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6e9dc-130">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="6e9dc-131">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6e9dc-132">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="6e9dc-133">Метод класса, определяющий, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом разрешения, не только для объекта File, но и для общего ресурса, в котором находится файл или каталог (если он находится в общей папке).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="6e9dc-134">**Имени**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="6e9dc-135">Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6e9dc-136">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="6e9dc-137">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="6e9dc-138">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="6e9dc-139">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="6e9dc-140">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="6e9dc-141">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="6e9dc-142">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="6e9dc-143">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="6e9dc-144">Свойства</span><span class="sxs-lookup"><span data-stu-id="6e9dc-144">Properties</span></span>

<span data-ttu-id="6e9dc-145">Класс **Win32 \_ шорткутфиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e9dc-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-149">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-150">Битовая маска, представляющая права доступа, необходимые для доступа к файлу или выполнения конкретных операций над ним.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="6e9dc-151">Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="6e9dc-152">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="6e9dc-153">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6e9dc-154">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6e9dc-155">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6e9dc-156">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6e9dc-157">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6e9dc-158">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6e9dc-159">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6e9dc-160">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6e9dc-161">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6e9dc-162">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6e9dc-163">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6e9dc-164">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6e9dc-165">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6e9dc-166">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6e9dc-167">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e9dc-168">**Архив**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-169">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-171">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-172">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="6e9dc-173">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-174">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-177">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-178">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-178">A short textual description of the object.</span></span>

<span data-ttu-id="6e9dc-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-181">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-183">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-184">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="6e9dc-185">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-186">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-189">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-190">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6e9dc-191">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6e9dc-192">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6e9dc-193">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6e9dc-194">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-198">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-199">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-199">Name of the class.</span></span>

<span data-ttu-id="6e9dc-200">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-202">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-204">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-205">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="6e9dc-206">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-207">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-210">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-211">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-211">Class of the computer system.</span></span>

<span data-ttu-id="6e9dc-212">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-216">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-217">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-217">Name of the computer system.</span></span>

<span data-ttu-id="6e9dc-218">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-219">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-222">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-223">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-223">A textual description of the object.</span></span>

<span data-ttu-id="6e9dc-224">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-225">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-226">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-228">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("диск")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-229">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="6e9dc-230">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="6e9dc-230">Example: "c:"</span></span>

<span data-ttu-id="6e9dc-231">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-232">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-235">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-236">Имя файла в формате 8,3.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-236">File name in 8.3 format.</span></span>

<span data-ttu-id="6e9dc-237">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="6e9dc-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="6e9dc-238">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-239">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-240">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-242">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-243">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="6e9dc-244">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-248">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-249">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6e9dc-250">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6e9dc-251">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6e9dc-252">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="6e9dc-253">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-254">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-257">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-258">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="6e9dc-259">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="6e9dc-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="6e9dc-260">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-264">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-265">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-265">File name without the file name extension.</span></span>

<span data-ttu-id="6e9dc-266">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="6e9dc-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="6e9dc-267">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-268">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-271">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("размер"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-272">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="6e9dc-273">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6e9dc-274">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-278">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-279">Дескриптор, представляющий тип файла, указанный в свойстве **Extension** .</span><span class="sxs-lookup"><span data-stu-id="6e9dc-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="6e9dc-280">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-281">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-284">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-285">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-285">Class of the file system.</span></span>

<span data-ttu-id="6e9dc-286">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-287">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-290">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-291">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-291">Name of the file system.</span></span>

<span data-ttu-id="6e9dc-292">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-293">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-294">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-296">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-297">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="6e9dc-298">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-300">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-302">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-303">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-303">Indicates when the object was installed.</span></span> <span data-ttu-id="6e9dc-304">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6e9dc-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-306">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-307">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-309">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-310">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="6e9dc-311">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6e9dc-312">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-313">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-314">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-316">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-317">Дата и время последнего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="6e9dc-318">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-320">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-322">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-323">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="6e9dc-324">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-325">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-328">Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-329">Строка производителя из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="6e9dc-330">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-331">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-334">Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-335">Свойство Name — это строка, представляющая унаследованное имя, которое служит ключом экземпляра логического файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="6e9dc-336">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-336">Full path names should be provided.</span></span>

<span data-ttu-id="6e9dc-337">Пример: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="6e9dc-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="6e9dc-338">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-339">**Путь**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-342">Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("путь")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-343">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="6e9dc-344">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="6e9dc-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="6e9dc-345">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-346">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-347">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-349">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-350">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="6e9dc-351">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-352">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-355">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-356">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="6e9dc-357">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6e9dc-358">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6e9dc-359">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6e9dc-360">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="6e9dc-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6e9dc-361">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6e9dc-362">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6e9dc-363">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6e9dc-364">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6e9dc-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6e9dc-365">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6e9dc-366">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6e9dc-367">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6e9dc-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e9dc-368">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6e9dc-369">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6e9dc-370">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6e9dc-371">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6e9dc-372">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6e9dc-373">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6e9dc-374">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6e9dc-375">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6e9dc-376">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e9dc-377">**Система**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-378">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-380">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-381">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="6e9dc-382">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-383">**Целевой объект**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-384">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-386">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ бегинсреадекс")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-387">Имя объекта, которому является ярлык.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-388">**Version**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-389">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-391">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("версия")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-392">Строка версии из ресурса версии (если таковая имеется).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="6e9dc-393">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e9dc-394">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e9dc-395">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6e9dc-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e9dc-397">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="6e9dc-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="6e9dc-398">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="6e9dc-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="6e9dc-399">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e9dc-400">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e9dc-400">Remarks</span></span>

<span data-ttu-id="6e9dc-401">Класс **Win32 \_ шорткутфиле** является производным от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="6e9dc-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e9dc-402">Требования</span><span class="sxs-lookup"><span data-stu-id="6e9dc-402">Requirements</span></span>



| <span data-ttu-id="6e9dc-403">Требование</span><span class="sxs-lookup"><span data-stu-id="6e9dc-403">Requirement</span></span> | <span data-ttu-id="6e9dc-404">Значение</span><span class="sxs-lookup"><span data-stu-id="6e9dc-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9dc-405">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e9dc-405">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9dc-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e9dc-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e9dc-407">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e9dc-407">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9dc-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e9dc-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e9dc-409">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e9dc-409">Namespace</span></span><br/>                | <span data-ttu-id="6e9dc-410">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6e9dc-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e9dc-411">MOF</span><span class="sxs-lookup"><span data-stu-id="6e9dc-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e9dc-412"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e9dc-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e9dc-413">DLL</span><span class="sxs-lookup"><span data-stu-id="6e9dc-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e9dc-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e9dc-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9dc-415">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e9dc-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9dc-416">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="6e9dc-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="6e9dc-417">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="6e9dc-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
