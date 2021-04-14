---
description: Этот класс является классом типа события для события создания файла. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Класс FileIo_Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984492"
---
# <a name="fileio_create-class"></a><span data-ttu-id="91184-104">\_Класс FileIo CREATE</span><span class="sxs-lookup"><span data-stu-id="91184-104">FileIo\_Create class</span></span>

<span data-ttu-id="91184-105">Этот класс является классом типа события для события создания файла.</span><span class="sxs-lookup"><span data-stu-id="91184-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="91184-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="91184-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="91184-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91184-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="91184-108">Участники</span><span class="sxs-lookup"><span data-stu-id="91184-108">Members</span></span>

<span data-ttu-id="91184-109">Класс **FileIo \_ CREATE** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="91184-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="91184-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="91184-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91184-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="91184-111">Properties</span></span>

<span data-ttu-id="91184-112">Класс **FileIo \_ CREATE** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91184-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91184-113">**креатеоптионс**</span><span class="sxs-lookup"><span data-stu-id="91184-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-116">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="91184-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="91184-117">Значения, передаваемые в параметрах *креатеоптионс* и *креатедиспоситионс* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="91184-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="91184-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="91184-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-121">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="91184-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="91184-122">Значение, передаваемое в параметре *FileAttributes* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="91184-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="91184-123">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="91184-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-126">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="91184-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91184-127">Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="91184-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="91184-128">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="91184-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-131">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="91184-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91184-132">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="91184-132">IO request packet.</span></span> <span data-ttu-id="91184-133">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="91184-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="91184-134">**опенпас**</span><span class="sxs-lookup"><span data-stu-id="91184-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91184-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91184-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-137">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="91184-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="91184-138">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="91184-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="91184-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="91184-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-142">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="91184-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="91184-143">Значение, передаваемое в параметре *шареакцесс* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="91184-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="91184-144">**ттид**</span><span class="sxs-lookup"><span data-stu-id="91184-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91184-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91184-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91184-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91184-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91184-147">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="91184-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91184-148">Идентификатор потока, который создает файл.</span><span class="sxs-lookup"><span data-stu-id="91184-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91184-149">Требования</span><span class="sxs-lookup"><span data-stu-id="91184-149">Requirements</span></span>



| <span data-ttu-id="91184-150">Требование</span><span class="sxs-lookup"><span data-stu-id="91184-150">Requirement</span></span> | <span data-ttu-id="91184-151">Значение</span><span class="sxs-lookup"><span data-stu-id="91184-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91184-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91184-152">Minimum supported client</span></span><br/> | <span data-ttu-id="91184-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91184-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91184-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91184-154">Minimum supported server</span></span><br/> | <span data-ttu-id="91184-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91184-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91184-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91184-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91184-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="91184-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
