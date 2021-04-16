---
description: '\_Класс каталога CIM представляет тип файла, который логически группирует содержащиеся в нем файлы данных и предоставляет сведения о пути для сгруппированных файлов.'
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: Класс CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655965"
---
# <a name="cim_directory-class"></a><span data-ttu-id="c38ef-103">\_Класс каталога CIM</span><span class="sxs-lookup"><span data-stu-id="c38ef-103">CIM\_Directory class</span></span>

<span data-ttu-id="c38ef-104">Класс **\_ каталога CIM** представляет тип файла, который логически группирует содержащиеся в нем файлы данных и предоставляет сведения о пути для сгруппированных файлов.</span><span class="sxs-lookup"><span data-stu-id="c38ef-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c38ef-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c38ef-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c38ef-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c38ef-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c38ef-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c38ef-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c38ef-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38ef-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c38ef-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="c38ef-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c38ef-110">Members</span></span>

<span data-ttu-id="c38ef-111">Класс **\_ каталога CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c38ef-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="c38ef-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c38ef-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c38ef-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c38ef-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c38ef-114">Методы</span><span class="sxs-lookup"><span data-stu-id="c38ef-114">Methods</span></span>

<span data-ttu-id="c38ef-115">Класс **\_ каталога CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c38ef-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="c38ef-116">Метод</span><span class="sxs-lookup"><span data-stu-id="c38ef-116">Method</span></span>                                                                                           | <span data-ttu-id="c38ef-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c38ef-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c38ef-118">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="c38ef-119">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c38ef-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c38ef-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c38ef-121">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="c38ef-122">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="c38ef-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="c38ef-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="c38ef-124">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="c38ef-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="c38ef-125">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c38ef-127">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="c38ef-128">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-129">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="c38ef-130">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="c38ef-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="c38ef-131">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="c38ef-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c38ef-132">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c38ef-133">**копекс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="c38ef-134">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="c38ef-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="c38ef-135">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="c38ef-136">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="c38ef-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="c38ef-137">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-138">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c38ef-139">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="c38ef-140">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-141">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c38ef-142">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="c38ef-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="c38ef-143">Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="c38ef-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="c38ef-144">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="c38ef-145">**Имени**</span><span class="sxs-lookup"><span data-stu-id="c38ef-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="c38ef-146">Переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-147">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="c38ef-148">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="c38ef-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="c38ef-149">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c38ef-150">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="c38ef-151">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="c38ef-152">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c38ef-153">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="c38ef-154">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="c38ef-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="c38ef-155">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-156">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="c38ef-157">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="c38ef-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="c38ef-158">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="c38ef-159">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c38ef-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="c38ef-160">Свойства</span><span class="sxs-lookup"><span data-stu-id="c38ef-160">Properties</span></span>

<span data-ttu-id="c38ef-161">Класс **\_ каталога CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c38ef-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c38ef-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="c38ef-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c38ef-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-165">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="c38ef-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-166">Битовая маска, представляющая права доступа, необходимые для доступа к каталогу или выполнения конкретных операций с ним.</span><span class="sxs-lookup"><span data-stu-id="c38ef-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="c38ef-167">Значения см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="c38ef-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="c38ef-168">На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="c38ef-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="c38ef-169">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c38ef-170">**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="c38ef-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="c38ef-171">**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="c38ef-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="c38ef-172">**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="c38ef-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="c38ef-173">**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="c38ef-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="c38ef-174">**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="c38ef-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="c38ef-175">**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="c38ef-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="c38ef-176">**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="c38ef-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="c38ef-177">**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="c38ef-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="c38ef-178">**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="c38ef-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="c38ef-179">**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="c38ef-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="c38ef-180">**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="c38ef-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="c38ef-181">**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="c38ef-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="c38ef-182">**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="c38ef-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="c38ef-183">**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="c38ef-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c38ef-184">**Архив**</span><span class="sxs-lookup"><span data-stu-id="c38ef-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-185">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-187">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="c38ef-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-188">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="c38ef-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="c38ef-189">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-190">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c38ef-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-193">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c38ef-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-194">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-194">Short textual description of the object.</span></span>

<span data-ttu-id="c38ef-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="c38ef-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-197">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-199">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="c38ef-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-200">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="c38ef-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="c38ef-201">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-202">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="c38ef-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-205">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="c38ef-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-206">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="c38ef-207">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="c38ef-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="c38ef-208">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="c38ef-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="c38ef-209">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="c38ef-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="c38ef-210">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c38ef-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-214">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="c38ef-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-215">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="c38ef-215">Name of the class.</span></span>

<span data-ttu-id="c38ef-216">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="c38ef-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-218">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c38ef-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-220">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="c38ef-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-221">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-221">Date and time that the file was created.</span></span>

<span data-ttu-id="c38ef-222">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-223">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c38ef-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-226">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-227">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="c38ef-227">Class of the computer system.</span></span>

<span data-ttu-id="c38ef-228">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c38ef-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-232">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-233">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="c38ef-233">Name of the computer system.</span></span>

<span data-ttu-id="c38ef-234">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-235">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c38ef-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-238">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c38ef-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-239">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-239">Textual description of the object.</span></span>

