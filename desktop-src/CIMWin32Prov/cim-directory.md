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
ms.openlocfilehash: 38f41b28689ac8ae4bebc29248e27d8e6b17eae1b265237acd91ed2b03d97c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321604"
---
# <a name="cim_directory-class"></a>\_Класс каталога CIM

Класс **\_ каталога CIM** представляет тип файла, который логически группирует содержащиеся в нем файлы данных и предоставляет сведения о пути для сгруппированных файлов.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **\_ каталога CIM** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ каталога CIM** содержит следующие методы.



| Метод                                                                                           | Описание                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-directory.md)     | Изменяет разрешения безопасности для логического файла, указанного в пути к объекту. Не реализовано инструментарием WMI.<br/>                                   |
| [**чанжесекуритипермиссионсекс**](changesecuritypermissionsex-method-in-class-cim-directory.md) | Изменяет разрешения безопасности для логического файла, указанного в пути к объекту. Не реализовано инструментарием WMI.<br/>                                   |
| [**Повторно**](compress-method-in-class-cim-directory.md)                                       | Сжимает логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                              |
| [**компрессекс**](compressex-method-in-class-cim-directory.md)                                   | Сжимает логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                              |
| [**Копировать**](copy-method-in-class-cim-directory.md)                                               | Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром. Не реализовано инструментарием WMI.<br/> |
| [**копекс**](copyex-method-in-class-cim-directory.md)                                           | Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром. Не реализовано инструментарием WMI.<br/> |
| [**Удален**](delete-method-in-class-cim-directory.md)                                           | Удаляет логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                                 |
| [**делетикс**](deleteex-method-in-class-cim-directory.md)                                       | Удаляет логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                                 |
| [**жетеффективепермиссион**](geteffectivepermission-method-in-class-cim-directory.md)           | Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** . Не реализовано инструментарием WMI.<br/>                |
| [**Имени**](rename-method-in-class-cim-directory.md)                                           | Переименовывает логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                                 |
| [**такеовнершип**](takeownership-method-in-class-cim-directory.md)                             | Получает владение логическим файлом, указанным в пути объекта. Не реализовано инструментарием WMI.<br/>                                                   |
| [**такеовнершипекс**](takeownershipex-method-in-class-cim-directory.md)                         | Получает владение логическим файлом, указанным в пути объекта. Не реализовано инструментарием WMI.<br/>                                                   |
| [**Распаковать**](uncompress-method-in-class-cim-directory.md)                                   | Распаковывает логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                            |
| [**ункомпрессекс**](uncompressex-method-in-class-cim-directory.md)                               | Распаковывает логический файл (или каталог), указанный в пути объекта. Не реализовано инструментарием WMI.<br/>                                            |



 

### <a name="properties"></a>Свойства

Класс **\_ каталога CIM** имеет следующие свойства.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")
</dt> </dl>

Битовая маска, представляющая права доступа, необходимые для доступа к каталогу или выполнения конкретных операций с ним. Значения см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.

 

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

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")
</dt> </dl>

Если задано **значение true**, файл должен быть архивирован.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
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

Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("сжатый")
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

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод сжатия")
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

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")
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

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Дата создания")
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

Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы компьютера ")
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

Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CSName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя системы компьютера ")
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

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
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

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")
</dt> </dl>

Буква диска (включая двоеточие, следующее за буквой диска) файла. Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "c:"

</dd> <dt>

**еигхтдотсрифиленаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")
</dt> </dl>

Имя файла, совместимое с DOS. Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "c: \\ рограмма ~ 1"

</dd> <dt>

**Зашифрована**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")
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

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("метод шифрования")
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

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("расширение файла")
</dt> </dl>

Расширение имени файла без предшествующей точки (DOT).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "txt", "MOF", "MDB"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")
</dt> </dl>

Имя файла без расширения имени файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "Мидатафиле"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Размер файла в байтах.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип файла")
</dt> </dl>

Дескриптор, представляющий тип файла (указывается свойством **Extension** ).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**фскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса файловой системы ")
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

Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Файловая система CIM**](cim-filesystem.md)".**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя файловой системы ")
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

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("скрыто")
</dt> </dl>

Если **значение — true**, файл скрыт.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**инусекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (текущее число открытых файлов)
</dt> </dl>

Число "файлов, открываемых в данный момент для файла".

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ластакцессед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последний доступ")
</dt> </dl>

Дата и время последнего обращения к файлу.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Последнее изменение")
</dt> </dl>

Дата и время последнего изменения файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Унаследованное имя, служащее ключом экземпляра логического файла в файловой системе (укажите полные имена путей).

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

пример: "C: \\ Windows \\ system \\win.ini"

</dd> <dt>

**Путь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")
</dt> </dl>

Путь к файлу, включая начальную и конечную обратную косую черту. Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: " \\ \\ система Windows \\ "

</dd> <dt>

**Чтения**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")
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

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
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

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("системный файл")
</dt> </dl>

**Значение true**, если файл является системным файлом.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Writeable (Доступно для записи)**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("с возможностью записи")
</dt> </dl>

Если **значение — true**, файл может быть записан.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ каталога CIM** является производным от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Инструментарий WMI не реализует этот класс. Дополнительные сведения о классах, производных от **\_ каталога CIM**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

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

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

