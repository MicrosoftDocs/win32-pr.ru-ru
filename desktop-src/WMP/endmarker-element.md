---
title: ЕНДМАРКЕР, элемент
description: Элемент ЕНДМАРКЕР указывает маркер, по которому проигрыватель Windows Media останавливает отрисовку потока.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Проигрыватель Windows Media, элемент ЕНДМАРКЕР
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699186"
---
# <a name="endmarker-element"></a><span data-ttu-id="ff13f-104">ЕНДМАРКЕР, элемент</span><span class="sxs-lookup"><span data-stu-id="ff13f-104">ENDMARKER Element</span></span>

<span data-ttu-id="ff13f-105">Элемент **ендмаркер** указывает маркер, по которому проигрыватель Windows Media останавливает отрисовку потока.</span><span class="sxs-lookup"><span data-stu-id="ff13f-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="ff13f-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ff13f-106">Attributes</span></span>

<span data-ttu-id="ff13f-107">**Нумерация**</span><span class="sxs-lookup"><span data-stu-id="ff13f-107">**NUMBER**</span></span>

<span data-ttu-id="ff13f-108">Номер числового маркера в индексе.</span><span class="sxs-lookup"><span data-stu-id="ff13f-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="ff13f-109">Значение по умолчанию — конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="ff13f-109">The default value is the end of the content.</span></span>

<span data-ttu-id="ff13f-110">**ИМЯ**</span><span class="sxs-lookup"><span data-stu-id="ff13f-110">**NAME**</span></span>

<span data-ttu-id="ff13f-111">Имя именованного маркера в индексе.</span><span class="sxs-lookup"><span data-stu-id="ff13f-111">The name of a named marker in the index.</span></span> <span data-ttu-id="ff13f-112">Значение по умолчанию — конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="ff13f-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ff13f-113">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ff13f-113">Parent/Child Elements</span></span>



| <span data-ttu-id="ff13f-114">Иерархия</span><span class="sxs-lookup"><span data-stu-id="ff13f-114">Hierarchy</span></span>       | <span data-ttu-id="ff13f-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="ff13f-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="ff13f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ff13f-116">Parent elements</span></span> | <span data-ttu-id="ff13f-117">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="ff13f-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="ff13f-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ff13f-118">Child elements</span></span>  | <span data-ttu-id="ff13f-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ff13f-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="ff13f-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="ff13f-120">Remarks</span></span>

<span data-ttu-id="ff13f-121">Этот элемент указывает маркер, на котором проигрыватель Windows Media останавливает отрисовку потока, определенного в родительской **записи** или элементе **ref** .</span><span class="sxs-lookup"><span data-stu-id="ff13f-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="ff13f-122">Примечание</span><span class="sxs-lookup"><span data-stu-id="ff13f-122">Note</span></span>

<span data-ttu-id="ff13f-123">Используйте элемент **ендмаркер** с атрибутом **Number** или **Name** , но не обоими.</span><span class="sxs-lookup"><span data-stu-id="ff13f-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="ff13f-124">В режиме предварительного просмотра достижение завершающего маркера останавливает предварительную версию, даже если не прошло время, заданное элементом **превиевдуратион** .</span><span class="sxs-lookup"><span data-stu-id="ff13f-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="ff13f-125">Элемент **ендмаркер** также имеет приоритет над элементом **DURATION** .</span><span class="sxs-lookup"><span data-stu-id="ff13f-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="ff13f-126">Элемент **ендмаркер** , определенный внутри **ссылочного** элемента, имеет приоритет над **ендмаркер** , определенным в родительском элементе **entry** элемента **ref** .</span><span class="sxs-lookup"><span data-stu-id="ff13f-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="ff13f-127">Если маркер, заданный элементом **ендмаркер** , находится в потоке раньше, чем маркер, заданный элементом **стартмаркер** , содержимое не будет воспроизводиться, но ошибки не создаются.</span><span class="sxs-lookup"><span data-stu-id="ff13f-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="ff13f-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff13f-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="ff13f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ff13f-129">Requirements</span></span>



| <span data-ttu-id="ff13f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ff13f-130">Requirement</span></span> | <span data-ttu-id="ff13f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ff13f-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ff13f-132">Версия</span><span class="sxs-lookup"><span data-stu-id="ff13f-132">Version</span></span><br/> | <span data-ttu-id="ff13f-133">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ff13f-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff13f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff13f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff13f-135">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ff13f-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ff13f-136">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ff13f-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





