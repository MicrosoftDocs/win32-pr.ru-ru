---
description: '&Win32 \_ кодекфиле \# 32; Класс WMI представляет аудио или видеокодек, установленный в компьютерной системе.'
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Класс Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142301"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="a2dc6-103">\_Класс Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="a2dc6-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="a2dc6-104">Класс **WMI \_ кодекфиле** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет аудио или видеокодек, установленный в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="a2dc6-105">Кодеки преобразуют один тип формата мультимедиа в другой, обычно это сжатый формат в несжатый формат.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="a2dc6-106">Имя «кодек» является производным от сочетания сжатия и распаковки.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="a2dc6-107">Например, кодек может преобразовать сжатый формат, например MS-ADPCM, в несжатый формат, например PCM, который может играться в большинстве звуков.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="a2dc6-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a2dc6-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2dc6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2dc6-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="a2dc6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a2dc6-111">Members</span></span>

<span data-ttu-id="a2dc6-112">Класс **Win32 \_ кодекфиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="a2dc6-113">Методы</span><span class="sxs-lookup"><span data-stu-id="a2dc6-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a2dc6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2dc6-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a2dc6-115">Методы</span><span class="sxs-lookup"><span data-stu-id="a2dc6-115">Methods</span></span>

<span data-ttu-id="a2dc6-116">Класс **Win32 \_ кодекфиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="a2dc6-117">Метод</span><span class="sxs-lookup"><span data-stu-id="a2dc6-117">Method</span></span>                                                                                             | <span data-ttu-id="a2dc6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a2dc6-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2dc6-119">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="a2dc6-120">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="a2dc6-121">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="a2dc6-122">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="a2dc6-123">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="a2dc6-124">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a2dc6-125">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="a2dc6-126">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a2dc6-127">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="a2dc6-128">Копирует логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="a2dc6-129">**копекс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="a2dc6-130">Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром FileName.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="a2dc6-131">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="a2dc6-132">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="a2dc6-133">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="a2dc6-134">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="a2dc6-135">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="a2dc6-136">Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** , не только для объекта File, но и для общего ресурса, в котором находится файл или каталог (если он находится в общей папке).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="a2dc6-137">**Имени**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="a2dc6-138">Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="a2dc6-139">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="a2dc6-140">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="a2dc6-141">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="a2dc6-142">Метод класса, который получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a2dc6-143">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="a2dc6-144">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a2dc6-145">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="a2dc6-146">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="a2dc6-147">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2dc6-147">Properties</span></span>

<span data-ttu-id="a2dc6-148">Класс **Win32 \_ кодекфиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2dc6-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-152">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-153">Битовая маска, представляющая права доступа, необходимые для доступа или выполнения конкретных операций с файлом кодека.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="a2dc6-154">Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="a2dc6-155">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="a2dc6-156">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a2dc6-157">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="a2dc6-158">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a2dc6-159">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="a2dc6-160">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="a2dc6-161">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="a2dc6-162">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="a2dc6-163">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="a2dc6-164">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="a2dc6-165">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="a2dc6-166">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="a2dc6-167">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="a2dc6-168">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="a2dc6-169">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="a2dc6-170">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2dc6-171">**Архив**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-174">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-175">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="a2dc6-176">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-177">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-180">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-181">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-181">Short description of the object.</span></span>

<span data-ttu-id="a2dc6-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-186">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-187">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="a2dc6-188">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-189">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-192">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-193">Алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a2dc6-194">Если невозможно (или не требуется) описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, сжат ли логический файл. "Сжатый" для представления того, что файл сжат, но либо его схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что логический файл не сжат.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="a2dc6-195">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-199">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-200">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a2dc6-201">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a2dc6-202">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-204">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-206">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-207">Дата создания файла.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-207">File creation date.</span></span>

<span data-ttu-id="a2dc6-208">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-209">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-212">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-213">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-213">Class of the computer system.</span></span>

<span data-ttu-id="a2dc6-214">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-218">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-219">Строка, представляющая имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="a2dc6-220">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-221">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-224">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (описание), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ медиаресаурцес \\ \\ ICM \| Description")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-225">Полное имя драйвера кодека.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-225">Full name of the codec driver.</span></span> <span data-ttu-id="a2dc6-226">Эта строка должна отображаться в виде длинных (описательных) пробелов.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="a2dc6-227">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a2dc6-228">Пример: "Microsoft PCM Converter"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-229">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-232">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-233">Буква диска (включая двоеточие) файла.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="a2dc6-234">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-235">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-236">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-239">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-240">Совместимое с DOS имя файла для этого файла.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="a2dc6-241">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-242">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-243">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-244">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-246">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-247">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="a2dc6-248">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-252">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-253">Алгоритм или инструмент, используемый для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="a2dc6-254">Если вы не можете (или не хотите) описать схему шифрования (возможно, по соображениям безопасности), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, зашифрован ли логический файл. "Encrypted" для представления того, что файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается. и «not encrypted» для представления того, что логический файл не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="a2dc6-255">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-256">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-259">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-260">Расширение имени файла (без точки).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-260">File name extension (without the dot).</span></span>

