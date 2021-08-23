---
description: Каталог Win32 \_&\# 32; Класс WMI представляет запись каталога в компьютерной системе, на которой работает Windows.
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
ms.openlocfilehash: 1247a965f5d447ab2e6e86737feff96b205a6a74e3cab5e3e94cade9a2f8394c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699854"
---
# <a name="win32_directory-class"></a>\_Класс каталога Win32

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ каталога Win32** представляет запись каталога в компьютерной системе, на которой работает Windows. Каталог — это тип файла, который логически группирует файлы данных и предоставляет сведения о пути для сгруппированных файлов. Пример: C: \\ TEMP. **Win32 \_ Каталог** не включает каталоги сетевых дисков.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **\_ каталога Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ каталога Win32** содержит следующие методы.



| Метод                                                                                             | Описание                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-directory.md)     | Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                        |
| [**чанжесекуритипермиссионсекс**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Метод класса, который изменяет разрешения безопасности для логического файла, указанного в пути к объекту.<br/>                                                                                                                        |
| [**Повторно**](compress-method-in-class-win32-directory.md)                                       | Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                   |
| [**компрессекс**](compressex-method-in-class-win32-directory.md)                                   | Метод класса, который сжимает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                   |
| [**Копировать**](copy-method-in-class-win32-directory.md)                                               | Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.<br/>                                                                                        |
| [**копекс**](copyex-method-in-class-win32-directory.md)                                           | Метод класса, копирующий логический файл или каталог, указанный в пути к объекту, в расположение, указанное параметром *filename* .<br/>                                                                                   |
| [**Удален**](delete-method-in-class-win32-directory.md)                                           | Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                      |
| [**делетикс**](deleteex-method-in-class-win32-directory.md)                                       | Метод класса, который удаляет логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                      |
| [**жетеффективепермиссион**](geteffectivepermission-method-in-class-win32-directory.md)           | Метод класса, определяющий, имеет ли вызывающий объект агрегированные разрешения, заданные аргументом *Permissions* , не только для объекта File, но и для общей папки, в которой находится файл или каталог (если он находится в общей папке).<br/> |
| [**Имени**](rename-method-in-class-win32-directory.md)                                           | Метод класса, который переименовывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                      |
| [**такеовнершип**](takeownership-method-in-class-win32-directory.md)                             | Метод класса, который получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                                        |
| [**такеовнершипекс**](takeownershipex-method-in-class-win32-directory.md)                         | Метод класса, который получает владение логическим файлом, указанным в пути объекта.<br/>                                                                                                                                        |
| [**Распаковать**](uncompress-method-in-class-win32-directory.md)                                   | Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                 |
| [**ункомпрессекс**](uncompressex-method-in-class-win32-directory.md)                               | Метод класса, который распаковывает логический файл (или каталог), указанный в пути к объекту.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Свойства

Класс **\_ каталога Win32** имеет следующие свойства.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("права доступа")
</dt> </dl>

Битовая маска, представляющая права доступа, необходимые для доступа к каталогу или выполнения конкретных операций с ним. Значения битов см. в разделе [**константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> На томах FAT вместо него возвращается значение **полного \_ доступа** , означающее, что для объекта не задана безопасность.

 

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)


</dt> <dd>

Предоставляет право на чтение данных из файла. Для каталога это значение предоставляет право на перечисление содержимого каталога.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)


</dt> <dd>

Предоставляет право на запись данных в файл. Для каталога это значение предоставляет право на создание файла в каталоге.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог** (4)


</dt> <dd>

Предоставляет право добавлять данные в файл. Для каталога это значение предоставляет право на создание подкаталога.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8)


</dt> <dd>

Предоставляет право на чтение расширенных атрибутов.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16)


</dt> <dd>

Предоставляет право на запись расширенных атрибутов.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)


</dt> <dd>

Предоставляет право на выполнение файла. Для каталога можно просмотреть каталог.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64)


</dt> <dd>

Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)


</dt> <dd>

Предоставляет право на чтение атрибутов файлов.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256)


</dt> <dd>

Предоставляет право на изменение атрибутов файлов.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Delete** (65536)


</dt> <dd>

Предоставляет доступ на удаление.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072)


</dt> <dd>

Предоставляет доступ на чтение дескриптора безопасности и владельца.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144)


</dt> <dd>

Предоставляет доступ на запись к избирательному списку управления доступом.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288)


</dt> <dd>

Назначает владельца записи.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Синхронизация** (1048576)


</dt> <dd>

Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Доступ к \_ \_Безопасность системы** (18809343)


</dt> <dd>

Управляет возможностью получения или задания списка SACL в дескрипторе безопасности объекта.

</dd> </dl>

</dd> <dt>

**Архив**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("следует архивировать")
</dt> </dl>

Указывает, задан ли бит архива для папки. Бит архива используется программами резервного копирования для обнаружения файлов, для которых необходимо создать резервную копию. Если задано **значение true**, файл должен быть архивирован.

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

Указывает, сжата ли папка. Инструментарий WMI распознает папки, сжатые с помощью самого инструментария WMI или графического пользовательского интерфейса. Однако он не распознает .ZIP файлы как сжатые. **Значение true**, если файл сжат.

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

