---
description: Определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре разрешений для объекта файла, каталога и общего ресурса, в котором расположен файл ярлыка, если файл или каталог находится в общей папке.
ms.assetid: 36f823c1-fa19-40a1-b750-41e1f73bdf01
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса Win32_ShortcutFile (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52b57318ac05212304024ead82026d6daf0d8ea4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141314"
---
# <a name="geteffectivepermission-method-of-the-win32_shortcutfile-class"></a>Метод Жетеффективепермиссион \_ класса Win32 шорткутфиле

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) жетеффективепермиссион определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре *Permissions* для объекта File, каталога и общего ресурса, в котором расположен файл ярлыка, если файл или каталог находится в общей папке.

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

Битовая карта разрешений.

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

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Файл \_ ВЫПОЛНИТЬ (файл) \_ обход файла (каталог)** (32 (0x20))


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

Предоставляет доступ на запись к списку управления доступом на уровне пользователей (DACL).

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

Возвращает **значение true** , если пользователь имеет указанные разрешения, и **значение false** , если пользователь не имеет указанных разрешений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Аклуи. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Шорткутфиле Win32**](win32-shortcutfile.md)
</dt> </dl>

 

