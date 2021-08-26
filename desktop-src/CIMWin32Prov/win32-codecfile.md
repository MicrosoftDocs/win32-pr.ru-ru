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
ms.openlocfilehash: 1d9f41178c69f40513b26de5221af6eb7b5e425acf5c4893f2de87fb18211291
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079914"
---
# <a name="win32_codecfile-class"></a>\_Класс Win32 кодекфиле

Класс **WMI \_ кодекфиле** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет аудио или видеокодек, установленный в компьютерной системе. Кодеки преобразуют один тип формата мультимедиа в другой, обычно это сжатый формат в несжатый формат. Имя «кодек» является производным от сочетания сжатия и распаковки. Например, кодек может преобразовать сжатый формат, например MS-ADPCM, в несжатый формат, например PCM, который может играться в большинстве звуков.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **Win32 \_ кодекфиле** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ кодекфиле** содержит следующие методы.



| Метод                                                                                             | Описание                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                         |
| [**чанжесекуритипермиссионсекс**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                         |
| [**Повторно**](compress-method-in-class-win32-codecfile.md)                                       | Сжимает логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                    |
| [**компрессекс**](compressex-method-in-class-win32-codecfile.md)                                   | Сжимает логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                    |
| [**Копировать**](copy-method-in-class-win32-codecfile.md)                                               | Копирует логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.<br/>                                                                                         |
| [**копекс**](copyex-method-in-class-win32-codecfile.md)                                           | Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром FileName.<br/>                                                                    |
| [**Удален**](delete-method-in-class-win32-codecfile.md)                                           | Удаляет логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                       |
| [**делетикс**](deleteex-method-in-class-win32-codecfile.md)                                       | Удаляет логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                       |
| [**жетеффективепермиссион**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Определяет, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом **разрешения** , не только для объекта File, но и для общего ресурса, в котором находится файл или каталог (если он находится в общей папке).<br/> |
| [**Имени**](rename-method-in-class-win32-codecfile.md)                                           | Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                     |
| [**такеовнершип**](takeownership-method-in-class-win32-codecfile.md)                             | Получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                                         |
| [**такеовнершипекс**](takeownershipex-method-in-class-win32-codecfile.md)                         | Метод класса, который получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                       |
| [**Распаковать**](uncompress-method-in-class-win32-codecfile.md)                                   | Распаковывает логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                  |
| [**ункомпрессекс**](uncompressex-method-in-class-win32-codecfile.md)                               | Распаковывает логический файл (или каталог), указанный в пути объекта.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ кодекфиле** имеет следующие свойства.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")
</dt> </dl>

Битовая маска, представляющая права доступа, необходимые для доступа или выполнения конкретных операций с файлом кодека. Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

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

Краткое описание объекта.

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

Алгоритм или инструмент, используемый для сжатия логического файла. Если невозможно (или не требуется) описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, сжат ли логический файл. "Сжатый" для представления того, что файл сжат, но либо его схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что логический файл не сжат.

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

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

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

Дата создания файла.

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

Строка, представляющая имя компьютерной системы.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (описание), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ медиаресаурцес \\ \\ ICM \| Description")
</dt> </dl>

Полное имя драйвера кодека. Эта строка должна отображаться в виде длинных (описательных) пробелов.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

Пример: "Microsoft PCM Converter"

</dd> <dt>

**Накопитель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("диск")
</dt> </dl>

Буква диска (включая двоеточие) файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Совместимое с DOS имя файла для этого файла.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Алгоритм или инструмент, используемый для шифрования логического файла. Если вы не можете (или не хотите) описать схему шифрования (возможно, по соображениям безопасности), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, зашифрован ли логический файл. "Encrypted" для представления того, что файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается. и «not encrypted» для представления того, что логический файл не зашифрован.

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

Расширение имени файла (без точки).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Примеры: "txt", "MOF", "MDB"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")
</dt> </dl>

Имя файла (без расширения).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

Пример: "Autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Размер файла (в байтах).

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

Тип файла (указывается свойством **расширения** ).

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

**Группа**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")
</dt> </dl>

Кодек, представленный этим классом.

Значения качества производительности:

<dl> <dd>Аудиосигнал</dd> <dd>Роли</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Звук** ("аудио")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Видео** ("видео")


</dt> <dd></dd> </dl>

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

Объект был установлен. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

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

Последний доступ к файлу.

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

Файл был изменен в последний раз.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")
</dt> </dl>

Строка производителя из ресурса версии, если таковая имеется.

Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Унаследованное имя, служащее ключом экземпляра логического файла в файловой системе. Необходимо указать полные имена путей.

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

Путь к файлу. Сюда входят начальные и конечные обратные косые черты.

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Файл может быть прочитан.

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

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

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

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("версия")
</dt> </dl>

Строка версии из ресурса версии, если таковая имеется.

Это свойство наследуется от [**CIM- \_ файла**](cim-datafile.md).

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

Класс **Win32 \_ кодекфиле** является производным от [**CIM- \_ файла**](cim-datafile.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

