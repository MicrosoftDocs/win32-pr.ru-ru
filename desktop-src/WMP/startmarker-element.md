---
title: СТАРТМАРКЕР, элемент
description: Элемент СТАРТМАРКЕР указывает маркер, с помощью которого проигрыватель Windows Media начнет отрисовку потока.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Проигрыватель Windows Media, элемент СТАРТМАРКЕР
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698978"
---
# <a name="startmarker-element"></a><span data-ttu-id="ec369-104">СТАРТМАРКЕР, элемент</span><span class="sxs-lookup"><span data-stu-id="ec369-104">STARTMARKER Element</span></span>

<span data-ttu-id="ec369-105">Элемент **стартмаркер** указывает маркер, с помощью которого проигрыватель Windows Media начнет отрисовку потока.</span><span class="sxs-lookup"><span data-stu-id="ec369-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="ec369-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec369-106">Attributes</span></span>

<span data-ttu-id="ec369-107">**Нумерация**</span><span class="sxs-lookup"><span data-stu-id="ec369-107">**NUMBER**</span></span>

<span data-ttu-id="ec369-108">Номер числового маркера в индексе.</span><span class="sxs-lookup"><span data-stu-id="ec369-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="ec369-109">Значение по умолчанию — это начало содержимого по запросу или текущего расположения в потоке в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ec369-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="ec369-110">**ИМЯ**</span><span class="sxs-lookup"><span data-stu-id="ec369-110">**NAME**</span></span>

<span data-ttu-id="ec369-111">Имя именованного маркера в индексе.</span><span class="sxs-lookup"><span data-stu-id="ec369-111">The name of a named marker in the index.</span></span> <span data-ttu-id="ec369-112">Значение по умолчанию — это начало содержимого по запросу или текущего расположения в потоке в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="ec369-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ec369-113">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec369-113">Parent/Child Elements</span></span>



| <span data-ttu-id="ec369-114">Иерархия</span><span class="sxs-lookup"><span data-stu-id="ec369-114">Hierarchy</span></span>       | <span data-ttu-id="ec369-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="ec369-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="ec369-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ec369-116">Parent elements</span></span> | <span data-ttu-id="ec369-117">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="ec369-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="ec369-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec369-118">Child elements</span></span>  | <span data-ttu-id="ec369-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ec369-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="ec369-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="ec369-120">Remarks</span></span>

<span data-ttu-id="ec369-121">Этот элемент задает маркер, с помощью которого проигрыватель Windows Media начинает отрисовку потока, определенного в родительской **записи** или элементе **ref** .</span><span class="sxs-lookup"><span data-stu-id="ec369-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="ec369-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ec369-122">**Note**</span></span>

<span data-ttu-id="ec369-123">Используйте этот элемент с атрибутом **Number** или **Name** , но не обоими.</span><span class="sxs-lookup"><span data-stu-id="ec369-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="ec369-124">Элемент **стартмаркер** , определенный внутри **ссылочного** элемента, имеет приоритет над элементом **стартмаркер** , определенным в родительском элементе **entry** элемента **ref** .</span><span class="sxs-lookup"><span data-stu-id="ec369-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="ec369-125">Элемент **стартмаркер** также имеет приоритет над элементом **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="ec369-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="ec369-126">Если маркер, заданный элементом **стартмаркер** , происходит позже в потоке, отличном от маркера, определенного элементом **ендмаркер** , содержимое не будет воспроизводиться, но ошибки не создаются.</span><span class="sxs-lookup"><span data-stu-id="ec369-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="ec369-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec369-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="ec369-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ec369-128">Requirements</span></span>



| <span data-ttu-id="ec369-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ec369-129">Requirement</span></span> | <span data-ttu-id="ec369-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ec369-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ec369-131">Версия</span><span class="sxs-lookup"><span data-stu-id="ec369-131">Version</span></span><br/> | <span data-ttu-id="ec369-132">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ec369-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec369-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec369-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec369-134">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ec369-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ec369-135">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ec369-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





