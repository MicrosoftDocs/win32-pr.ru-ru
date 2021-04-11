---
description: Каталог Win32 \_&\# 32; Класс WMI представляет запись каталога в компьютерной системе под Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Класс Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262725"
---
# <a name="win32_directory-class"></a><span data-ttu-id="c1c37-103">\_Класс каталога Win32</span><span class="sxs-lookup"><span data-stu-id="c1c37-103">Win32\_Directory class</span></span>

<span data-ttu-id="c1c37-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ каталога Win32** представляет запись каталога в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="c1c37-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="c1c37-105">Каталог — это тип файла, который логически группирует файлы данных и предоставляет сведения о пути для сгруппированных файлов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="c1c37-106">Пример: C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="c1c37-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="c1c37-107">**Win32 \_ Каталог** не включает каталоги сетевых дисков.</span><span class="sxs-lookup"><span data-stu-id="c1c37-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="c1c37-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c1c37-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c1c37-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c1c37-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c37-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1c37-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="c1c37-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c1c37-111">Members</span></span>

<span data-ttu-id="c1c37-112">Класс **\_ каталога Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1c37-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="c1c37-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c1c37-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1c37-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1c37-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1c37-115">Методы</span><span class="sxs-lookup"><span data-stu-id="c1c37-115">Methods</span></span>

<span data-ttu-id="c1c37-116">Класс **\_ каталога Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="c1c37-117">Метод</span><span class="sxs-lookup"><span data-stu-id="c1c37-117">Method</span></span>                                                                                             | <span data-ttu-id="c1c37-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c1c37-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1c37-119">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="c1c37-120">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c1c37-121">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="c1c37-122">Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c1c37-123">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="c1c37-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="c1c37-124">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="c1c37-125">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="c1c37-126">Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="c1c37-127">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="c1c37-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="c1c37-128">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="c1c37-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c1c37-129">**копекс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="c1c37-130">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="c1c37-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c1c37-131">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="c1c37-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="c1c37-132">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="c1c37-133">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="c1c37-134">Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="c1c37-135">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="c1c37-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="c1c37-136">Метод класса, определяющий, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом *Permissions* , не только для объекта File, но и для общей папки, в которой находится файл или каталог (если он находится в общей папке).</span><span class="sxs-lookup"><span data-stu-id="c1c37-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="c1c37-137">**Имени**</span><span class="sxs-lookup"><span data-stu-id="c1c37-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="c1c37-138">Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="c1c37-139">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="c1c37-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="c1c37-140">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c1c37-141">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="c1c37-142">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c1c37-143">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="c1c37-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="c1c37-144">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="c1c37-145">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="c1c37-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="c1c37-146">Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c1c37-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="c1c37-147">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1c37-147">Properties</span></span>

<span data-ttu-id="c1c37-148">Класс **\_ каталога Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c1c37-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1c37-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="c1c37-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1c37-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-152">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="c1c37-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-153">Битовая маска, представляющая права доступа, необходимые для доступа к каталогу или выполнения конкретных операций с ним.</span><span class="sxs-lookup"><span data-stu-id="c1c37-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="c1c37-154">Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="c1c37-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="c1c37-155">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="c1c37-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="c1c37-156">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c1c37-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="c1c37-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-158">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="c1c37-159">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="c1c37-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="c1c37-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="c1c37-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-161">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="c1c37-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="c1c37-162">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c1c37-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="c1c37-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог** (4)</span><span class="sxs-lookup"><span data-stu-id="c1c37-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-164">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="c1c37-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="c1c37-165">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="c1c37-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="c1c37-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="c1c37-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-167">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="c1c37-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="c1c37-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-169">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="c1c37-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="c1c37-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-171">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-171">Grants the right to execute a file.</span></span> <span data-ttu-id="c1c37-172">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="c1c37-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="c1c37-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="c1c37-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-174">Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c1c37-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="c1c37-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="c1c37-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-176">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="c1c37-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="c1c37-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-178">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="c1c37-179"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="c1c37-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-180">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="c1c37-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="c1c37-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="c1c37-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-182">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="c1c37-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="c1c37-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="c1c37-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-184">Предоставляет доступ на запись к избирательному списку управления доступом.</span><span class="sxs-lookup"><span data-stu-id="c1c37-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="c1c37-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="c1c37-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-186">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="c1c37-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="c1c37-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="c1c37-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-188">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="c1c37-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="c1c37-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Доступ к \_ \_Безопасность системы** (18809343)</span><span class="sxs-lookup"><span data-stu-id="c1c37-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="c1c37-190">Управляет возможностью получения или задания списка SACL в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c1c37-191">**Архив**</span><span class="sxs-lookup"><span data-stu-id="c1c37-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-192">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-194">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="c1c37-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-195">Указывает, задан ли бит архива для папки.</span><span class="sxs-lookup"><span data-stu-id="c1c37-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="c1c37-196">Бит архива используется программами резервного копирования для обнаружения файлов, для которых необходимо создать резервную копию.</span><span class="sxs-lookup"><span data-stu-id="c1c37-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="c1c37-197">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="c1c37-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="c1c37-198">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-199">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c1c37-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-202">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c1c37-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-203">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-203">A short textual description of the object.</span></span>

