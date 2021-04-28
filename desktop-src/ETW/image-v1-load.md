---
description: Image_V1_Load класс. Этот класс является классом типа события для событий загрузки изображения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Класс Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106502"
---
# <a name="image_v1_load-class"></a><span data-ttu-id="4f10a-104">Image \_ v1, \_ класс загрузки</span><span class="sxs-lookup"><span data-stu-id="4f10a-104">Image\_V1\_Load class</span></span>

<span data-ttu-id="4f10a-105">Этот класс является классом типа событий для событий загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="4f10a-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="4f10a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4f10a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f10a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f10a-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="4f10a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4f10a-108">Members</span></span>

<span data-ttu-id="4f10a-109">Класс **\_ \_ загрузки Image v1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4f10a-109">The **Image\_V1\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="4f10a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f10a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f10a-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="4f10a-111">Properties</span></span>

<span data-ttu-id="4f10a-112">Класс **\_ \_ загрузки Image v1** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="4f10a-112">The **Image\_V1\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f10a-113">FileName</span><span class="sxs-lookup"><span data-stu-id="4f10a-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f10a-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4f10a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f10a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-116">Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4f10a-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4f10a-117">Имя и расширение файла DLL или исполняемого образа для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4f10a-117">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="4f10a-118">ImageBase</span><span class="sxs-lookup"><span data-stu-id="4f10a-118">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f10a-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f10a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f10a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="4f10a-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4f10a-122">Базовый адрес приложения, в котором загружается образ.</span><span class="sxs-lookup"><span data-stu-id="4f10a-122">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4f10a-123">ImageSize</span><span class="sxs-lookup"><span data-stu-id="4f10a-123">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f10a-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f10a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f10a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-126">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="4f10a-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4f10a-127">Размер загружаемого образа.</span><span class="sxs-lookup"><span data-stu-id="4f10a-127">Size of the image being loaded.</span></span>

<span data-ttu-id="4f10a-128">При использовании этого свойства тип данных для этого свойства фактически имеет размер \_ t.</span><span class="sxs-lookup"><span data-stu-id="4f10a-128">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="4f10a-129">Квалификатор указателя используется, чтобы определить, равен ли размер \_ t 4-байтам или 8-байтам.</span><span class="sxs-lookup"><span data-stu-id="4f10a-129">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4f10a-130">ProcessId</span><span class="sxs-lookup"><span data-stu-id="4f10a-130">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f10a-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f10a-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4f10a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f10a-133">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="4f10a-133">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4f10a-134">Определяет процесс, в который загружается образ.</span><span class="sxs-lookup"><span data-stu-id="4f10a-134">Identifies the process into which the image is loaded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f10a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4f10a-135">Requirements</span></span>



| <span data-ttu-id="4f10a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4f10a-136">Requirement</span></span> | <span data-ttu-id="4f10a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4f10a-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f10a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f10a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4f10a-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f10a-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4f10a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f10a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4f10a-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f10a-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f10a-142">См. также</span><span class="sxs-lookup"><span data-stu-id="4f10a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f10a-143">**Образ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="4f10a-143">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




