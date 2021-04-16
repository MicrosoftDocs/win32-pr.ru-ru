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
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="4b40f-104">\_Класс дискио TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="4b40f-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="4b40f-105">Этот класс является классом типа событий для событий дискового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="4b40f-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b40f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b40f-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4b40f-108">Участники</span><span class="sxs-lookup"><span data-stu-id="4b40f-108">Members</span></span>

<span data-ttu-id="4b40f-109">Класс **дискио \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b40f-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4b40f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b40f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b40f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b40f-111">Properties</span></span>

<span data-ttu-id="4b40f-112">Класс **дискио \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b40f-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b40f-113">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="4b40f-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-114">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4b40f-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-116">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="4b40f-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-117">Смещение в байтах от начала физического диска.</span><span class="sxs-lookup"><span data-stu-id="4b40f-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-118">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="4b40f-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-121">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="4b40f-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-122">Число, идентифицирующее физический диск.</span><span class="sxs-lookup"><span data-stu-id="4b40f-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-123">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="4b40f-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-126">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (6), [**pointer**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4b40f-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-127">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**FileIo \_ Name**](fileio-name.md) , чтобы определить файл, участвующий в операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-128">**хигхресреспонсетиме**</span><span class="sxs-lookup"><span data-stu-id="4b40f-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4b40f-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-131">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="4b40f-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-132">Время между запуском и завершением операций ввода-вывода, измеряемое диспетчером секций (в единицах тактов [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="4b40f-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="4b40f-133">**Windows Server 2003:** Это свойство имеет значение [**вмидатаид**](event-tracing-mof-qualifiers.md) , равное 7.</span><span class="sxs-lookup"><span data-stu-id="4b40f-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="4b40f-134">**Windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b40f-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-135">**IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-136">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-138">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (7), [**pointer**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4b40f-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-139">Пакет запроса ввода-вывода, который определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="4b40f-140">**Windows server 2003, windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b40f-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-141">**ирпфлагс**</span><span class="sxs-lookup"><span data-stu-id="4b40f-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-144">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="4b40f-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-145">Может содержать один или несколько из следующих флагов пакетов запроса ввода-вывода (определенных в файле Нтддк. h, который является файлом заголовка DDK):</span><span class="sxs-lookup"><span data-stu-id="4b40f-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="4b40f-146">**\_НЕкэшированный IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="4b40f-147">**IO IRP с \_ разбивкой на страницы \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="4b40f-148">**\_Завершение монтирования IRP \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="4b40f-149">**\_синхронный \_ API IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="4b40f-150">**\_IRP, связанный с IRP \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="4b40f-151">**\_операции ввода-вывода в буфере IRP \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="4b40f-152">**\_БУФЕР освобождения IRP \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="4b40f-153">**\_входная \_ Операция IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="4b40f-154">**\_синхронный \_ Ввод-вывод на пейджер \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="4b40f-155">**\_операция создания \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="4b40f-156">**\_операция чтения \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="4b40f-157">**\_операция записи \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="4b40f-158">**\_операция закрытия \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="4b40f-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="4b40f-159">**\_Завершение отложенного \_ ввода-вывода IRP \_**</span><span class="sxs-lookup"><span data-stu-id="4b40f-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b40f-160">**иссуингсреадид**</span><span class="sxs-lookup"><span data-stu-id="4b40f-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-163">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="4b40f-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-164">Идентификатор выдающего потока.</span><span class="sxs-lookup"><span data-stu-id="4b40f-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="4b40f-165">**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003, windows 2000 Server и windows 2000 Professional:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b40f-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="4b40f-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-169">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="4b40f-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-170">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="4b40f-170">Reserved.</span></span>

<span data-ttu-id="4b40f-171">**Windows server 2008 R2, Windows server 2008 и Windows 7:** Имя свойства — **куеуедепс**, которое содержит счетчик тактов ЦП от начала операции до конца операции.</span><span class="sxs-lookup"><span data-stu-id="4b40f-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4b40f-172">Обратите внимание, что это значение может быть переполнено.</span><span class="sxs-lookup"><span data-stu-id="4b40f-172">Note that this value can overflow.</span></span>

<span data-ttu-id="4b40f-173">Windows **Vista, Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003, windows 2000 Server и windows 2000 Professional:** Имя свойства — **соглашение**, которое содержит счетчик тактов ЦП от начала операции до конца операции.</span><span class="sxs-lookup"><span data-stu-id="4b40f-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4b40f-174">Обратите внимание, что это значение может быть переполнено.</span><span class="sxs-lookup"><span data-stu-id="4b40f-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="4b40f-175">**трансферсизе**</span><span class="sxs-lookup"><span data-stu-id="4b40f-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b40f-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b40f-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b40f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b40f-178">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="4b40f-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="4b40f-179">Размер данных, считываемых или записываемых с диска, в байтах.</span><span class="sxs-lookup"><span data-stu-id="4b40f-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b40f-180">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b40f-180">Remarks</span></span>

<span data-ttu-id="4b40f-181">Windows Server 2003 использует следующее определение для класса типа событий **дискио \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="4b40f-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="4b40f-182">Свойство **соглашение** содержит счетчик тактов ЦП от начала операции до конца операции.</span><span class="sxs-lookup"><span data-stu-id="4b40f-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4b40f-183">Обратите внимание, что это значение может быть переполнено.</span><span class="sxs-lookup"><span data-stu-id="4b40f-183">Note that this value can overflow.</span></span>

<span data-ttu-id="4b40f-184">Свойство **хигхресреспонсетиме** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b40f-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="4b40f-185">В Windows Server 2003 с пакетом обновления 1 (SP1) и Windows Vista используется следующее определение класса типа событий **дискио \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="4b40f-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="4b40f-186">Свойство **IRP** — это пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="4b40f-187">Это свойство идентифицирует действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="4b40f-188">Это свойство можно использовать с событиями [**дискио \_ TypeGroup2**](diskio-typegroup2.md) для корреляции времени ответа.</span><span class="sxs-lookup"><span data-stu-id="4b40f-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="4b40f-189">Свойство **хигхресреспонсетиме** поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b40f-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="4b40f-190">Свойство содержит время между инициацией ввода-вывода и завершением, измеряемое Партитионманажер (в единицах Кекуериперформанцекаунтер).</span><span class="sxs-lookup"><span data-stu-id="4b40f-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="4b40f-191">Используйте это свойство вместо свойства **соглашение** для определения времени ответа дискового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="4b40f-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b40f-192">Требования</span><span class="sxs-lookup"><span data-stu-id="4b40f-192">Requirements</span></span>



| <span data-ttu-id="4b40f-193">Требование</span><span class="sxs-lookup"><span data-stu-id="4b40f-193">Requirement</span></span> | <span data-ttu-id="4b40f-194">Значение</span><span class="sxs-lookup"><span data-stu-id="4b40f-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4b40f-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b40f-195">Minimum supported client</span></span><br/> | <span data-ttu-id="4b40f-196">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b40f-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b40f-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b40f-197">Minimum supported server</span></span><br/> | <span data-ttu-id="4b40f-198">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b40f-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4b40f-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b40f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b40f-200">**дискио**</span><span class="sxs-lookup"><span data-stu-id="4b40f-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
