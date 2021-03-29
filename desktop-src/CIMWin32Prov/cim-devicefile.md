---
description: Класс CIM \_ девицефиле представляет тип логического файла, который представляет устройство.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: Класс CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990665"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="65228-103">\_Класс CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="65228-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="65228-104">Класс **CIM \_ девицефиле** представляет тип логического файла, который представляет устройство.</span><span class="sxs-lookup"><span data-stu-id="65228-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="65228-105">Это соглашение полезно для операционных систем, управляющих устройствами с помощью потоковой модели ввода-вывода в байтах.</span><span class="sxs-lookup"><span data-stu-id="65228-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="65228-106">Логическое устройство, связанное с этим файлом, указывается с помощью отношения [**CIM \_ девицеакцесседбифиле**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="65228-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65228-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65228-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65228-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65228-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="65228-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="65228-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="65228-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65228-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65228-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="65228-112">Члены</span><span class="sxs-lookup"><span data-stu-id="65228-112">Members</span></span>

<span data-ttu-id="65228-113">Класс **CIM \_ девицефиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65228-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="65228-114">Методы</span><span class="sxs-lookup"><span data-stu-id="65228-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="65228-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="65228-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65228-116">Методы</span><span class="sxs-lookup"><span data-stu-id="65228-116">Methods</span></span>

<span data-ttu-id="65228-117">Класс **CIM \_ девицефиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="65228-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="65228-118">Метод</span><span class="sxs-lookup"><span data-stu-id="65228-118">Method</span></span>                                                                                            | <span data-ttu-id="65228-119">Описание</span><span class="sxs-lookup"><span data-stu-id="65228-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65228-120">**чанжесекуритипермиссионс**</span><span class="sxs-lookup"><span data-stu-id="65228-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="65228-121">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="65228-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="65228-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="65228-123">**чанжесекуритипермиссионсекс**</span><span class="sxs-lookup"><span data-stu-id="65228-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="65228-124">Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="65228-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="65228-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="65228-126">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="65228-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="65228-127">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-128">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="65228-129">**компрессекс**</span><span class="sxs-lookup"><span data-stu-id="65228-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="65228-130">Сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-131">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="65228-132">**Копировать**</span><span class="sxs-lookup"><span data-stu-id="65228-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="65228-133">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="65228-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="65228-134">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="65228-135">**копекс**</span><span class="sxs-lookup"><span data-stu-id="65228-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65228-136">Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="65228-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="65228-137">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="65228-138">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="65228-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65228-139">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-140">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65228-141">**делетикс**</span><span class="sxs-lookup"><span data-stu-id="65228-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="65228-142">Удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-143">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65228-144">**жетеффективепермиссион**</span><span class="sxs-lookup"><span data-stu-id="65228-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="65228-145">Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="65228-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="65228-146">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="65228-147">**Имени**</span><span class="sxs-lookup"><span data-stu-id="65228-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="65228-148">Переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-149">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="65228-150">**такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="65228-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="65228-151">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="65228-152">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="65228-153">**такеовнершипекс**</span><span class="sxs-lookup"><span data-stu-id="65228-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="65228-154">Получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="65228-155">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="65228-156">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="65228-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="65228-157">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-158">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="65228-159">**ункомпрессекс**</span><span class="sxs-lookup"><span data-stu-id="65228-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="65228-160">Распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="65228-161">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65228-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="65228-162">Свойства</span><span class="sxs-lookup"><span data-stu-id="65228-162">Properties</span></span>

<span data-ttu-id="65228-163">Класс **CIM \_ девицефиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="65228-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65228-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="65228-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65228-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65228-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-167">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")</span><span class="sxs-lookup"><span data-stu-id="65228-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="65228-168">Битовый массив, представляющий права доступа к заданному файлу или каталогу, который хранится у пользователя или группы, от имени которой возвращается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="65228-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="65228-169">На томах FAT возвращается **полный \_ доступ** , что означает, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="65228-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="65228-170">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="65228-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="65228-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="65228-172">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="65228-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="65228-173">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="65228-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="65228-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="65228-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="65228-175">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="65228-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="65228-176">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="65228-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="65228-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="65228-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="65228-178">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="65228-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="65228-179">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="65228-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="65228-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="65228-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="65228-181">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="65228-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="65228-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="65228-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="65228-183">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="65228-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="65228-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="65228-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="65228-185">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="65228-185">Grants the right to execute a file.</span></span> <span data-ttu-id="65228-186">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="65228-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="65228-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="65228-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="65228-188">Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65228-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="65228-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="65228-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="65228-190">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="65228-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="65228-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="65228-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="65228-192">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="65228-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="65228-193"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="65228-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="65228-194">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="65228-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="65228-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="65228-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="65228-196">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="65228-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="65228-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="65228-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="65228-198">Предоставляет доступ на запись к избирательному списку управления доступом.</span><span class="sxs-lookup"><span data-stu-id="65228-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="65228-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="65228-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="65228-200">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="65228-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="65228-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="65228-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="65228-202">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="65228-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="65228-203">**Архив**</span><span class="sxs-lookup"><span data-stu-id="65228-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-204">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-206">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")</span><span class="sxs-lookup"><span data-stu-id="65228-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="65228-207">Если задано **значение true**, файл должен быть архивирован.</span><span class="sxs-lookup"><span data-stu-id="65228-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="65228-208">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-209">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="65228-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-212">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="65228-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="65228-213">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-213">Short textual description of the object.</span></span>

