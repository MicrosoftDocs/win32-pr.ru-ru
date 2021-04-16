---
description: Этот класс является классом типа событий для событий дискового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: Класс DiskIo_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542514"
---
# <a name="diskio_typegroup1-class"></a>\_Класс дискио TypeGroup1

Этот класс является классом типа событий для событий дискового ввода-вывода.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Участники

Класс **дискио \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **дискио \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Тип данных: **sint64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Смещение в байтах от начала физического диска.

</dd> <dt>

**дискнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Число, идентифицирующее физический диск.

</dd> <dt>

**Закрыт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (6), [**pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**FileIo \_ Name**](fileio-name.md) , чтобы определить файл, участвующий в операции ввода-вывода.

</dd> <dt>

**хигхресреспонсетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

Время между запуском и завершением операций ввода-вывода, измеряемое диспетчером секций (в единицах тактов [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003:** Это свойство имеет значение [**вмидатаид**](event-tracing-mof-qualifiers.md) , равное 7.

**Windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (7), [**pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Пакет запроса ввода-вывода, который определяет действие ввода-вывода.

**Windows server 2003, windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.

</dd> <dt>

**ирпфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Может содержать один или несколько из следующих флагов пакетов запроса ввода-вывода (определенных в файле Нтддк. h, который является файлом заголовка DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **\_НЕкэшированный IRP**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **IO IRP с \_ разбивкой на страницы \_**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **\_Завершение монтирования IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **\_синхронный \_ API IRP**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP, связанный с IRP \_**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **\_операции ввода-вывода в буфере IRP \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**\_БУФЕР освобождения IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_входная \_ Операция IRP**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **\_синхронный \_ Ввод-вывод на пейджер \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_операция создания \_ IRP**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_операция чтения \_ IRP**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_операция записи \_ IRP**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **\_операция закрытия \_ IRP**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **\_Завершение отложенного \_ ввода-вывода IRP \_**
</dt> </dl>

</dd> <dt>

**иссуингсреадид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

Идентификатор выдающего потока.

**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003, windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Зарезервировано.

**Windows server 2008 R2, Windows server 2008 и Windows 7:** Имя свойства — **куеуедепс**, которое содержит счетчик тактов ЦП от начала операции до конца операции. Обратите внимание, что это значение может быть переполнено.

Windows **Vista, Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003, windows 2000 Server и windows 2000 Professional:** Имя свойства — **соглашение**, которое содержит счетчик тактов ЦП от начала операции до конца операции. Обратите внимание, что это значение может быть переполнено.

</dd> <dt>

**трансферсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Размер данных, считываемых или записываемых с диска, в байтах.

</dd> </dl>

## <a name="remarks"></a>Примечания

Windows Server 2003 использует следующее определение для класса типа событий **дискио \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

Свойство **соглашение** содержит счетчик тактов ЦП от начала операции до конца операции. Обратите внимание, что это значение может быть переполнено.

Свойство **хигхресреспонсетиме** не поддерживается.

В Windows Server 2003 с пакетом обновления 1 (SP1) и Windows Vista используется следующее определение класса типа событий **дискио \_ TypeGroup1** .

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

Свойство **IRP** — это пакет запроса ввода-вывода. Это свойство идентифицирует действие ввода-вывода. Это свойство можно использовать с событиями [**дискио \_ TypeGroup2**](diskio-typegroup2.md) для корреляции времени ответа.

Свойство **хигхресреспонсетиме** поддерживается. Свойство содержит время между инициацией ввода-вывода и завершением, измеряемое Партитионманажер (в единицах Кекуериперформанцекаунтер). Используйте это свойство вместо свойства **соглашение** для определения времени ответа дискового ввода-вывода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дискио**](diskio.md)
</dt> </dl>

 

 
