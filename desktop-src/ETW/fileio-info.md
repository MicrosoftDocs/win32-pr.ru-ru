---
description: Этот класс является классом типа события для события сведений о файле. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Класс FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985845"
---
# <a name="fileio_info-class"></a><span data-ttu-id="a3a89-104">\_Класс сведений FileIo</span><span class="sxs-lookup"><span data-stu-id="a3a89-104">FileIo\_Info class</span></span>

<span data-ttu-id="a3a89-105">Этот класс является классом типа события для события сведений о файле.</span><span class="sxs-lookup"><span data-stu-id="a3a89-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="a3a89-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a3a89-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a89-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a89-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="a3a89-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a3a89-108">Members</span></span>

<span data-ttu-id="a3a89-109">Класс **\_ сведений FileIo** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a3a89-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="a3a89-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a3a89-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3a89-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a3a89-111">Properties</span></span>

<span data-ttu-id="a3a89-112">Класс **\_ сведений FileIo** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a3a89-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3a89-113">**екстраинфо**</span><span class="sxs-lookup"><span data-stu-id="a3a89-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-116">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="a3a89-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-117">Для запросов Филедиспоситионинформатион это поле содержит запрошенное расположение.</span><span class="sxs-lookup"><span data-stu-id="a3a89-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="a3a89-118">Для запросов Филиндоффилеинформатион и Филеаллокатионинформатион это поле содержит указанный размер файла.</span><span class="sxs-lookup"><span data-stu-id="a3a89-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="a3a89-119">**филекэй**</span><span class="sxs-lookup"><span data-stu-id="a3a89-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-122">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="a3a89-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-123">Чтобы определить имя файла, сопоставьте значение этого свойства со свойством **FileObject** события [**FileIo \_ Name**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a89-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="a3a89-124">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="a3a89-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-127">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="a3a89-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-128">Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="a3a89-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="a3a89-129">**инфокласс**</span><span class="sxs-lookup"><span data-stu-id="a3a89-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-132">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="a3a89-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-133">Запрошенный класс сведений о файле.</span><span class="sxs-lookup"><span data-stu-id="a3a89-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="a3a89-134">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="a3a89-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-137">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="a3a89-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-138">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a3a89-138">IO request packet.</span></span> <span data-ttu-id="a3a89-139">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a3a89-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="a3a89-140">**ттид**</span><span class="sxs-lookup"><span data-stu-id="a3a89-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3a89-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3a89-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a89-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3a89-143">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="a3a89-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3a89-144">Идентификатор потока, выполняющего операцию.</span><span class="sxs-lookup"><span data-stu-id="a3a89-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3a89-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3a89-145">Remarks</span></span>

<span data-ttu-id="a3a89-146">Задать сведения и события сведений о запросах указывают на то, что были заданы или запрошены атрибуты файла.</span><span class="sxs-lookup"><span data-stu-id="a3a89-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="a3a89-147">При выполнении команды ФСКТЛ регистрируется событие управления файловой системой (Фсконтрол).</span><span class="sxs-lookup"><span data-stu-id="a3a89-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a89-148">Требования</span><span class="sxs-lookup"><span data-stu-id="a3a89-148">Requirements</span></span>



| <span data-ttu-id="a3a89-149">Требование</span><span class="sxs-lookup"><span data-stu-id="a3a89-149">Requirement</span></span> | <span data-ttu-id="a3a89-150">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a89-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3a89-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3a89-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a89-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3a89-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a3a89-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3a89-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a89-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3a89-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3a89-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3a89-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a89-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="a3a89-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




