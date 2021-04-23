---
description: Этот класс является классом типа событий для событий чтения и записи файлов. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: Класс FileIo_ReadWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985844"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="138dc-104">\_Класс FileIo ReadWrite</span><span class="sxs-lookup"><span data-stu-id="138dc-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="138dc-105">Этот класс является классом типа событий для событий чтения и записи файлов.</span><span class="sxs-lookup"><span data-stu-id="138dc-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="138dc-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="138dc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="138dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="138dc-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="138dc-108">Участники</span><span class="sxs-lookup"><span data-stu-id="138dc-108">Members</span></span>

<span data-ttu-id="138dc-109">Класс **FileIo \_ ReadWrite** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="138dc-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="138dc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="138dc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="138dc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="138dc-111">Properties</span></span>

<span data-ttu-id="138dc-112">Класс **FileIo \_ ReadWrite** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="138dc-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="138dc-113">**филекэй**</span><span class="sxs-lookup"><span data-stu-id="138dc-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-116">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="138dc-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="138dc-117">Чтобы определить имя файла, сопоставьте значение этого свойства со свойством **FileObject** события [**FileIo \_ Name**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="138dc-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-118">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="138dc-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-121">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="138dc-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="138dc-122">Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="138dc-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-123">**иофлагс**</span><span class="sxs-lookup"><span data-stu-id="138dc-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-126">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="138dc-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="138dc-127">Флаги пакета запроса ввода-вывода, указанные для этой операции.</span><span class="sxs-lookup"><span data-stu-id="138dc-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-128">**иосизе**</span><span class="sxs-lookup"><span data-stu-id="138dc-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-131">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="138dc-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="138dc-132">Число запрошенных байтов.</span><span class="sxs-lookup"><span data-stu-id="138dc-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-133">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="138dc-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-136">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="138dc-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="138dc-137">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="138dc-137">IO request packet.</span></span> <span data-ttu-id="138dc-138">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="138dc-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="138dc-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-140">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="138dc-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-142">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="138dc-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="138dc-143">Начальное смещение файла для запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="138dc-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="138dc-144">**ттид**</span><span class="sxs-lookup"><span data-stu-id="138dc-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dc-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="138dc-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="138dc-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="138dc-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dc-147">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="138dc-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="138dc-148">Идентификатор потока, выполняющего операцию.</span><span class="sxs-lookup"><span data-stu-id="138dc-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="138dc-149">Требования</span><span class="sxs-lookup"><span data-stu-id="138dc-149">Requirements</span></span>



| <span data-ttu-id="138dc-150">Требование</span><span class="sxs-lookup"><span data-stu-id="138dc-150">Requirement</span></span> | <span data-ttu-id="138dc-151">Значение</span><span class="sxs-lookup"><span data-stu-id="138dc-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="138dc-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="138dc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="138dc-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="138dc-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="138dc-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="138dc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="138dc-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="138dc-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="138dc-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="138dc-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138dc-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="138dc-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




