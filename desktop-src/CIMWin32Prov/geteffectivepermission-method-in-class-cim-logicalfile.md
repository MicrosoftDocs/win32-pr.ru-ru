---
description: Определяет, имеет ли вызывающий объект агрегированные разрешения для \_ объекта LOGICALFILE CIM и общую папку, в которой находится файл или каталог, как указано в аргументе Permissions.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса CIM_LogicalFile (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fcafa33d9761d813b075b0f6bb56e5d940c73346bea4d4147366b5569679b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675828"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a>Метод Жетеффективепермиссион \_ класса CIM LogicalFile

Метод **жетеффективепермиссион** определяет, есть ли у вызывающего объекта агрегированные разрешения на объект [**CIM \_ LogicalFile**](cim-logicalfile.md) , а также общую папку, в которой находится файл или каталог, как указано в аргументе *Permissions* .

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Список разрешений, о которых может запросить пользователь.

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

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)


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

Предоставляет право на удаление каталога и всех содержащихся в нем файлов, даже если файлы доступны только для чтения.

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

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если вызов имеет необходимое разрешение; в противном случае возвращается **значение false**.

## <a name="remarks"></a>Remarks

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Аклуи. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_LOGICALFILE CIM**](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

