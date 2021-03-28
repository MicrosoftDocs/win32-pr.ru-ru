---
description: Этот класс является классом типа событий для событий перечисления каталога и уведомления каталога. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: Класс FileIo_DirEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984489"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="52469-104">\_Класс FileIo диренум</span><span class="sxs-lookup"><span data-stu-id="52469-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="52469-105">Этот класс является классом типа событий для событий перечисления каталога и уведомления каталога.</span><span class="sxs-lookup"><span data-stu-id="52469-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="52469-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="52469-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52469-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52469-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="52469-108">Участники</span><span class="sxs-lookup"><span data-stu-id="52469-108">Members</span></span>

<span data-ttu-id="52469-109">Класс **FileIo \_ диренум** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="52469-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="52469-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="52469-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52469-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="52469-111">Properties</span></span>

<span data-ttu-id="52469-112">Класс **FileIo \_ диренум** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52469-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52469-113">**филеиндекс**</span><span class="sxs-lookup"><span data-stu-id="52469-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-116">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="52469-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="52469-117">Индекс файла, из которого необходимо продолжить перечисление каталогов.</span><span class="sxs-lookup"><span data-stu-id="52469-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="52469-118">**филекэй**</span><span class="sxs-lookup"><span data-stu-id="52469-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-121">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="52469-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="52469-122">Чтобы определить имя каталога, сопоставьте значение этого свойства свойству **FileObject** события [**FileIo \_ Name**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="52469-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="52469-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="52469-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="52469-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52469-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-126">Квалификаторы: Вмидатаид (8), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="52469-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="52469-127">Шаблон, указанный для перечисления каталогов.</span><span class="sxs-lookup"><span data-stu-id="52469-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="52469-128">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="52469-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-131">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="52469-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="52469-132">Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.</span><span class="sxs-lookup"><span data-stu-id="52469-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="52469-133">**инфокласс**</span><span class="sxs-lookup"><span data-stu-id="52469-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-136">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="52469-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="52469-137">Запрошенный класс сведений о перечислении каталога.</span><span class="sxs-lookup"><span data-stu-id="52469-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="52469-138">**ирпптр**</span><span class="sxs-lookup"><span data-stu-id="52469-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-141">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="52469-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="52469-142">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="52469-142">IO request packet.</span></span> <span data-ttu-id="52469-143">Это свойство определяет действие ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="52469-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="52469-144">**Длина**</span><span class="sxs-lookup"><span data-stu-id="52469-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-147">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="52469-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="52469-148">Размер буфера запроса в байтах.</span><span class="sxs-lookup"><span data-stu-id="52469-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="52469-149">**ттид**</span><span class="sxs-lookup"><span data-stu-id="52469-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52469-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52469-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52469-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="52469-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52469-152">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="52469-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="52469-153">Идентификатор потока, выполняющего операцию.</span><span class="sxs-lookup"><span data-stu-id="52469-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52469-154">Примечания</span><span class="sxs-lookup"><span data-stu-id="52469-154">Remarks</span></span>

<span data-ttu-id="52469-155">События перечисления каталогов и уведомления каталога записываются при перечислении каталога или при отправке уведомлений об изменении каталога в зарегистрированные прослушиватели соответственно.</span><span class="sxs-lookup"><span data-stu-id="52469-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="52469-156">Требования</span><span class="sxs-lookup"><span data-stu-id="52469-156">Requirements</span></span>



| <span data-ttu-id="52469-157">Требование</span><span class="sxs-lookup"><span data-stu-id="52469-157">Requirement</span></span> | <span data-ttu-id="52469-158">Значение</span><span class="sxs-lookup"><span data-stu-id="52469-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52469-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52469-159">Minimum supported client</span></span><br/> | <span data-ttu-id="52469-160">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52469-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52469-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52469-161">Minimum supported server</span></span><br/> | <span data-ttu-id="52469-162">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52469-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52469-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52469-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52469-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="52469-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




