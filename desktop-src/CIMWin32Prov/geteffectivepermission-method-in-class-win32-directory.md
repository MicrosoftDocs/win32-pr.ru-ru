---
description: Определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре Permissions для \_ объекта каталога Win32, каталога и общего ресурса, где расположен файл записи каталога (если файл или каталог находятся в общей папке).
ms.assetid: ece22cb0-a4ca-4ad7-b6d3-213dda4ce5b1
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса Win32_Directory (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2a4c17785e931c32cbca65d79cfd5931e4c0848a65a36132bef78d379401241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760524"
---
# <a name="geteffectivepermission-method-of-the-win32_directory-class"></a>Метод Жетеффективепермиссион \_ класса каталога Win32

Метод [](geteffectivepermission-method-in-class-win32-shortcutfile.md) [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) жетеффективепермиссион определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре *Permissions* для объекта [**\_ каталога Win32**](win32-directory.md) , каталога и общего ресурса, где расположен файл записи каталога (если файл или каталог находится в общей папке).

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Разрешения* \[ окне\]
</dt> <dd>

Битовая карта разрешений, о которых может запросить вызывающий объект.

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файл) \_ каталог списка файлов \_ (каталог)** (1 (0x1))


</dt> <dd>

Предоставляет право на чтение данных из файла. Для каталога это значение предоставляет право на перечисление содержимого каталога.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) файл \_ Добавить \_ файл (каталог)** (2 (0x2))


</dt> <dd>

Предоставляет право на запись данных в файл. Для каталога это значение предоставляет право на создание файла в каталоге.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файл) файл \_ Добавить \_ подкаталог (каталог)** (4 (0x4))


</dt> <dd>

Предоставляет право добавлять данные в файл. Для каталога это значение предоставляет право на создание подкаталога.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8 (0x8))


</dt> <dd>

Предоставляет право на чтение расширенных атрибутов.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16 (0x10))


</dt> <dd>

Предоставляет право на запись расширенных атрибутов.

</dd> <dt>

<span id="FILE_EXECUTE__file_______FILE_TRAVERSE__directory_"></span><span id="file_execute__file_______file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_______FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file_______FILE_TRAVERSE__directory_"></span><span id="file_execute__file_______file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_______FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНИТЬ (файл) \_ обход файла (каталог)** (32 (0x20))


</dt> <dd>

Предоставляет право на выполнение файла. Для каталога можно просмотреть каталог.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64 (0x40))


</dt> <dd>

Предоставляет право на удаление каталога и всех содержащихся в нем файлов, даже если файлы доступны только для чтения.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128 (0x80))


</dt> <dd>

Предоставляет право на чтение атрибутов файлов.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256 (0x100))


</dt> <dd>

Предоставляет право на изменение атрибутов файлов.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))


</dt> <dd>

Предоставляет доступ на удаление.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072 (0x20000))


</dt> <dd>

Предоставляет доступ на чтение дескриптора безопасности и владельца.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144 (0x40000))


</dt> <dd>

Предоставляет доступ на запись к списку управления доступом на уровне пользователей.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288 (0x80000))


</dt> <dd>

Назначает владельца записи.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))


</dt> <dd>

Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если вызывающий объект имеет указанные разрешения, и **false** , если вызывающий объект не имеет указанных разрешений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Аклуи. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Каталог Win32**](win32-directory.md)
</dt> </dl>

 

