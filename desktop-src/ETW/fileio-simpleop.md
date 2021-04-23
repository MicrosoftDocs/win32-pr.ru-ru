---
description: Этот класс является классом типа события для простых событий файловых операций. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Класс FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985841"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="ce3a2-104">\_Класс FileIo симплеоп</span><span class="sxs-lookup"><span data-stu-id="ce3a2-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="ce3a2-105">Этот класс является классом типа события для простых событий файловых операций.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="ce3a2-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce3a2-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="ce3a2-108">Участники</span><span class="sxs-lookup"><span data-stu-id="ce3a2-108">Members</span></span>

<span data-ttu-id="ce3a2-109">Класс **FileIo \_ симплеоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ce3a2-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="ce3a2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce3a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce3a2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce3a2-111">Properties</span></span>

<span data-ttu-id="ce3a2-112">Класс **FileIo \_ симплеоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce3a2-113">**филекэй**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3a2-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce3a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-116">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="ce3a2-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ce3a2-117">Чтобы определить имя файла, сопоставьте значение этого свойства со свойством **FileObject** события [**FileIo \_ Name**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="ce3a2-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a2-118">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3a2-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce3a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-121">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="ce3a2-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ce3a2-122">Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a2-123">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3a2-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce3a2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-126">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="ce3a2-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ce3a2-127">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-127">IO request packet.</span></span> <span data-ttu-id="ce3a2-128">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a2-129">**ттид**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3a2-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce3a2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3a2-132">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="ce3a2-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ce3a2-133">Идентификатор потока, выполняющего операцию.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce3a2-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce3a2-134">Remarks</span></span>

<span data-ttu-id="ce3a2-135">Событие очистки регистрируется при закрытии последнего маркера файла.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="ce3a2-136">Событие закрытия указывает, что файловый объект освобождается.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="ce3a2-137">Событие Flush указывает, когда буферы файлов полностью сброшены на диск.</span><span class="sxs-lookup"><span data-stu-id="ce3a2-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3a2-138">Требования</span><span class="sxs-lookup"><span data-stu-id="ce3a2-138">Requirements</span></span>



| <span data-ttu-id="ce3a2-139">Требование</span><span class="sxs-lookup"><span data-stu-id="ce3a2-139">Requirement</span></span> | <span data-ttu-id="ce3a2-140">Значение</span><span class="sxs-lookup"><span data-stu-id="ce3a2-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce3a2-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce3a2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3a2-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce3a2-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce3a2-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce3a2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3a2-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce3a2-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce3a2-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce3a2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3a2-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="ce3a2-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




