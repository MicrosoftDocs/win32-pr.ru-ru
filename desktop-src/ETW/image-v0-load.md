---
description: Этот класс является классом типа событий для событий загрузки изображения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Класс Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984221"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="5ebb6-104">Image \_ v0 \_ Load, класс</span><span class="sxs-lookup"><span data-stu-id="5ebb6-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="5ebb6-105">Этот класс является классом типа событий для событий загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="5ebb6-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebb6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ebb6-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="5ebb6-108">Участники</span><span class="sxs-lookup"><span data-stu-id="5ebb6-108">Members</span></span>

<span data-ttu-id="5ebb6-109">Класс **image \_ v0 \_ Load** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5ebb6-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="5ebb6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ebb6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ebb6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ebb6-111">Properties</span></span>

<span data-ttu-id="5ebb6-112">Класс **image \_ v0 \_ Load** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ebb6-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="5ebb6-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebb6-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ebb6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ebb6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="5ebb6-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5ebb6-117">Базовый адрес приложения, в котором загружается образ.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5ebb6-118">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="5ebb6-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebb6-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5ebb6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ebb6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-121">Квалификаторы: Вмидатаид (3), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5ebb6-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5ebb6-122">Имя и расширение файла DLL или исполняемого образа для загрузки.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="5ebb6-123">модулесизе</span><span class="sxs-lookup"><span data-stu-id="5ebb6-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebb6-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ebb6-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ebb6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebb6-126">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="5ebb6-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5ebb6-127">Размер изображения.</span><span class="sxs-lookup"><span data-stu-id="5ebb6-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ebb6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5ebb6-128">Requirements</span></span>



| <span data-ttu-id="5ebb6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5ebb6-129">Requirement</span></span> | <span data-ttu-id="5ebb6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5ebb6-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5ebb6-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ebb6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebb6-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ebb6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5ebb6-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ebb6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebb6-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ebb6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5ebb6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ebb6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebb6-136">**\_V0 изображения**</span><span class="sxs-lookup"><span data-stu-id="5ebb6-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




