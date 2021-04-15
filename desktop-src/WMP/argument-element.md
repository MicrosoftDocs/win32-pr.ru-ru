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
# <a name="argument-element"></a>Элемент Argument

Элемент **Argument** содержит одну часть строки условия. Строка условия обычно содержит условие и часть значения. Например, в строке Условия «исполнитель равно Joe» условием является «EQUAL», а значение «Joe».

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Атрибуты

**имя** (обязательно)

Имя одной части строки условия.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                         |
|-----------|----------------------------------|
| Parent    | [экстент](fragment-element.md) |
| Дочерний     | None                             |



 

## <a name="remarks"></a>Remarks

Если атрибут **Name** элемента **фрагмента** является характеристикой элемента мультимедиа, например исполнителем или жанром, элемент **Fragment** должен содержать два элемента **Argument** : один, указывающий условие, а другой — значение. В следующей таблице показаны два возможных значения для атрибута **Name** и способы использования элементов **Argument** для указания условий и значений.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение атрибута</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Условие</td>
<td>Содержимое элемента <strong>Argument</strong> является частью условия в строке условия. Например, в строке Условия исполнитель имеет &quot; &quot; значение Joe, а условие &quot; равно &quot; . Условие в строке условия должно быть одним из следующих: равно, не равно, Contains, не содержит, меньше, больше, является, не более чем, более чем, более поздним, чем, более ранним, чем выше, чем выше, а более поздней, чем выше, чем выше, ни по меньшей мере.</td>
</tr>
<tr class="even">
<td>Значение</td>
<td>Содержимым элемента <strong>Argument</strong> является часть значения строки условия. Например, в строке условия &quot; исполнитель, равный Джо &quot; , значение является &quot; Джо &quot; . Например<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Если атрибут **Name** элемента **фрагмента** имеет значение "ограничить общий размер до" или "ограничить общую длительность до", элемент **фрагмента** должен содержать два элемента **Argument** : один, указывающий формат и один, указывающий число. В следующей таблице показаны два возможных значения для атрибута **Name** и способы использования элементов **Argument** для ограничения размера или продолжительности списка воспроизведения.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение атрибута</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Формат</td>
<td>Если атрибут <strong>Name</strong> элемента <strong>Fragment</strong> имеет &quot; ограничение общего размера до &quot; , содержимое элемента <strong>Argument</strong> должно быть одним из следующих: килобайт, мегабайт или гигабайт. Если атрибут <strong>Name</strong> элемента <strong>Fragment</strong> имеет &quot; ограничение общей длительности до &quot; , содержимое элемента <strong>Argument</strong> должно быть одним из следующих: секунды, минуты, часы или дни.<br/></td>
</tr>
<tr class="even">
<td>Число</td>
<td>Содержимое элемента <strong>Argument</strong> является числом, ограничивающим размер или длительность списка воспроизведения. Примеров<br/>
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



 

Если атрибут **Name** элемента **Fragment** имеет ограничение количества элементов, элемент **Fragment** должен содержать один элемент **Argument** , указывающий количество элементов. В следующей таблице показано, как использовать числовое значение атрибута **Name** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение атрибута</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Число</td>
<td>Содержимое элемента <strong>Argument</strong> является числом, ограничивающим количество элементов в списке воспроизведения. Например<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Fragment**](fragment-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





