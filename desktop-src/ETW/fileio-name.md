---
description: FileIo_Name Class — этот класс является классом типа события для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: Класс FileIo_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9fabfbcfa318ad809b5cb2f66d72f19abf21112d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106592"
---
# <a name="fileio_name-class"></a><span data-ttu-id="9f903-104">\_Класс имен FileIo</span><span class="sxs-lookup"><span data-stu-id="9f903-104">FileIo\_Name class</span></span>

<span data-ttu-id="9f903-105">Этот класс является классом типа события для событий файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9f903-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="9f903-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9f903-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f903-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f903-107">Syntax</span></span>

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="9f903-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9f903-108">Members</span></span>

<span data-ttu-id="9f903-109">Класс **\_ имен FileIo** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9f903-109">The **FileIo\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="9f903-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f903-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f903-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="9f903-111">Properties</span></span>

<span data-ttu-id="9f903-112">Класс **\_ имен FileIo** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f903-112">The **FileIo\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f903-113">FileName</span><span class="sxs-lookup"><span data-stu-id="9f903-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f903-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f903-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f903-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f903-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f903-116">Квалификаторы: Вмидатаид (2), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="9f903-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9f903-117">Полный путь к файлу, не включая букву диска.</span><span class="sxs-lookup"><span data-stu-id="9f903-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="9f903-118">Закрыт</span><span class="sxs-lookup"><span data-stu-id="9f903-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f903-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f903-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f903-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f903-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f903-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="9f903-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f903-122">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9f903-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f903-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="9f903-123">Remarks</span></span>

<span data-ttu-id="9f903-124">**Windows Server 2003:** Чтобы получить букву диска для пути к имени файла, используйте значение свойства **FileObject** для сопоставлений с соответствующим событием [ \_ TypeGroup1 дискио](diskio-typegroup1.md) .</span><span class="sxs-lookup"><span data-stu-id="9f903-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="9f903-125">В \_ событии дискио TypeGroup1 используйте значения свойств **Дискнумбер** и **ByteOffset** для сопоставления с соответствующим событием [системконфиг \_ логдиск](systemconfig-logdisk.md) (**ByteOffset** сопоставляется с **стартоффсет**).</span><span class="sxs-lookup"><span data-stu-id="9f903-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="9f903-126">Свойство **дривелеттерстринг** содержит букву диска.</span><span class="sxs-lookup"><span data-stu-id="9f903-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f903-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9f903-127">Requirements</span></span>



| <span data-ttu-id="9f903-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9f903-128">Requirement</span></span> | <span data-ttu-id="9f903-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9f903-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f903-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f903-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9f903-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f903-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f903-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f903-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9f903-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f903-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f903-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9f903-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f903-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="9f903-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