<span data-ttu-id="65228-214">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65228-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="65228-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-218">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")</span><span class="sxs-lookup"><span data-stu-id="65228-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="65228-219">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="65228-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="65228-220">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-221">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="65228-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-224">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")</span><span class="sxs-lookup"><span data-stu-id="65228-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="65228-225">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="65228-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="65228-226">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="65228-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="65228-227">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="65228-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="65228-228">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="65228-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="65228-229">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="65228-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-233">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="65228-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-234">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="65228-234">Name of the class.</span></span>

<span data-ttu-id="65228-235">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="65228-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-237">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65228-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65228-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-239">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")</span><span class="sxs-lookup"><span data-stu-id="65228-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="65228-240">Дата создания файла.</span><span class="sxs-lookup"><span data-stu-id="65228-240">File's creation date.</span></span>

<span data-ttu-id="65228-241">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-242">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="65228-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-245">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="65228-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-246">Класс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="65228-246">Class of the computer system.</span></span>

<span data-ttu-id="65228-247">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="65228-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-251">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")</span><span class="sxs-lookup"><span data-stu-id="65228-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-252">Имя компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="65228-252">Name of the computer system.</span></span>

<span data-ttu-id="65228-253">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-254">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65228-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-257">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="65228-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="65228-258">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-258">Textual description of the object.</span></span>

<span data-ttu-id="65228-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65228-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-260">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="65228-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-263">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")</span><span class="sxs-lookup"><span data-stu-id="65228-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="65228-264">Буква диска (включая двоеточие, следующее за буквой диска) файла.</span><span class="sxs-lookup"><span data-stu-id="65228-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="65228-265">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-266">Пример: "c:"</span><span class="sxs-lookup"><span data-stu-id="65228-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="65228-267">**еигхтдотсрифиленаме**</span><span class="sxs-lookup"><span data-stu-id="65228-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-270">Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")</span><span class="sxs-lookup"><span data-stu-id="65228-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-271">Совместимое с DOS имя файла для файла.</span><span class="sxs-lookup"><span data-stu-id="65228-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="65228-272">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-273">Пример: "c: \\ рограмма ~ 1"</span><span class="sxs-lookup"><span data-stu-id="65228-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="65228-274">**Зашифрована**</span><span class="sxs-lookup"><span data-stu-id="65228-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-275">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-277">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")</span><span class="sxs-lookup"><span data-stu-id="65228-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="65228-278">**Значение true**, если файл зашифрован.</span><span class="sxs-lookup"><span data-stu-id="65228-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="65228-279">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="65228-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-283">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")</span><span class="sxs-lookup"><span data-stu-id="65228-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="65228-284">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="65228-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="65228-285">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="65228-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="65228-286">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="65228-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="65228-287">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="65228-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="65228-288">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-289">**Расширение**</span><span class="sxs-lookup"><span data-stu-id="65228-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-292">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")</span><span class="sxs-lookup"><span data-stu-id="65228-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="65228-293">Расширение имени файла без предшествующей точки (DOT).</span><span class="sxs-lookup"><span data-stu-id="65228-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="65228-294">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-295">Пример: "txt", "MOF", "MDB"</span><span class="sxs-lookup"><span data-stu-id="65228-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="65228-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="65228-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-299">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")</span><span class="sxs-lookup"><span data-stu-id="65228-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-300">Имя файла без расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="65228-300">File name without the file name extension.</span></span>

<span data-ttu-id="65228-301">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-302">Пример: "Мидатафиле"</span><span class="sxs-lookup"><span data-stu-id="65228-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="65228-303">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="65228-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-304">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65228-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65228-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-306">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="65228-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="65228-307">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="65228-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="65228-308">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-309">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="65228-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="65228-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="65228-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-313">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")</span><span class="sxs-lookup"><span data-stu-id="65228-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="65228-314">Дескриптор, представляющий тип файла (указывается свойством **Extension** ).</span><span class="sxs-lookup"><span data-stu-id="65228-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="65228-315">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-316">**фскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="65228-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-319">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="65228-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-320">Класс файловой системы.</span><span class="sxs-lookup"><span data-stu-id="65228-320">Class of the file system.</span></span>

<span data-ttu-id="65228-321">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-322">**Имя файловой системы**</span><span class="sxs-lookup"><span data-stu-id="65228-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-325">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")</span><span class="sxs-lookup"><span data-stu-id="65228-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="65228-326">Имя файловой системы.</span><span class="sxs-lookup"><span data-stu-id="65228-326">Name of the file system.</span></span>

