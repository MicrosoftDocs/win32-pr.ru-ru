---
description: Этот класс является классом типа события, который помечает начало событий чтения, записи и очистки диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Класс DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540375"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="503f6-104">\_Класс дискио TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="503f6-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="503f6-105">Этот класс является классом типа события, который помечает начало событий чтения, записи и очистки диска.</span><span class="sxs-lookup"><span data-stu-id="503f6-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="503f6-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="503f6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="503f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="503f6-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="503f6-108">Участники</span><span class="sxs-lookup"><span data-stu-id="503f6-108">Members</span></span>

<span data-ttu-id="503f6-109">Класс **дискио \_ TypeGroup2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="503f6-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="503f6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="503f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="503f6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="503f6-111">Properties</span></span>

<span data-ttu-id="503f6-112">Класс **дискио \_ TypeGroup2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="503f6-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="503f6-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="503f6-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503f6-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="503f6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="503f6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="503f6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="503f6-116">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1), [**pointer**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="503f6-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="503f6-117">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="503f6-117">I/O request packet.</span></span> <span data-ttu-id="503f6-118">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="503f6-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="503f6-119">**иссуингсреадид**</span><span class="sxs-lookup"><span data-stu-id="503f6-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503f6-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="503f6-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="503f6-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="503f6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="503f6-122">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="503f6-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="503f6-123">Идентификатор выдающего потока.</span><span class="sxs-lookup"><span data-stu-id="503f6-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="503f6-124">**Windows server 2008 R2, Windows server 2008, Windows 7 и Windows Vista:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="503f6-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="503f6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="503f6-125">Requirements</span></span>



| <span data-ttu-id="503f6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="503f6-126">Requirement</span></span> | <span data-ttu-id="503f6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="503f6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="503f6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="503f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="503f6-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="503f6-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="503f6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="503f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="503f6-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="503f6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="503f6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="503f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503f6-133">**дискио**</span><span class="sxs-lookup"><span data-stu-id="503f6-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




