---
title: Элемент Argument
description: Элемент Argument содержит одну часть строки условия.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- Проигрыватель Windows Media, элемент Argument
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695137"
---
# <a name="argument-element"></a><span data-ttu-id="a4886-104">Элемент Argument</span><span class="sxs-lookup"><span data-stu-id="a4886-104">argument Element</span></span>

<span data-ttu-id="a4886-105">Элемент **Argument** содержит одну часть строки условия.</span><span class="sxs-lookup"><span data-stu-id="a4886-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="a4886-106">Строка условия обычно содержит условие и часть значения.</span><span class="sxs-lookup"><span data-stu-id="a4886-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="a4886-107">Например, в строке Условия «исполнитель равно Joe» условием является «EQUAL», а значение «Joe».</span><span class="sxs-lookup"><span data-stu-id="a4886-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="a4886-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a4886-108">Attributes</span></span>

<span data-ttu-id="a4886-109">**имя** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="a4886-109">**name** (required)</span></span>

<span data-ttu-id="a4886-110">Имя одной части строки условия.</span><span class="sxs-lookup"><span data-stu-id="a4886-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="a4886-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a4886-111">Parent/Child Elements</span></span>



| <span data-ttu-id="a4886-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="a4886-112">Hierarchy</span></span> | <span data-ttu-id="a4886-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="a4886-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="a4886-114">Parent</span><span class="sxs-lookup"><span data-stu-id="a4886-114">Parent</span></span>    | [<span data-ttu-id="a4886-115">экстент</span><span class="sxs-lookup"><span data-stu-id="a4886-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="a4886-116">Дочерний</span><span class="sxs-lookup"><span data-stu-id="a4886-116">Child</span></span>     | <span data-ttu-id="a4886-117">None</span><span class="sxs-lookup"><span data-stu-id="a4886-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="a4886-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="a4886-118">Remarks</span></span>

<span data-ttu-id="a4886-119">Если атрибут **Name** элемента **фрагмента** является характеристикой элемента мультимедиа, например исполнителем или жанром, элемент **Fragment** должен содержать два элемента **Argument** : один, указывающий условие, а другой — значение.</span><span class="sxs-lookup"><span data-stu-id="a4886-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="a4886-120">В следующей таблице показаны два возможных значения для атрибута **Name** и способы использования элементов **Argument** для указания условий и значений.</span><span class="sxs-lookup"><span data-stu-id="a4886-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4886-121">Значение атрибута</span><span class="sxs-lookup"><span data-stu-id="a4886-121">Attribute value</span></span></th>
<th><span data-ttu-id="a4886-122">Описание</span><span class="sxs-lookup"><span data-stu-id="a4886-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4886-123">Условие</span><span class="sxs-lookup"><span data-stu-id="a4886-123">Condition</span></span></td>
<td><span data-ttu-id="a4886-124">Содержимое элемента <strong>Argument</strong> является частью условия в строке условия.</span><span class="sxs-lookup"><span data-stu-id="a4886-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="a4886-125">Например, в строке Условия исполнитель имеет &quot; &quot; значение Joe, а условие &quot; равно &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4886-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="a4886-126">Условие в строке условия должно быть одним из следующих: равно, не равно, Contains, не содержит, меньше, больше, является, не более чем, более чем, более поздним, чем, более ранним, чем выше, чем выше, а более поздней, чем выше, чем выше, ни по меньшей мере.</span><span class="sxs-lookup"><span data-stu-id="a4886-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4886-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a4886-127">Value</span></span></td>
<td><span data-ttu-id="a4886-128">Содержимым элемента <strong>Argument</strong> является часть значения строки условия.</span><span class="sxs-lookup"><span data-stu-id="a4886-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="a4886-129">Например, в строке условия &quot; исполнитель, равный Джо &quot; , значение является &quot; Джо &quot; . Например</span><span class="sxs-lookup"><span data-stu-id="a4886-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4886-130">Если атрибут **Name** элемента **фрагмента** имеет значение "ограничить общий размер до" или "ограничить общую длительность до", элемент **фрагмента** должен содержать два элемента **Argument** : один, указывающий формат и один, указывающий число.</span><span class="sxs-lookup"><span data-stu-id="a4886-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="a4886-131">В следующей таблице показаны два возможных значения для атрибута **Name** и способы использования элементов **Argument** для ограничения размера или продолжительности списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a4886-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4886-132">Значение атрибута</span><span class="sxs-lookup"><span data-stu-id="a4886-132">Attribute value</span></span></th>
<th><span data-ttu-id="a4886-133">Описание</span><span class="sxs-lookup"><span data-stu-id="a4886-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4886-134">Формат</span><span class="sxs-lookup"><span data-stu-id="a4886-134">Format</span></span></td>
<td><span data-ttu-id="a4886-135">Если атрибут <strong>Name</strong> элемента <strong>Fragment</strong> имеет &quot; ограничение общего размера до &quot; , содержимое элемента <strong>Argument</strong> должно быть одним из следующих: килобайт, мегабайт или гигабайт. Если атрибут <strong>Name</strong> элемента <strong>Fragment</strong> имеет &quot; ограничение общей длительности до &quot; , содержимое элемента <strong>Argument</strong> должно быть одним из следующих: секунды, минуты, часы или дни.</span><span class="sxs-lookup"><span data-stu-id="a4886-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4886-136">Число</span><span class="sxs-lookup"><span data-stu-id="a4886-136">Number</span></span></td>
<td><span data-ttu-id="a4886-137">Содержимое элемента <strong>Argument</strong> является числом, ограничивающим размер или длительность списка воспроизведения. Примеров</span><span class="sxs-lookup"><span data-stu-id="a4886-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4886-138">Если атрибут **Name** элемента **Fragment** имеет ограничение количества элементов, элемент **Fragment** должен содержать один элемент **Argument** , указывающий количество элементов.</span><span class="sxs-lookup"><span data-stu-id="a4886-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="a4886-139">В следующей таблице показано, как использовать числовое значение атрибута **Name** .</span><span class="sxs-lookup"><span data-stu-id="a4886-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4886-140">Значение атрибута</span><span class="sxs-lookup"><span data-stu-id="a4886-140">Attribute value</span></span></th>
<th><span data-ttu-id="a4886-141">Описание</span><span class="sxs-lookup"><span data-stu-id="a4886-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4886-142">Число</span><span class="sxs-lookup"><span data-stu-id="a4886-142">Number</span></span></td>
<td><span data-ttu-id="a4886-143">Содержимое элемента <strong>Argument</strong> является числом, ограничивающим количество элементов в списке воспроизведения. Например</span><span class="sxs-lookup"><span data-stu-id="a4886-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a4886-144">Требования</span><span class="sxs-lookup"><span data-stu-id="a4886-144">Requirements</span></span>



| <span data-ttu-id="a4886-145">Требование</span><span class="sxs-lookup"><span data-stu-id="a4886-145">Requirement</span></span> | <span data-ttu-id="a4886-146">Значение</span><span class="sxs-lookup"><span data-stu-id="a4886-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="a4886-147">Версия</span><span class="sxs-lookup"><span data-stu-id="a4886-147">Version</span></span><br/> | <span data-ttu-id="a4886-148">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a4886-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4886-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4886-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4886-150">**Элемент Fragment**</span><span class="sxs-lookup"><span data-stu-id="a4886-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="a4886-151">**Справочник по элементам списка воспроизведения Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a4886-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