<span data-ttu-id="c38ef-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-241">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="c38ef-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-244">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="c38ef-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-245">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="c38ef-246">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-247">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="c38ef-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-248">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="c38ef-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-251">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="c38ef-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-252">Имя файла, совместимое с DOS.</span><span class="sxs-lookup"><span data-stu-id="c38ef-252">DOS-compatible file name.</span></span> <span data-ttu-id="c38ef-253">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-254">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="c38ef-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-255">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="c38ef-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-256">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-258">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="c38ef-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-259">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="c38ef-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="c38ef-260">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="c38ef-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-264">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="c38ef-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-265">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="c38ef-266">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="c38ef-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="c38ef-267">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="c38ef-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="c38ef-268">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="c38ef-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="c38ef-269">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-270">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="c38ef-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-273">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="c38ef-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-274">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="c38ef-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="c38ef-275">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-276">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="c38ef-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="c38ef-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-280">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="c38ef-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-281">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-281">File name without the file name extension.</span></span>

<span data-ttu-id="c38ef-282">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-283">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="c38ef-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-284">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="c38ef-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-285">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c38ef-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-287">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="c38ef-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-288">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="c38ef-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="c38ef-289">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-290">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c38ef-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="c38ef-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-294">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="c38ef-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-295">Дескриптор, представляющий тип файла (указывается свойством **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="c38ef-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="c38ef-296">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-297">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c38ef-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-300">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-301">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c38ef-301">Class of the file system.</span></span>

<span data-ttu-id="c38ef-302">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-303">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="c38ef-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-306">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-307">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="c38ef-307">Name of the file system.</span></span>

<span data-ttu-id="c38ef-308">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-309">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="c38ef-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-310">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-312">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="c38ef-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-313">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="c38ef-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="c38ef-314">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c38ef-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-316">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c38ef-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-318">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-319">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-319">Date and time when the object was installed.</span></span> <span data-ttu-id="c38ef-320">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="c38ef-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c38ef-321">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-322">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="c38ef-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-323">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c38ef-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-325">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="c38ef-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-326">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="c38ef-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="c38ef-327">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-328">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c38ef-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-329">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="c38ef-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-330">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c38ef-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-332">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="c38ef-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-333">Дата и время последнего обращения к файлу.</span><span class="sxs-lookup"><span data-stu-id="c38ef-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="c38ef-334">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="c38ef-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-336">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c38ef-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-338">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="c38ef-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-339">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="c38ef-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="c38ef-340">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-341">**Name**</span><span class="sxs-lookup"><span data-stu-id="c38ef-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-344">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c38ef-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-345">Унаследованное имя, служащее ключом экземпляра логического файла в файловой системе (укажите полные имена путей).</span><span class="sxs-lookup"><span data-stu-id="c38ef-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="c38ef-346">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c38ef-347">Пример: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="c38ef-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-348">**Путь**</span><span class="sxs-lookup"><span data-stu-id="c38ef-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-351">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="c38ef-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-352">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="c38ef-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="c38ef-353">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-354">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="c38ef-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-355">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="c38ef-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-356">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-358">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="c38ef-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-359">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="c38ef-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="c38ef-360">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-361">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c38ef-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c38ef-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-364">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c38ef-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-365">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c38ef-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="c38ef-366">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c38ef-367">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c38ef-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c38ef-368">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c38ef-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c38ef-369">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c38ef-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c38ef-370">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c38ef-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c38ef-371">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c38ef-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c38ef-372">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c38ef-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c38ef-373">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c38ef-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c38ef-374">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c38ef-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c38ef-375">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c38ef-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c38ef-376">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c38ef-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c38ef-377">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c38ef-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c38ef-378">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c38ef-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c38ef-379">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c38ef-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c38ef-380">**Система**</span><span class="sxs-lookup"><span data-stu-id="c38ef-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-381">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-383">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="c38ef-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-384">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="c38ef-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="c38ef-385">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ef-386">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="c38ef-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38ef-387">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c38ef-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c38ef-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38ef-389">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="c38ef-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="c38ef-390">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="c38ef-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="c38ef-391">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c38ef-392">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c38ef-392">Remarks</span></span>

<span data-ttu-id="c38ef-393">Класс **\_ каталога CIM** является производным от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="c38ef-394">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c38ef-394">WMI does not implement this class.</span></span> <span data-ttu-id="c38ef-395">Дополнительные сведения о классах, производных от **\_ каталога CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c38ef-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c38ef-396">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c38ef-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c38ef-397">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c38ef-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38ef-398">Требования</span><span class="sxs-lookup"><span data-stu-id="c38ef-398">Requirements</span></span>



| <span data-ttu-id="c38ef-399">Требование</span><span class="sxs-lookup"><span data-stu-id="c38ef-399">Requirement</span></span> | <span data-ttu-id="c38ef-400">Значение</span><span class="sxs-lookup"><span data-stu-id="c38ef-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c38ef-401">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c38ef-401">Minimum supported client</span></span><br/> | <span data-ttu-id="c38ef-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c38ef-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c38ef-403">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c38ef-403">Minimum supported server</span></span><br/> | <span data-ttu-id="c38ef-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c38ef-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c38ef-405">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c38ef-405">Namespace</span></span><br/>                | <span data-ttu-id="c38ef-406">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c38ef-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c38ef-407">MOF</span><span class="sxs-lookup"><span data-stu-id="c38ef-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c38ef-408"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c38ef-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c38ef-409">DLL</span><span class="sxs-lookup"><span data-stu-id="c38ef-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c38ef-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c38ef-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38ef-411">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c38ef-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38ef-412">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c38ef-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