<span data-ttu-id="65228-327">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-328">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="65228-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-331">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")</span><span class="sxs-lookup"><span data-stu-id="65228-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="65228-332">Если **значение — true**, файл скрыт.</span><span class="sxs-lookup"><span data-stu-id="65228-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="65228-333">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="65228-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-335">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65228-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65228-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="65228-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="65228-338">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-338">Date and time when the object was installed.</span></span> <span data-ttu-id="65228-339">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="65228-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="65228-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65228-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-341">**инусекаунт**</span><span class="sxs-lookup"><span data-stu-id="65228-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65228-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65228-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-344">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)</span><span class="sxs-lookup"><span data-stu-id="65228-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="65228-345">Число "файлов, открываемых в данный момент для файла".</span><span class="sxs-lookup"><span data-stu-id="65228-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="65228-346">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-347">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="65228-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="65228-348">**ластакцессед**</span><span class="sxs-lookup"><span data-stu-id="65228-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-349">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65228-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65228-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-351">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")</span><span class="sxs-lookup"><span data-stu-id="65228-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="65228-352">Дата и время последнего обращения к файлу.</span><span class="sxs-lookup"><span data-stu-id="65228-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="65228-353">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="65228-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-355">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65228-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65228-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-357">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")</span><span class="sxs-lookup"><span data-stu-id="65228-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="65228-358">Дата и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="65228-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="65228-359">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="65228-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-363">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65228-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65228-364">Унаследованное имя, служащее ключом экземпляра логического файла в файловой системе (укажите полные имена путей).</span><span class="sxs-lookup"><span data-stu-id="65228-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="65228-365">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65228-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="65228-366">Пример: "C: \\ Windows \\ System \\win.ini"</span><span class="sxs-lookup"><span data-stu-id="65228-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="65228-367">**Путь**</span><span class="sxs-lookup"><span data-stu-id="65228-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-370">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")</span><span class="sxs-lookup"><span data-stu-id="65228-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="65228-371">Путь к файлу, включая начальную и конечную обратную косую черту.</span><span class="sxs-lookup"><span data-stu-id="65228-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="65228-372">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-373">Пример: " \\ \\ система Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="65228-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="65228-374">**Чтения**</span><span class="sxs-lookup"><span data-stu-id="65228-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-375">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-377">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")</span><span class="sxs-lookup"><span data-stu-id="65228-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="65228-378">Если **значение — true**, файл можно считать.</span><span class="sxs-lookup"><span data-stu-id="65228-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="65228-379">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-380">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="65228-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65228-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65228-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-383">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="65228-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="65228-384">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="65228-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="65228-385">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="65228-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="65228-386">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="65228-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="65228-387">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="65228-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="65228-388">Невыполняемое состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="65228-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="65228-389">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="65228-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="65228-390">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="65228-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="65228-391">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65228-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="65228-392">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="65228-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="65228-393">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="65228-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="65228-394">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="65228-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="65228-395">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="65228-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="65228-396">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="65228-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="65228-397">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="65228-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="65228-398">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="65228-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="65228-399">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="65228-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="65228-400">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="65228-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="65228-401">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="65228-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="65228-402">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="65228-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="65228-403">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="65228-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="65228-404">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="65228-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="65228-405">**Система**</span><span class="sxs-lookup"><span data-stu-id="65228-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-406">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-408">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")</span><span class="sxs-lookup"><span data-stu-id="65228-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="65228-409">**Значение true**, если файл является системным файлом.</span><span class="sxs-lookup"><span data-stu-id="65228-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="65228-410">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="65228-411">**Writeable (Доступно для записи)**</span><span class="sxs-lookup"><span data-stu-id="65228-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65228-412">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65228-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65228-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65228-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65228-414">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")</span><span class="sxs-lookup"><span data-stu-id="65228-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="65228-415">Если **значение — true**, файл может быть записан.</span><span class="sxs-lookup"><span data-stu-id="65228-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="65228-416">Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65228-417">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65228-417">Remarks</span></span>

<span data-ttu-id="65228-418">Класс **CIM \_ девицефиле** является производным от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65228-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="65228-419">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="65228-419">WMI does not implement this class.</span></span>

<span data-ttu-id="65228-420">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="65228-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65228-421">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="65228-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65228-422">Требования</span><span class="sxs-lookup"><span data-stu-id="65228-422">Requirements</span></span>



| <span data-ttu-id="65228-423">Требование</span><span class="sxs-lookup"><span data-stu-id="65228-423">Requirement</span></span> | <span data-ttu-id="65228-424">Значение</span><span class="sxs-lookup"><span data-stu-id="65228-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65228-425">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65228-425">Minimum supported client</span></span><br/> | <span data-ttu-id="65228-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65228-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65228-427">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65228-427">Minimum supported server</span></span><br/> | <span data-ttu-id="65228-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65228-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65228-429">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="65228-429">Namespace</span></span><br/>                | <span data-ttu-id="65228-430">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65228-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65228-431">MOF</span><span class="sxs-lookup"><span data-stu-id="65228-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65228-432"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65228-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65228-433">DLL</span><span class="sxs-lookup"><span data-stu-id="65228-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65228-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65228-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65228-435">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65228-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65228-436">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="65228-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

