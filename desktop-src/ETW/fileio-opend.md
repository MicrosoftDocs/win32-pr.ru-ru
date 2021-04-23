---
description: Этот класс является классом типа события для событий конца файловой операции. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Класс FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816264"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="3ae56-104">FileIo \_ открытый класс</span><span class="sxs-lookup"><span data-stu-id="3ae56-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="3ae56-105">Этот класс является классом типа события для событий конца файловой операции.</span><span class="sxs-lookup"><span data-stu-id="3ae56-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="3ae56-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="3ae56-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ae56-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="3ae56-108">Участники</span><span class="sxs-lookup"><span data-stu-id="3ae56-108">Members</span></span>

<span data-ttu-id="3ae56-109">**\_ Открытый класс FileIo** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3ae56-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="3ae56-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ae56-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ae56-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ae56-111">Properties</span></span>

<span data-ttu-id="3ae56-112">**\_ Открытый класс FileIo** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ae56-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ae56-113">**екстраинфо**</span><span class="sxs-lookup"><span data-stu-id="3ae56-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae56-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae56-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ae56-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="3ae56-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3ae56-117">Дополнительные сведения, возвращаемые файловой системой для операции.</span><span class="sxs-lookup"><span data-stu-id="3ae56-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="3ae56-118">Например, для запроса на чтение — фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="3ae56-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="3ae56-119">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="3ae56-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae56-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae56-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ae56-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-122">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="3ae56-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3ae56-123">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="3ae56-123">IO request packet.</span></span> <span data-ttu-id="3ae56-124">Это свойство определяет завершающее действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="3ae56-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="3ae56-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae56-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae56-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae56-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3ae56-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae56-128">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="3ae56-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="3ae56-129">Возвращаемое значение из операции.</span><span class="sxs-lookup"><span data-stu-id="3ae56-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ae56-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ae56-130">Remarks</span></span>

<span data-ttu-id="3ae56-131">События [**FileIo**](fileio.md) регистрируются в начале операции.</span><span class="sxs-lookup"><span data-stu-id="3ae56-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="3ae56-132">Открытые события можно включить отдельно, чтобы указать конец этих операций.</span><span class="sxs-lookup"><span data-stu-id="3ae56-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="3ae56-133">IRP можно использовать для сопоставления событий начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="3ae56-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae56-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3ae56-134">Requirements</span></span>



| <span data-ttu-id="3ae56-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3ae56-135">Requirement</span></span> | <span data-ttu-id="3ae56-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae56-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ae56-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ae56-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae56-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ae56-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ae56-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ae56-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae56-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ae56-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ae56-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ae56-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae56-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="3ae56-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




