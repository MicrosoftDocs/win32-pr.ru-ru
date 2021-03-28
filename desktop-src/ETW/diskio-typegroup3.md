---
description: Этот класс является классом типа событий для событий очистки дискового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: Класс DiskIo_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984233"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="163db-104">\_Класс дискио TypeGroup3</span><span class="sxs-lookup"><span data-stu-id="163db-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="163db-105">Этот класс является классом типа событий для событий очистки дискового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="163db-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="163db-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="163db-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="163db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="163db-107">Syntax</span></span>

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="163db-108">Участники</span><span class="sxs-lookup"><span data-stu-id="163db-108">Members</span></span>

<span data-ttu-id="163db-109">Класс **дискио \_ TypeGroup3** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="163db-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="163db-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="163db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="163db-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="163db-111">Properties</span></span>

<span data-ttu-id="163db-112">Класс **дискио \_ TypeGroup3** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="163db-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="163db-113">**дискнумбер**</span><span class="sxs-lookup"><span data-stu-id="163db-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="163db-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="163db-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="163db-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="163db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="163db-116">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="163db-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="163db-117">Число, идентифицирующее физический диск.</span><span class="sxs-lookup"><span data-stu-id="163db-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="163db-118">**хигхресреспонсетиме**</span><span class="sxs-lookup"><span data-stu-id="163db-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="163db-119">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="163db-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="163db-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="163db-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="163db-121">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="163db-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="163db-122">Количество тактов ЦП от начала операции до конца операции.</span><span class="sxs-lookup"><span data-stu-id="163db-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="163db-123">**IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="163db-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="163db-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="163db-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="163db-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="163db-126">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (4), [**pointer**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="163db-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="163db-127">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="163db-127">I/O request packet.</span></span> <span data-ttu-id="163db-128">Это свойство идентифицирует действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="163db-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="163db-129">**ирпфлагс**</span><span class="sxs-lookup"><span data-stu-id="163db-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="163db-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="163db-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="163db-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="163db-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="163db-132">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="163db-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="163db-133">Может содержать один или несколько из следующих флагов пакетов запроса ввода-вывода (определенных в файле Нтддк. h, который является файлом заголовка DDK):</span><span class="sxs-lookup"><span data-stu-id="163db-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="163db-134">**\_НЕкэшированный IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="163db-135">**IO IRP с \_ разбивкой на страницы \_**</span><span class="sxs-lookup"><span data-stu-id="163db-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="163db-136">**\_Завершение монтирования IRP \_**</span><span class="sxs-lookup"><span data-stu-id="163db-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="163db-137">**\_синхронный \_ API IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="163db-138">**\_IRP, связанный с IRP \_**</span><span class="sxs-lookup"><span data-stu-id="163db-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="163db-139">**\_операции ввода-вывода в буфере IRP \_**</span><span class="sxs-lookup"><span data-stu-id="163db-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="163db-140">**\_БУФЕР освобождения IRP \_**</span><span class="sxs-lookup"><span data-stu-id="163db-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="163db-141">**\_входная \_ Операция IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="163db-142">**\_синхронный \_ Ввод-вывод на пейджер \_**</span><span class="sxs-lookup"><span data-stu-id="163db-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="163db-143">**\_операция создания \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="163db-144">**\_операция чтения \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="163db-145">**\_операция записи \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="163db-146">**\_операция закрытия \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="163db-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="163db-147">**\_Завершение отложенного \_ ввода-вывода IRP \_**</span><span class="sxs-lookup"><span data-stu-id="163db-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="163db-148">**иссуингсреадид**</span><span class="sxs-lookup"><span data-stu-id="163db-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="163db-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="163db-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="163db-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="163db-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="163db-151">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="163db-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="163db-152">Идентификатор выдающего потока.</span><span class="sxs-lookup"><span data-stu-id="163db-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="163db-153">**Windows server 2008 R2, Windows server 2008, Windows 7 и Windows Vista:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="163db-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="163db-154">Требования</span><span class="sxs-lookup"><span data-stu-id="163db-154">Requirements</span></span>



| <span data-ttu-id="163db-155">Требование</span><span class="sxs-lookup"><span data-stu-id="163db-155">Requirement</span></span> | <span data-ttu-id="163db-156">Значение</span><span class="sxs-lookup"><span data-stu-id="163db-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="163db-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="163db-157">Minimum supported client</span></span><br/> | <span data-ttu-id="163db-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="163db-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="163db-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="163db-159">Minimum supported server</span></span><br/> | <span data-ttu-id="163db-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="163db-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="163db-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="163db-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="163db-162">**дискио**</span><span class="sxs-lookup"><span data-stu-id="163db-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




