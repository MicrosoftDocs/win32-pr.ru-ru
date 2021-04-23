---
title: Элемент DURATION
description: Элемент DURATION определяет продолжительность времени, в течение которого проигрыватель Windows Media выводит связанную запись списка воспроизведения.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Элемент DURATION проигрыватель Windows Media
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698981"
---
# <a name="duration-element"></a><span data-ttu-id="1e8ee-104">Элемент DURATION</span><span class="sxs-lookup"><span data-stu-id="1e8ee-104">DURATION Element</span></span>

<span data-ttu-id="1e8ee-105">Элемент **DURATION** определяет продолжительность времени, в течение которого проигрыватель Windows Media выводит связанную запись списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="1e8ee-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1e8ee-106">Attributes</span></span>

<span data-ttu-id="1e8ee-107">**Значение** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="1e8ee-107">**VALUE** (required)</span></span>

<span data-ttu-id="1e8ee-108">Продолжительность времени в часах, минутах, секундах и сотых долях секунды, которая отрисовывается проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="1e8ee-109">Значение по умолчанию — это вся длина записи.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="1e8ee-110">Если запись является графическим файлом, необходимо указать значение длительности.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="1e8ee-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1e8ee-111">Parent/Child Elements</span></span>



| <span data-ttu-id="1e8ee-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="1e8ee-112">Hierarchy</span></span>       | <span data-ttu-id="1e8ee-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="1e8ee-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="1e8ee-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1e8ee-114">Parent elements</span></span> | <span data-ttu-id="1e8ee-115">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="1e8ee-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="1e8ee-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1e8ee-116">Child elements</span></span>  | <span data-ttu-id="1e8ee-117">Нет</span><span class="sxs-lookup"><span data-stu-id="1e8ee-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="1e8ee-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="1e8ee-118">Remarks</span></span>

<span data-ttu-id="1e8ee-119">Этот элемент определяет продолжительность времени, в течение которого поток должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="1e8ee-120">Если **значение атрибута value** превышает длину потока содержимого, поток завершается в его нормальной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="1e8ee-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="1e8ee-121">Этот элемент может находиться либо в элементе **ref** , либо в элементе **entry** .</span><span class="sxs-lookup"><span data-stu-id="1e8ee-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="1e8ee-122">Однако элемент **DURATION** , определенный в элементе **ref** , переопределяет тот, который отображается в родительском элементе **entry** элемента **ref** .</span><span class="sxs-lookup"><span data-stu-id="1e8ee-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="1e8ee-123">Элемент **DURATION** переопределяет элемент **превиевдуратион** .</span><span class="sxs-lookup"><span data-stu-id="1e8ee-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="1e8ee-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e8ee-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="1e8ee-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1e8ee-125">Requirements</span></span>



| <span data-ttu-id="1e8ee-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1e8ee-126">Requirement</span></span> | <span data-ttu-id="1e8ee-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1e8ee-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1e8ee-128">Версия</span><span class="sxs-lookup"><span data-stu-id="1e8ee-128">Version</span></span><br/> | <span data-ttu-id="1e8ee-129">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="1e8ee-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e8ee-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e8ee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e8ee-131">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1e8ee-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="1e8ee-132">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1e8ee-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





