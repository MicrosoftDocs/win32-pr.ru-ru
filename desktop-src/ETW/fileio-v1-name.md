---
description: Этот класс является классом типа события для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Класс FileIo_V1_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081081"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="78d51-104">\_ \_ Класс имен FileIo v1</span><span class="sxs-lookup"><span data-stu-id="78d51-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="78d51-105">Этот класс является классом типа события для событий файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="78d51-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="78d51-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="78d51-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78d51-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="78d51-108">Участники</span><span class="sxs-lookup"><span data-stu-id="78d51-108">Members</span></span>

<span data-ttu-id="78d51-109">Класс **\_ \_ имен FileIo v1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="78d51-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="78d51-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="78d51-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78d51-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="78d51-111">Properties</span></span>

<span data-ttu-id="78d51-112">Класс **\_ \_ имен FileIo v1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="78d51-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78d51-113">FileName</span><span class="sxs-lookup"><span data-stu-id="78d51-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78d51-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="78d51-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78d51-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78d51-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78d51-116">Квалификаторы: Вмидатаид (2), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="78d51-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="78d51-117">Полный путь к файлу, не включая букву диска.</span><span class="sxs-lookup"><span data-stu-id="78d51-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="78d51-118">Закрыт</span><span class="sxs-lookup"><span data-stu-id="78d51-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78d51-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78d51-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78d51-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="78d51-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78d51-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="78d51-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="78d51-122">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="78d51-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78d51-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="78d51-123">Remarks</span></span>

<span data-ttu-id="78d51-124">**Windows Server 2003:** Чтобы получить букву диска для пути к имени файла, используйте значение свойства **FileObject** для сопоставлений с соответствующим событием [ \_ TypeGroup1 дискио](diskio-typegroup1.md) .</span><span class="sxs-lookup"><span data-stu-id="78d51-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="78d51-125">В \_ событии дискио TypeGroup1 используйте значения свойств **Дискнумбер** и **ByteOffset** для сопоставления с соответствующим событием [системконфиг \_ логдиск](systemconfig-logdisk.md) (**ByteOffset** сопоставляется с **стартоффсет**).</span><span class="sxs-lookup"><span data-stu-id="78d51-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="78d51-126">Свойство **дривелеттерстринг** содержит букву диска.</span><span class="sxs-lookup"><span data-stu-id="78d51-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d51-127">Требования</span><span class="sxs-lookup"><span data-stu-id="78d51-127">Requirements</span></span>



| <span data-ttu-id="78d51-128">Требование</span><span class="sxs-lookup"><span data-stu-id="78d51-128">Requirement</span></span> | <span data-ttu-id="78d51-129">Значение</span><span class="sxs-lookup"><span data-stu-id="78d51-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78d51-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78d51-130">Minimum supported client</span></span><br/> | <span data-ttu-id="78d51-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78d51-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="78d51-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78d51-132">Minimum supported server</span></span><br/> | <span data-ttu-id="78d51-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78d51-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78d51-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78d51-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d51-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="78d51-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