Алгоритм или средство (обычно метод), используемые для сжатия логического файла. Если невозможно (или не требуется) описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы представить, что неизвестно, сжат ли логический файл. "Сжатый" для представления того, что файл сжат, но либо его схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что логический файл не сжат.

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

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

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

Дата создания объекта файловой системы. Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Имя класса создания для системы компьютера с областями.

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

Имя компьютера, на котором хранится объект файловой системы.

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

Буква диска (включая двоеточие), где хранится объект файловой системы.

Пример: "c:"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**еигхтдотсрифиленаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("восемь точек имя файла")
</dt> </dl>

Имя папки, совместимое с MS-DOS.

Пример: "c: \\ рограмма ~ 1"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Зашифрована**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("зашифровано")
</dt> </dl>

Указывает, была ли зашифрована папка. **Значение true**, если папка зашифрована.

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

Расширение имени файла для объекта файловой системы, не включая точку (.), которая отделяет расширение от имени файла.

Примеры: "txt", "MOF", "MDB"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя файла")
</dt> </dl>

Имя файла (без точки или расширения) файла.

Пример: "Autoexec"

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Размер объекта файловой системы в байтах. Хотя папки обладают свойством **Размер файла** , всегда возвращается значение 0. Чтобы определить размер папки, используйте FileSystemObject или добавьте размер всех файлов, хранящихся в папке.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Например, файл. mdb, скорее всего, будет иметь тип файла приложение Microsoft Access. Файл. ASP, вероятно, имеет файл HTML-документ. Папки обычно выводятся просто как папка.

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

Тип файловой системы (NTFS, FAT, FAT32), установленной на диске, где находится файл или папка.

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

Указывает, скрыт ли объект файловой системы. Если **значение — true**, файл скрыт.

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

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

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

Дата последнего обращения к файлу. Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Дата последнего изменения файла. Дополнительные сведения о работе с форматами даты и времени WMI см. в разделе [задачи WMI: даты и время](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Свойство Name — это строка, представляющая унаследованное имя, которое служит ключом экземпляра логического файла в файловой системе. Необходимо указать полные имена путей. пример: C: \\ Windows \\ system \\win.ini

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Путь**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("путь")
</dt> </dl>

Путь к файлу. Путь включает в себя начальную и конечную обратную косую черту, но не букву диска или имя папки.

Для папки c: \\ Windows \\ system32 \\ WBEM путь — \\ Windows \\ system32 \\ . Для папки c: \\ используется путь \\ .

Это свойство наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Чтения**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("доступно для чтения")
</dt> </dl>

Указывает, можно ли читать элементы в папке. Если **значение — true**, файл можно считать.

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

Указывает, является ли объект системным файлом. **Значение true**, если файл является системным файлом

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

Класс **\_ каталога Win32** является производным от [**\_ каталога CIM**](cim-directory.md).

**Обзор**

Папки — это объекты файловой системы, предназначенные для хранения других объектов файловой системы. Однако это не означает, что все папки являются одинаковыми. Вместо этого они могут значительно варьироваться. Некоторые папки являются папками операционной системы, которые, как правило, не должны изменяться сценарием. Некоторые папки доступны только для чтения. Это означает, что пользователи могут получать доступ к содержимому этой папки, но не могут добавлять, удалять или изменять эти содержимое. Некоторые папки сжимаются для оптимального хранилища, другие — как скрытые и невидимые для пользователей.

Инструментарий WMI использует класс **\_ каталога Win32** для управления папками. В значительной степени свойства и методы, доступные в этом классе, идентичны свойствам и методам, доступным в классе [**\_ файлов CIM**](cim-datafile.md) , класс, используемый для управления файлами. Это означает, что после того, как вы узнали, как управлять папками с помощью инструментария WMI, вы, без дополнительной работы, также узнаете, как управлять файлами.

Класс [**сопоставления \_ подкаталога Win32**](win32-subdirectory.md) также используется для управления файлами и папками. Класс **\_ подкаталога Win32** связывает папку и ее непосредственные вложенные папки. Например, в структуре папок C: \\ \\ журналы скриптов, журналы — это вложенная папка сценариев, а сценарии — это вложенная папка корневой папки C: \\ . Однако журналы не считаются вложенными папками C: \\ .

Свойства любой папки в файловой системе можно получить с помощью класса **\_ каталога Win32** . Свойства, доступные с помощью этого класса, показаны в таблице 11,1. чтобы получить свойства для одной папки, Windows создайте запрос на языке запросов (WQL) для класса **\_ каталога Win32** , убедившись, что вы включили имя папки. Например, этот запрос привязывается к папке D: \\ Archive:

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

При указании имени файла или папки в WQL-запросе убедитесь, что \\ для разделения компонентов пути используется две обратные косые черты ( \\ ).

Если требуется ограничить извлечение данных на один диск, включите предложение WHERE, указывающее букву диска. Например, этот запрос возвращает список всех папок на диске C:

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Если необходимо перечислить все папки на компьютере, учтите, что выполнение этого запроса может занять длительное время.

## <a name="examples"></a>Примеры

Следующий пример сценария VBScript извлекает свойства папки C: \\ Scripts.


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



Следующий пример сценария VBScript возвращает список всех скрытых папок на компьютере.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



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

[**\_Каталог CIM**](cim-directory.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

