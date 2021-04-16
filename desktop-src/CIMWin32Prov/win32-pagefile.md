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
# <a name="win32_pagefile-class"></a>\_Класс файла подкачки Win32

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ файла подкачки Win32** представляет файл, используемый для обработки страничной замены файла виртуальной памяти в системе Win32. Этот класс не рекомендуется к использованию.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **\_ файла подкачки Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ файла подкачки Win32** содержит следующие методы.



| Метод                                                                                            | Описание                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-pagefile.md)     | Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                       |
| [**чанжесекуритипермиссионсекс**](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                       |
| [**Повторно**](compress-method-in-class-win32-pagefile.md)                                       | Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                  |
| [**компрессекс**](compressex-method-in-class-win32-pagefile.md)                                   | Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                  |
| [**Копировать**](copy-method-in-class-win32-pagefile.md)                                               | Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.<br/>                                                                                       |
| [**копекс**](copyex-method-in-class-win32-pagefile.md)                                           | Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром FileName.<br/>                                                                                    |
| [**Удалить**](delete-method-in-class-win32-pagefile.md)                                           | Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                     |
| [**делетикс**](deleteex-method-in-class-win32-pagefile.md)                                       | Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                     |
| [**жетеффективепермиссион**](geteffectivepermission-method-in-class-win32-pagefile.md)           | Метод класса, определяющий, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом *разрешения* , не только для объекта File, но и для общего ресурса, в котором находится файл или каталог (если он находится в общей папке).<br/> |
| [**Имени**](rename-method-in-class-win32-pagefile.md)                                           | Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                     |
| [**такеовнершип**](takeownership-method-in-class-win32-pagefile.md)                             | Метод класса, который получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                                       |
| [**такеовнершипекс**](takeownershipex-method-in-class-win32-pagefile.md)                         | Метод класса, который получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                                       |
| [**Распаковать**](uncompress-method-in-class-win32-pagefile.md)                                   | Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                |
| [**ункомпрессекс**](uncompressex-method-in-class-win32-pagefile.md)                               | Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                |



 

### <a name="properties"></a>Свойства

Класс **\_ файла подкачки Win32** имеет следующие свойства.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("права доступа")
</dt> </dl>

Битовая маска, представляющая права доступа, необходимые для доступа к файлу или выполнения конкретных операций над ним. Значения см. в разделе [**константы прав доступа к файлам и каталогам**](../wmisdk/file-and-directory-access-rights-constants.md).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**Файл \_ ЧТЕНИЕ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**Файл \_ НАПИСАНие \_ соглашения EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**Файл \_ Удаление \_ дочернего (каталога)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**Файл \_ ЗАПИСЬ \_ атрибутов** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Delete** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Чтение \_ Элемент управления** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Запись \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Запись \_ Владелец** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Синхронизация** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Архив**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("следует архивировать")
</dt> </dl>

Если задано **значение true**, файл должен быть архивирован.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("сжатый")
</dt> </dl>

**Значение true**, если файл сжат.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**компрессионмесод**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод сжатия")
</dt> </dl>

Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла. Если схема сжатия неизвестна или не описана, используйте "Unknown". Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый". Если логический файл не сжат, используйте параметр NOT сжатый.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")
</dt> </dl>

Имя класса.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Дата создания")
</dt> </dl>

Дата и время создания файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**кскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы компьютера ")
</dt> </dl>

Класс компьютерной системы.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя системы компьютера ")
</dt> </dl>

Имя компьютерной системы.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Накопитель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("диск")
</dt> </dl>

Буква диска (включая двоеточие, следующее за буквой диска) файла. Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "c:"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**еигхтдотсрифиленаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("восемь точек имя файла")
</dt> </dl>

Имя файла, совместимое с DOS.

Пример: "c: \\ рограмма ~ 1"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Зашифрована**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("зашифровано")
</dt> </dl>

**Значение true**, если файл зашифрован.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("метод шифрования")
</dt> </dl>

Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла. Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown". Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted". Если логический файл не зашифрован, используйте параметр NOT encrypted.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Расширение**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("расширение файла")
</dt> </dl>

Расширение имени файла без предшествующей точки (DOT).

Пример: "txt", "MOF", "MDB"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя файла")
</dt> </dl>

Имя файла без расширения имени файла. Пример: "Мидатафиле"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Размер файла**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("размер"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Размер файла в байтах.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип файла")
</dt> </dl>

Дескриптор, представляющий тип файла, указанный в свойстве **Extension** .

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FreeSpace**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| дваваилпажефиле"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Место, доступное в файле подкачки. Операционная система может увеличить файл подкачки по мере необходимости, вплоть до ограничения, наложенного пользователем. Это свойство показывает разницу между размером текущей выделенной памяти и текущим размером файла подкачки. Он не показывает самый крупный возможный размер файла подкачки.

</dd> <dt>

**фскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса файловой системы ")
</dt> </dl>

Класс файловой системы.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Имя файловой системы**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя файловой системы ")
</dt> </dl>

Имя файловой системы.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Скрыта**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("скрыто")
</dt> </dl>

Если **значение — true**, файл скрыт.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**инитиалсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ управления \\ \\ \\ \\ памятью диспетчер сеансов \| пагингфилес"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Начальный размер файла подкачки.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**инусекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) (текущее число открытых файлов)
</dt> </dl>

Число "файлов, открываемых в данный момент для файла".

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**ластакцессед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последний доступ")
</dt> </dl>

Дата и время последнего доступа к файлу.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Последнее изменение")
</dt> </dl>

Дата и время последнего изменения файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")
</dt> </dl>

Строка производителя из ресурса версии (если таковая имеется).

Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| двтоталпажефиле"), [**единицы**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Максимальный размер файла подкачки, заданный пользователем. Операционная система не позволит файлу подкачки превысить это ограничение.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**переопределять**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**нткуерисистеминформатион**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| системпажефилеинформатион \| пажефиленаме")
</dt> </dl>

Имя файла подкачки.

Пример: "C: \\PAGEFILE.SYS"

</dd> <dt>

**Путь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("путь")
</dt> </dl>

Путь к файлу, включая начальную и конечную обратную косую черту.

Пример: " \\ \\ система Windows \\ "

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Чтения**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("доступно для чтения")
</dt> </dl>

Если **значение — true**, файл можно считать.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Строка, указывающая текущее состояние объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**Система**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("системный файл")
</dt> </dl>

**Значение true**, если файл является системным файлом.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("версия")
</dt> </dl>

Строка версии из ресурса версии (если таковая имеется).

Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).

</dd> <dt>

**Writeable (Доступно для записи)**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("с возможностью записи")
</dt> </dl>

Если **значение — true**, файл может быть записан.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ файла подкачки Win32** является производным от [**\_ каталога CIM**](cim-directory.md).

## <a name="examples"></a>Примеры

В следующем образце кода VBScript показано, как получить статистику файла **\_ подкачки** из экземпляров файла данных Win32.


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



В следующем образце кода Perl показано, как извлекать статистику файлов **\_ подкачки из экземпляров файлового файла Win32**.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
