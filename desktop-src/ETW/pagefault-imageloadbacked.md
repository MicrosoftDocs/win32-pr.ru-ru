---
description: Этот класс является классом типа события для загрузки изображения в событиях файла подкачки. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Класс PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985704"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="538a5-104">\_Класс PageFault имажелоадбаккед</span><span class="sxs-lookup"><span data-stu-id="538a5-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="538a5-105">Этот класс является классом типа события для загрузки изображения в событиях файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="538a5-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="538a5-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="538a5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="538a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="538a5-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="538a5-108">Участники</span><span class="sxs-lookup"><span data-stu-id="538a5-108">Members</span></span>

<span data-ttu-id="538a5-109">Класс **PageFault \_ имажелоадбаккед** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="538a5-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="538a5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="538a5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="538a5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="538a5-111">Properties</span></span>

<span data-ttu-id="538a5-112">Класс **PageFault \_ имажелоадбаккед** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="538a5-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="538a5-113">**девицечар**</span><span class="sxs-lookup"><span data-stu-id="538a5-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538a5-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="538a5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="538a5-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="538a5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="538a5-116">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="538a5-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="538a5-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="538a5-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="538a5-118">**филечар**</span><span class="sxs-lookup"><span data-stu-id="538a5-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538a5-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="538a5-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="538a5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="538a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="538a5-121">Квалификаторы: Вмидатаид (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="538a5-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="538a5-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="538a5-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="538a5-123">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="538a5-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538a5-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="538a5-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="538a5-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="538a5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="538a5-126">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="538a5-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="538a5-127">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**FileIo \_ Name**](fileio-name.md) , чтобы определить имя файла.</span><span class="sxs-lookup"><span data-stu-id="538a5-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="538a5-128">**лоадфлагс**</span><span class="sxs-lookup"><span data-stu-id="538a5-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="538a5-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="538a5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="538a5-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="538a5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="538a5-131">Квалификаторы: Вмидатаид (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="538a5-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="538a5-132">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="538a5-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="538a5-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="538a5-133">Remarks</span></span>

<span data-ttu-id="538a5-134">Событие регистрируется во время создания раздела образа (например, загрузка DLL), когда диспетчер памяти определяет, что образ необходимо скопировать в файл подкачки и запустить из него.</span><span class="sxs-lookup"><span data-stu-id="538a5-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="538a5-135">Как правило, образы запускаются из исходного файла, но резервное копирование может произойти, когда диспетчер памяти определяет, что исходный файл может быть изменен асинхронно существующими модулями записи или когда исходный файл находится на съемном носителе или удаленном устройстве.</span><span class="sxs-lookup"><span data-stu-id="538a5-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="538a5-136">Требования</span><span class="sxs-lookup"><span data-stu-id="538a5-136">Requirements</span></span>



| <span data-ttu-id="538a5-137">Требование</span><span class="sxs-lookup"><span data-stu-id="538a5-137">Requirement</span></span> | <span data-ttu-id="538a5-138">Значение</span><span class="sxs-lookup"><span data-stu-id="538a5-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="538a5-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="538a5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="538a5-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="538a5-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="538a5-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="538a5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="538a5-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="538a5-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="538a5-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="538a5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538a5-144">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="538a5-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