<span data-ttu-id="c1c37-204">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="c1c37-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-206">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-208">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="c1c37-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-209">Указывает, сжата ли папка.</span><span class="sxs-lookup"><span data-stu-id="c1c37-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="c1c37-210">Инструментарий WMI распознает папки, сжатые с помощью самого инструментария WMI или графического пользовательского интерфейса. Однако он не распознается. ZIP-файлы как сжатые.</span><span class="sxs-lookup"><span data-stu-id="c1c37-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="c1c37-211">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="c1c37-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="c1c37-212">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-213">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="c1c37-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-216">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="c1c37-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-217">Алгоритм или средство (обычно метод), используемые для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="c1c37-218">Если невозможно (или не требуется) описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, сжат ли логический файл. "Сжатый" для представления того, что файл сжат, но либо его схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что логический файл не сжат.</span><span class="sxs-lookup"><span data-stu-id="c1c37-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="c1c37-219">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c1c37-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-223">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="c1c37-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-224">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c1c37-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c1c37-225">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c1c37-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c1c37-226">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="c1c37-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-228">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1c37-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-230">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="c1c37-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-231">Дата создания объекта файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-231">Date that the file system object was created.</span></span> <span data-ttu-id="c1c37-232">Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="c1c37-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="c1c37-233">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-234">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c1c37-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-237">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-238">Имя класса создания для системы компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="c1c37-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="c1c37-239">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c1c37-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-243">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-244">Имя компьютера, на котором хранится объект файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="c1c37-245">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-246">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1c37-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-249">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c1c37-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-250">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-250">A textual description of the object.</span></span>

<span data-ttu-id="c1c37-251">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-252">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="c1c37-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-255">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="c1c37-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-256">Буква диска (включая двоеточие), где хранится объект файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="c1c37-257">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="c1c37-257">Example: "c:"</span></span>

<span data-ttu-id="c1c37-258">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-259">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="c1c37-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-262">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="c1c37-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-263">Имя папки, совместимое с MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="c1c37-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="c1c37-264">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="c1c37-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="c1c37-265">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-266">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="c1c37-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-267">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-269">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="c1c37-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-270">Указывает, была ли зашифрована папка.</span><span class="sxs-lookup"><span data-stu-id="c1c37-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="c1c37-271">**Значение true**, если папка зашифрована.</span><span class="sxs-lookup"><span data-stu-id="c1c37-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="c1c37-272">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="c1c37-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-276">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="c1c37-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-277">Алгоритм или инструмент, используемый для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="c1c37-278">Если вы не можете (или не хотите) описать схему шифрования (возможно, по соображениям безопасности), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, зашифрован ли логический файл. "Encrypted" для представления того, что файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается. и «not encrypted» для представления того, что логический файл не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="c1c37-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="c1c37-279">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-280">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="c1c37-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-283">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="c1c37-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-284">Расширение имени файла для объекта файловой системы, не включая точку (.), которая отделяет расширение от имени файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="c1c37-285">Примеры: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="c1c37-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="c1c37-286">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c1c37-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-290">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="c1c37-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-291">Имя файла (без точки или расширения) файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="c1c37-292">Пример: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="c1c37-292">Example: "autoexec"</span></span>

<span data-ttu-id="c1c37-293">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-294">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="c1c37-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-295">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c1c37-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-297">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="c1c37-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-298">Размер объекта файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="c1c37-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="c1c37-299">Хотя папки обладают свойством **Размер файла** , всегда возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="c1c37-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="c1c37-300">Чтобы определить размер папки, используйте FileSystemObject или добавьте размер всех файлов, хранящихся в папке.</span><span class="sxs-lookup"><span data-stu-id="c1c37-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="c1c37-301">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c1c37-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c1c37-302">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="c1c37-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-306">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="c1c37-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-307">Тип файла (указывается свойством **расширения** ).</span><span class="sxs-lookup"><span data-stu-id="c1c37-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="c1c37-308">Например, файл. mdb, скорее всего, будет иметь тип файла приложение Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c1c37-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="c1c37-309">Файл. ASP, вероятно, имеет файл HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="c1c37-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="c1c37-310">Папки обычно выводятся просто как папка.</span><span class="sxs-lookup"><span data-stu-id="c1c37-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="c1c37-311">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-312">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c1c37-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-315">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-316">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-316">Class of the file system.</span></span>

