---
description: Этот класс является классом типа событий для событий изображений. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Класс Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544895"
---
# <a name="image_load-class"></a><span data-ttu-id="a7edf-104">\_Класс загрузки Image</span><span class="sxs-lookup"><span data-stu-id="a7edf-104">Image\_Load class</span></span>

<span data-ttu-id="a7edf-105">Этот класс является классом типа событий для событий изображений.</span><span class="sxs-lookup"><span data-stu-id="a7edf-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="a7edf-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a7edf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7edf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7edf-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="a7edf-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a7edf-108">Members</span></span>

<span data-ttu-id="a7edf-109">Класс **\_ загрузки Image** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a7edf-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="a7edf-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7edf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7edf-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7edf-111">Properties</span></span>

<span data-ttu-id="a7edf-112">Класс **\_ загрузки Image** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a7edf-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7edf-113">дефаултбасе</span><span class="sxs-lookup"><span data-stu-id="a7edf-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-116">Квалификаторы: Вмидатаид (7), Pointer</span><span class="sxs-lookup"><span data-stu-id="a7edf-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-117">Базовый адрес по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7edf-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-118">FileName</span><span class="sxs-lookup"><span data-stu-id="a7edf-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a7edf-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-121">Квалификаторы: Вмидатаид (12), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="a7edf-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-122">Имя файла и расширение библиотеки DLL или исполняемого образа.</span><span class="sxs-lookup"><span data-stu-id="a7edf-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-123">ImageBase</span><span class="sxs-lookup"><span data-stu-id="a7edf-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-126">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="a7edf-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-127">Базовый адрес приложения, в котором загружается образ.</span><span class="sxs-lookup"><span data-stu-id="a7edf-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-128">имажечекксум</span><span class="sxs-lookup"><span data-stu-id="a7edf-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-131">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="a7edf-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-132">Контрольная сумма для образа.</span><span class="sxs-lookup"><span data-stu-id="a7edf-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="a7edf-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-136">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="a7edf-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-137">Размер загружаемого образа.</span><span class="sxs-lookup"><span data-stu-id="a7edf-137">Size of the image being loaded.</span></span>

<span data-ttu-id="a7edf-138">При использовании этого свойства тип данных для этого свойства фактически имеет размер \_ t.</span><span class="sxs-lookup"><span data-stu-id="a7edf-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="a7edf-139">Квалификатор указателя используется, чтобы определить, равен ли размер \_ t 4-байтам или 8-байтам.</span><span class="sxs-lookup"><span data-stu-id="a7edf-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="a7edf-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-143">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="a7edf-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-144">Определяет процесс, в который загружается образ.</span><span class="sxs-lookup"><span data-stu-id="a7edf-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="a7edf-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-148">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="a7edf-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-149">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a7edf-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="a7edf-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-153">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="a7edf-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-154">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a7edf-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="a7edf-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-158">Квалификаторы: Вмидатаид (9)</span><span class="sxs-lookup"><span data-stu-id="a7edf-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-159">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a7edf-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="a7edf-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-163">Квалификаторы: Вмидатаид (10)</span><span class="sxs-lookup"><span data-stu-id="a7edf-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-164">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a7edf-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="a7edf-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-168">Квалификаторы: Вмидатаид (11)</span><span class="sxs-lookup"><span data-stu-id="a7edf-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-169">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="a7edf-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7edf-170">тимедатестамп</span><span class="sxs-lookup"><span data-stu-id="a7edf-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7edf-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7edf-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7edf-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7edf-173">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="a7edf-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a7edf-174">Время и Дата загрузки или выгрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="a7edf-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7edf-175">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7edf-175">Remarks</span></span>

<span data-ttu-id="a7edf-176">События Дкстарт и Дценд перечисляют все загруженные изображения в начале и в конце трассировки соответственно.</span><span class="sxs-lookup"><span data-stu-id="a7edf-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7edf-177">Требования</span><span class="sxs-lookup"><span data-stu-id="a7edf-177">Requirements</span></span>



| <span data-ttu-id="a7edf-178">Требование</span><span class="sxs-lookup"><span data-stu-id="a7edf-178">Requirement</span></span> | <span data-ttu-id="a7edf-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a7edf-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7edf-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7edf-180">Minimum supported client</span></span><br/> | <span data-ttu-id="a7edf-181">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7edf-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7edf-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7edf-182">Minimum supported server</span></span><br/> | <span data-ttu-id="a7edf-183">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7edf-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7edf-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7edf-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7edf-185">**Образ —**</span><span class="sxs-lookup"><span data-stu-id="a7edf-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="a7edf-186">**\_V0 изображения**</span><span class="sxs-lookup"><span data-stu-id="a7edf-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="a7edf-187">**Образ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a7edf-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