<span data-ttu-id="a2dc6-261">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-262">Примеры: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-266">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-267">Имя файла (без расширения).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="a2dc6-268">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-269">Пример: "Autoexec"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-270">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-271">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-273">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-274">Размер файла (в байтах).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="a2dc6-275">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-276">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-280">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-281">Тип файла (указывается свойством **расширения** ).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="a2dc6-282">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-283">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-286">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-287">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-287">Class of the file system.</span></span>

<span data-ttu-id="a2dc6-288">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-289">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-292">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-293">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-293">Name of the file system.</span></span>

<span data-ttu-id="a2dc6-294">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-295">**Группа**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-298">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Drivers. desc")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-299">Кодек, представленный этим классом.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-299">Codec represented by this class.</span></span>

<span data-ttu-id="a2dc6-300">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="a2dc6-301">Аудиосигнал</span><span class="sxs-lookup"><span data-stu-id="a2dc6-301">"Audio"</span></span></dd> <dd><span data-ttu-id="a2dc6-302">Роли</span><span class="sxs-lookup"><span data-stu-id="a2dc6-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="a2dc6-303">**Звук** ("аудио")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="a2dc6-304">**Видео** ("видео")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2dc6-305">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-306">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-308">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-309">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="a2dc6-310">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-312">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-314">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-315">Объект был установлен.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-315">Object was installed.</span></span> <span data-ttu-id="a2dc6-316">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a2dc6-317">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-318">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-319">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-321">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-322">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="a2dc6-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="a2dc6-323">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-324">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-325">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-326">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-328">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-329">Последний доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-329">File was last accessed.</span></span>

<span data-ttu-id="a2dc6-330">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-332">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-334">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-335">Файл был изменен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-335">File was last modified.</span></span>

<span data-ttu-id="a2dc6-336">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-337">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-340">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-341">Строка производителя из ресурса версии, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="a2dc6-342">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-343">**Name**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-346">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-347">Унаследованное имя, служащее ключом экземпляра логического файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="a2dc6-348">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-348">Full path names should be provided.</span></span>

<span data-ttu-id="a2dc6-349">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a2dc6-350">Пример: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="a2dc6-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-351">**Путь**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-354">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-355">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-355">Path of the file.</span></span> <span data-ttu-id="a2dc6-356">Сюда входят начальные и конечные обратные косые черты.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="a2dc6-357">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="a2dc6-358">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="a2dc6-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-359">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-360">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-362">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-363">Файл может быть прочитан.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-363">File can be read.</span></span>

<span data-ttu-id="a2dc6-364">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-365">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-368">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-369">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-369">Current status of the object.</span></span> <span data-ttu-id="a2dc6-370">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a2dc6-371">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a2dc6-372">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="a2dc6-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a2dc6-373">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a2dc6-374">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a2dc6-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a2dc6-376">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a2dc6-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a2dc6-377">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a2dc6-378">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a2dc6-379">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a2dc6-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2dc6-380">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a2dc6-381">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a2dc6-382">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a2dc6-383">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a2dc6-384">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a2dc6-385">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a2dc6-386">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a2dc6-387">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a2dc6-388">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2dc6-389">**Система**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-390">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-392">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-393">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="a2dc6-394">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-398">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-399">Строка версии из ресурса версии, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="a2dc6-400">Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2dc6-401">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2dc6-402">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2dc6-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2dc6-404">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="a2dc6-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="a2dc6-405">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="a2dc6-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="a2dc6-406">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2dc6-407">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2dc6-407">Remarks</span></span>

<span data-ttu-id="a2dc6-408">Класс **Win32 \_ кодекфиле** является производным от [**CIM- \_ файла**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="a2dc6-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2dc6-409">Требования</span><span class="sxs-lookup"><span data-stu-id="a2dc6-409">Requirements</span></span>



| <span data-ttu-id="a2dc6-410">Требование</span><span class="sxs-lookup"><span data-stu-id="a2dc6-410">Requirement</span></span> | <span data-ttu-id="a2dc6-411">Значение</span><span class="sxs-lookup"><span data-stu-id="a2dc6-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2dc6-412">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2dc6-412">Minimum supported client</span></span><br/> | <span data-ttu-id="a2dc6-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2dc6-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2dc6-414">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2dc6-414">Minimum supported server</span></span><br/> | <span data-ttu-id="a2dc6-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2dc6-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2dc6-416">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2dc6-416">Namespace</span></span><br/>                | <span data-ttu-id="a2dc6-417">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2dc6-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2dc6-418">MOF</span><span class="sxs-lookup"><span data-stu-id="a2dc6-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2dc6-419"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc6-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2dc6-420">DLL</span><span class="sxs-lookup"><span data-stu-id="a2dc6-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2dc6-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2dc6-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2dc6-422">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2dc6-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2dc6-423">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="a2dc6-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="a2dc6-424">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2dc6-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