<span data-ttu-id="c1c37-317">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-318">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="c1c37-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-321">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-322">Тип файловой системы (NTFS, FAT, FAT32), установленной на диске, где находится файл или папка.</span><span class="sxs-lookup"><span data-stu-id="c1c37-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="c1c37-323">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-324">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="c1c37-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-325">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-327">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="c1c37-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-328">Указывает, скрыт ли объект файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="c1c37-329">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="c1c37-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="c1c37-330">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c1c37-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-332">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1c37-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-334">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-335">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c1c37-335">Indicates when the object was installed.</span></span> <span data-ttu-id="c1c37-336">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c1c37-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c1c37-337">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-338">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="c1c37-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-339">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c1c37-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-341">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="c1c37-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-342">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="c1c37-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="c1c37-343">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c1c37-344">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c1c37-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-345">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="c1c37-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-346">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1c37-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-348">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="c1c37-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-349">Дата последнего обращения к файлу.</span><span class="sxs-lookup"><span data-stu-id="c1c37-349">Date the file was last accessed.</span></span> <span data-ttu-id="c1c37-350">Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="c1c37-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="c1c37-351">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="c1c37-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-353">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1c37-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-355">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="c1c37-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-356">Дата последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="c1c37-356">Date the file was last modified.</span></span> <span data-ttu-id="c1c37-357">Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="c1c37-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="c1c37-358">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-359">**Name**</span><span class="sxs-lookup"><span data-stu-id="c1c37-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-362">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1c37-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-363">Свойство Name — это строка, представляющая унаследованное имя, которое служит ключом экземпляра логического файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="c1c37-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="c1c37-364">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="c1c37-364">Full path names should be provided.</span></span> <span data-ttu-id="c1c37-365">Пример: C: \\ Windows \\ System \\win.ini</span><span class="sxs-lookup"><span data-stu-id="c1c37-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="c1c37-366">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-367">**Путь**</span><span class="sxs-lookup"><span data-stu-id="c1c37-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-370">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="c1c37-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-371">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c1c37-371">Path for the file.</span></span> <span data-ttu-id="c1c37-372">Путь включает в себя начальную и конечную обратную косую черту, но не букву диска или имя папки.</span><span class="sxs-lookup"><span data-stu-id="c1c37-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="c1c37-373">Для папки c: \\ Windows \\ system32 \\ WBEM путь — \\ Windows \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="c1c37-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="c1c37-374">Для папки c: \\ используется путь \\ .</span><span class="sxs-lookup"><span data-stu-id="c1c37-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="c1c37-375">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-376">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="c1c37-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-377">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-379">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="c1c37-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-380">Указывает, можно ли читать элементы в папке.</span><span class="sxs-lookup"><span data-stu-id="c1c37-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="c1c37-381">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="c1c37-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="c1c37-382">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-383">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c1c37-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-384">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1c37-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-386">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c1c37-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-387">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c1c37-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="c1c37-388">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c1c37-389">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c1c37-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c1c37-390">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c1c37-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c1c37-391">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c1c37-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c1c37-392">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c1c37-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c1c37-393">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c1c37-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c1c37-394">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c1c37-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c1c37-395">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c1c37-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c1c37-396">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c1c37-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c1c37-397">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c1c37-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c1c37-398">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c1c37-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c1c37-399">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c1c37-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c1c37-400">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c1c37-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c1c37-401">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c1c37-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c1c37-402">**Система**</span><span class="sxs-lookup"><span data-stu-id="c1c37-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-403">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-405">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="c1c37-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-406">Указывает, является ли объект системным файлом.</span><span class="sxs-lookup"><span data-stu-id="c1c37-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="c1c37-407">**Значение true**, если файл является системным файлом</span><span class="sxs-lookup"><span data-stu-id="c1c37-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="c1c37-408">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1c37-409">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="c1c37-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1c37-410">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c1c37-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1c37-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1c37-412">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="c1c37-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="c1c37-413">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="c1c37-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="c1c37-414">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1c37-415">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1c37-415">Remarks</span></span>

