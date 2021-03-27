---
description: Этот класс является классом типа событий для событий неисправностей страниц. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Класс PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998834"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="ab0fa-104">\_Класс PageFault хардфаулт</span><span class="sxs-lookup"><span data-stu-id="ab0fa-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="ab0fa-105">Этот класс является классом типа событий для событий неисправностей страниц.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="ab0fa-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab0fa-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="ab0fa-108">Участники</span><span class="sxs-lookup"><span data-stu-id="ab0fa-108">Members</span></span>

<span data-ttu-id="ab0fa-109">Класс **PageFault \_ хардфаулт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab0fa-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="ab0fa-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab0fa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab0fa-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab0fa-111">Properties</span></span>

<span data-ttu-id="ab0fa-112">Класс **PageFault \_ хардфаулт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab0fa-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-116">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="ab0fa-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-117">Объем данных, считанных из Реадоффсет для удовлетворения сбоя.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="ab0fa-118">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-121">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="ab0fa-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-122">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**FileIo \_ Name**](fileio-name.md) , чтобы определить имя файла.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="ab0fa-123">**инитиалтиме**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-126">Квалификаторы: Вмидатаид (1), Extension ("Вмитиме")</span><span class="sxs-lookup"><span data-stu-id="ab0fa-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-127">Отметка времени начала, на которой произошла ошибка страницы.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ab0fa-128">**реадоффсет**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-131">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="ab0fa-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-132">Смещение файла, из которого считываются данные для удовлетворения ошибки.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="ab0fa-133">**тсреадид**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-136">Квалификаторы: Вмидатаид (5), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="ab0fa-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-137">Идентификатор потока, в котором произошла ошибка страницы.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="ab0fa-138">**виртуаладдресс**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab0fa-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab0fa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab0fa-141">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="ab0fa-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ab0fa-142">Адрес сбоя.</span><span class="sxs-lookup"><span data-stu-id="ab0fa-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab0fa-143">Требования</span><span class="sxs-lookup"><span data-stu-id="ab0fa-143">Requirements</span></span>



| <span data-ttu-id="ab0fa-144">Требование</span><span class="sxs-lookup"><span data-stu-id="ab0fa-144">Requirement</span></span> | <span data-ttu-id="ab0fa-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ab0fa-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab0fa-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab0fa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0fa-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab0fa-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab0fa-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab0fa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0fa-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab0fa-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab0fa-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab0fa-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0fa-151">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="ab0fa-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




