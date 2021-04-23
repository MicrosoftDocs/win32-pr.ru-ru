---
title: STARTTIME, элемент
description: Элемент STARTTIME определяет индекс времени, с которого проигрыватель Windows Media начнет отрисовку потока.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Проигрыватель Windows Media, элемент STARTTIME
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694804"
---
# <a name="starttime-element"></a><span data-ttu-id="38ced-104">STARTTIME, элемент</span><span class="sxs-lookup"><span data-stu-id="38ced-104">STARTTIME Element</span></span>

<span data-ttu-id="38ced-105">Элемент **StartTime** определяет индекс времени, с которого проигрыватель Windows Media начнет отрисовку потока.</span><span class="sxs-lookup"><span data-stu-id="38ced-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="38ced-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="38ced-106">Attributes</span></span>

<span data-ttu-id="38ced-107">**Значение** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="38ced-107">**VALUE** (required)</span></span>

<span data-ttu-id="38ced-108">Индекс времени (в часах, минутах, секундах и сотых долях секунды), с которого проигрыватель Windows Media начинает воспроизводить поток, определенный в связанном элементе.</span><span class="sxs-lookup"><span data-stu-id="38ced-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="38ced-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="38ced-109">Parent/Child Elements</span></span>



| <span data-ttu-id="38ced-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="38ced-110">Hierarchy</span></span>       | <span data-ttu-id="38ced-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="38ced-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="38ced-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="38ced-112">Parent elements</span></span> | <span data-ttu-id="38ced-113">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="38ced-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="38ced-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="38ced-114">Child elements</span></span>  | <span data-ttu-id="38ced-115">Нет</span><span class="sxs-lookup"><span data-stu-id="38ced-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="38ced-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="38ced-116">Remarks</span></span>

<span data-ttu-id="38ced-117">Этот элемент определяет индекс времени в содержимом, где проигрыватель Windows Media начинает отрисовку потока.</span><span class="sxs-lookup"><span data-stu-id="38ced-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="38ced-118">Этот элемент может использоваться только с сохраненным содержимым по запросу, которое было проиндексировано.</span><span class="sxs-lookup"><span data-stu-id="38ced-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="38ced-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="38ced-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="38ced-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38ced-120">Requirements</span></span>



| <span data-ttu-id="38ced-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38ced-121">Requirement</span></span> | <span data-ttu-id="38ced-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38ced-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="38ced-123">Версия</span><span class="sxs-lookup"><span data-stu-id="38ced-123">Version</span></span><br/> | <span data-ttu-id="38ced-124">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38ced-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38ced-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38ced-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ced-126">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="38ced-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="38ced-127">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="38ced-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