<span data-ttu-id="c1c37-416">Класс **\_ каталога Win32** является производным от [**\_ каталога CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="c1c37-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="c1c37-417">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="c1c37-417">**Overview**</span></span>

<span data-ttu-id="c1c37-418">Папки — это объекты файловой системы, предназначенные для хранения других объектов файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c1c37-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="c1c37-419">Однако это не означает, что все папки являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="c1c37-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="c1c37-420">Вместо этого они могут значительно варьироваться.</span><span class="sxs-lookup"><span data-stu-id="c1c37-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="c1c37-421">Некоторые папки являются папками операционной системы, которые, как правило, не должны изменяться сценарием.</span><span class="sxs-lookup"><span data-stu-id="c1c37-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="c1c37-422">Некоторые папки доступны только для чтения. Это означает, что пользователи могут получать доступ к содержимому этой папки, но не могут добавлять, удалять или изменять эти содержимое.</span><span class="sxs-lookup"><span data-stu-id="c1c37-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="c1c37-423">Некоторые папки сжимаются для оптимального хранилища, другие — как скрытые и невидимые для пользователей.</span><span class="sxs-lookup"><span data-stu-id="c1c37-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="c1c37-424">Инструментарий WMI использует класс **\_ каталога Win32** для управления папками.</span><span class="sxs-lookup"><span data-stu-id="c1c37-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="c1c37-425">В значительной степени свойства и методы, доступные в этом классе, идентичны свойствам и методам, доступным в классе [**\_ файлов CIM**](cim-datafile.md) , класс, используемый для управления файлами.</span><span class="sxs-lookup"><span data-stu-id="c1c37-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="c1c37-426">Это означает, что после того, как вы узнали, как управлять папками с помощью инструментария WMI, вы, без дополнительной работы, также узнаете, как управлять файлами.</span><span class="sxs-lookup"><span data-stu-id="c1c37-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="c1c37-427">Класс [**сопоставления \_ подкаталога Win32**](win32-subdirectory.md) также используется для управления файлами и папками.</span><span class="sxs-lookup"><span data-stu-id="c1c37-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="c1c37-428">Класс **\_ подкаталога Win32** связывает папку и ее непосредственные вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="c1c37-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="c1c37-429">Например, в структуре папок C: \\ \\ журналы скриптов, журналы — это вложенная папка сценариев, а сценарии — это вложенная папка корневой папки C: \\ .</span><span class="sxs-lookup"><span data-stu-id="c1c37-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="c1c37-430">Однако журналы не считаются вложенными папками C: \\ .</span><span class="sxs-lookup"><span data-stu-id="c1c37-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="c1c37-431">Свойства любой папки в файловой системе можно получить с помощью класса **\_ каталога Win32** .</span><span class="sxs-lookup"><span data-stu-id="c1c37-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="c1c37-432">Свойства, доступные с помощью этого класса, показаны в таблице 11,1.</span><span class="sxs-lookup"><span data-stu-id="c1c37-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="c1c37-433">Чтобы получить свойства для отдельной папки, создайте запрос на языке запросов Windows (WQL) для класса **\_ каталога Win32** , убедившись, что вы включили имя папки.</span><span class="sxs-lookup"><span data-stu-id="c1c37-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="c1c37-434">Например, этот запрос привязывается к папке D: \\ Archive:</span><span class="sxs-lookup"><span data-stu-id="c1c37-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="c1c37-435">При указании имени файла или папки в WQL-запросе убедитесь, что \\ для разделения компонентов пути используется две обратные косые черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="c1c37-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="c1c37-436">Если требуется ограничить извлечение данных на один диск, включите предложение WHERE, указывающее букву диска.</span><span class="sxs-lookup"><span data-stu-id="c1c37-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="c1c37-437">Например, этот запрос возвращает список всех папок на диске C:</span><span class="sxs-lookup"><span data-stu-id="c1c37-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="c1c37-438">Если необходимо перечислить все папки на компьютере, учтите, что выполнение этого запроса может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="c1c37-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="c1c37-439">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1c37-439">Examples</span></span>

<span data-ttu-id="c1c37-440">Следующий пример сценария VBScript извлекает свойства папки C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="c1c37-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="c1c37-441">Следующий пример сценария VBScript возвращает список всех скрытых папок на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c1c37-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="c1c37-442">Требования</span><span class="sxs-lookup"><span data-stu-id="c1c37-442">Requirements</span></span>



| <span data-ttu-id="c1c37-443">Требование</span><span class="sxs-lookup"><span data-stu-id="c1c37-443">Requirement</span></span> | <span data-ttu-id="c1c37-444">Значение</span><span class="sxs-lookup"><span data-stu-id="c1c37-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c37-445">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1c37-445">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c37-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1c37-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1c37-447">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1c37-447">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c37-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1c37-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1c37-449">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1c37-449">Namespace</span></span><br/>                | <span data-ttu-id="c1c37-450">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c1c37-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1c37-451">MOF</span><span class="sxs-lookup"><span data-stu-id="c1c37-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1c37-452"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1c37-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1c37-453">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c37-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c37-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c37-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c37-455">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1c37-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c37-456">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="c1c37-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="c1c37-457">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1c37-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

