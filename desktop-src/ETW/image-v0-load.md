---
description: Image_V0_Load класс. Этот класс является классом типа события для событий загрузки изображения. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106522"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="4c553-104">Image \_ v0 \_ Load, класс</span><span class="sxs-lookup"><span data-stu-id="4c553-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="4c553-105">Этот класс является классом типа событий для событий загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="4c553-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="4c553-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="4c553-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c553-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c553-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="4c553-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4c553-108">Members</span></span>

<span data-ttu-id="4c553-109">Класс **image \_ v0 \_ Load** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c553-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="4c553-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c553-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c553-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="4c553-111">Properties</span></span>

<span data-ttu-id="4c553-112">Класс **image \_ v0 \_ Load** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c553-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c553-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="4c553-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c553-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c553-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c553-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c553-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c553-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="4c553-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4c553-117">Базовый адрес приложения, в котором загружается образ.</span><span class="sxs-lookup"><span data-stu-id="4c553-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="4c553-118">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="4c553-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c553-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c553-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c553-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c553-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c553-121">Квалификаторы: Вмидатаид (3), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4c553-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4c553-122">Имя и расширение файла DLL или исполняемого образа для загрузки.</span><span class="sxs-lookup"><span data-stu-id="4c553-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="4c553-123">модулесизе</span><span class="sxs-lookup"><span data-stu-id="4c553-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c553-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c553-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c553-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c553-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c553-126">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="4c553-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4c553-127">Размер изображения.</span><span class="sxs-lookup"><span data-stu-id="4c553-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c553-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4c553-128">Requirements</span></span>



| <span data-ttu-id="4c553-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4c553-129">Requirement</span></span> | <span data-ttu-id="4c553-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4c553-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c553-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c553-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c553-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c553-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4c553-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c553-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c553-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4c553-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4c553-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4c553-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c553-136">**\_V0 изображения**</span><span class="sxs-lookup"><span data-stu-id="4c553-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




