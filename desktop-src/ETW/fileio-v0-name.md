---
description: '\_ \_ Класс имен FileIo v0 является более старой версией класса типов событий для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Класс FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816257"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="8acc1-104">FileIo \_ v0 \_ имя класса</span><span class="sxs-lookup"><span data-stu-id="8acc1-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="8acc1-105">Класс **\_ \_ имен FileIo v0** является более старой версией класса типов событий для событий файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="8acc1-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="8acc1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="8acc1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8acc1-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="8acc1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="8acc1-108">Members</span></span>

<span data-ttu-id="8acc1-109">Класс **\_ \_ имен FileIo v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8acc1-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="8acc1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8acc1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8acc1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8acc1-111">Properties</span></span>

<span data-ttu-id="8acc1-112">Класс **FileIo \_ v0 \_ Name** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8acc1-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8acc1-113">FileName</span><span class="sxs-lookup"><span data-stu-id="8acc1-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8acc1-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8acc1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8acc1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8acc1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8acc1-116">Квалификаторы: Вмидатаид (2), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="8acc1-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="8acc1-117">Полный путь к файлу, не включая букву диска.</span><span class="sxs-lookup"><span data-stu-id="8acc1-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="8acc1-118">Закрыт</span><span class="sxs-lookup"><span data-stu-id="8acc1-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8acc1-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8acc1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8acc1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8acc1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8acc1-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="8acc1-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8acc1-122">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="8acc1-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8acc1-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="8acc1-123">Remarks</span></span>

<span data-ttu-id="8acc1-124">**Windows Server 2003:** Чтобы получить букву диска для пути к имени файла, используйте значение свойства **FileObject** для сопоставлений с соответствующим событием [**\_ TypeGroup1 дискио**](diskio-typegroup1.md) .</span><span class="sxs-lookup"><span data-stu-id="8acc1-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="8acc1-125">В событии **дискио \_ TypeGroup1** используйте значения свойств **дискнумбер** и **ByteOffset** для сопоставлений с соответствующим событием [**системконфиг \_ логдиск**](systemconfig-logdisk.md) .</span><span class="sxs-lookup"><span data-stu-id="8acc1-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="8acc1-126">Свойство **дривелеттерстринг** содержит букву диска.</span><span class="sxs-lookup"><span data-stu-id="8acc1-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acc1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8acc1-127">Requirements</span></span>



| <span data-ttu-id="8acc1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8acc1-128">Requirement</span></span> | <span data-ttu-id="8acc1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8acc1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8acc1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8acc1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8acc1-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8acc1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8acc1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8acc1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8acc1-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8acc1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8acc1-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8acc1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acc1-135">**FileIo \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8acc1-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




