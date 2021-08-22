---
description: Классы WMI, представляющие файлы или каталоги, такие как Win32 \_ кодекфиле или CIM \_ File, содержат свойство AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Константы прав доступа к файлам и каталогам (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8678627b0f7d9ce2ed7f9c8e7e39c49bdcd3b6c3a8313f7d7b3c517c379093d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131386"
---
# <a name="file-and-directory-access-rights-constants"></a>Константы прав доступа к файлам и каталогам

Классы WMI, представляющие файлы или каталоги, такие как [**Win32 \_ Кодекфиле**](/windows/desktop/CIMWin32Prov/win32-codecfile) или [**CIM \_ File**](/windows/desktop/CIMWin32Prov/cim-datafile), содержат свойство **AccessMask** . Это свойство содержит битовые параметры, указывающие права доступа, которые должен иметь пользователь или группа для конкретного доступа или операций с файлом. Дополнительные сведения см. в статьях [безопасность и права доступа к файлам](/windows/desktop/FileIO/file-security-and-access-rights) и [изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

Классы файла или каталога, содержащие свойство **AccessMask** , включают:

-   [**\_Файл CIM**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_Каталог CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**\_LOGICALFILE CIM**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**\_Кодекфиле Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**\_Каталог Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**\_Нтевентлогфиле Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**\_Общий ресурс Win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**\_Шорткутфиле Win32**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

В следующем списке перечислены значения прав доступа к файлу и каталогу в свойстве **AccessMask** . Это свойство является точечным рисунком.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_Чтение \_ данных файла**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Предоставляет право на чтение данных из файла.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_каталог списка \_ файлов**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Предоставляет право на чтение данных из файла. Для каталога это значение предоставляет право на перечисление содержимого каталога.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_данные записи \_ файла**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Предоставляет право на запись данных в файл.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ФАЙЛ \_ Добавить \_ файл**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Предоставляет право на запись данных в файл. Для каталога это значение предоставляет право на создание файла в каталоге.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_Добавление \_ данных в файл**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Предоставляет право добавлять данные в файл. Для каталога это значение предоставляет право на создание подкаталога.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**ФАЙЛ \_ Добавить \_ подкаталог**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Предоставляет право добавлять данные в файл. Для каталога это значение предоставляет право на создание подкаталога.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**\_чтение файла \_ EA**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Предоставляет право на чтение расширенных атрибутов.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**запись в файл \_ \_ EA**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Предоставляет право на запись расширенных атрибутов.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_выполнение файла**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Предоставляет право на выполнение файла.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_обход файла**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Предоставляет право на выполнение файла. Для каталога можно просмотреть каталог.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_дочерний файл удаления файла \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_атрибуты чтения \_ файла**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Предоставляет право на чтение атрибутов файлов.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_атрибуты записи \_ файла**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Предоставляет право на изменение атрибутов файлов.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**УДАЛЕН**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Право на удаление объекта.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**\_Контроль чтения**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Предоставляет право на чтение сведений в дескрипторе безопасности для объекта, не включая сведения из списка SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ЗАПИСЬ \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Предоставляет право на изменение списка DACL в дескрипторе безопасности объекта для объекта.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**\_владелец записи**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Предоставляет право на изменение владельца в дескрипторе безопасности для объекта.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**ПОЛНИТ**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Предоставляет право на использование объекта для синхронизации. Это позволяет процессу ожидать, пока объект не поступает в сигнальное состояние. Некоторые типы объектов не поддерживают это право доступа.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Файл Winnt. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> </dl>

 

