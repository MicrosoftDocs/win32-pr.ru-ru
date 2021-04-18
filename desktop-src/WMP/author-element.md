---
title: AUTHOR, элемент
description: Элемент AUTHOR содержит имя автора метафайла Windows Media или клипа мультимедиа.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Проигрыватель Windows Media, элемент AUTHOR
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694638"
---
# <a name="author-element"></a>AUTHOR, элемент

Элемент **Author** содержит имя автора метафайла Windows Media или клипа мультимедиа.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элемент            |
|-----------------|--------------------|
| Родительские элементы | **ASX**, **запись** |
| Дочерние элементы  | Нет               |



 

## <a name="remarks"></a>Remarks

Этот элемент содержит текстовую строку, представляющую имя автора метафайла Windows Media или клипа мультимедиа. Элемент **Author** можно использовать внутри элемента **ASX** и в элементах **entry** .

Если этот элемент отображается в элементе **ASX** , то текст отображается как **Показать** информацию.

Если этот элемент встречается в элементе **entry** , то текст отображается как Автор клипа.

Каждый родительский элемент **ASX** и **entry** должен содержать не более одного дочернего элемента **Author** . Несколько элементов **Author** после первого будут пропущены и не будут отображаться.

## <a name="examples"></a>Примеры


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Справочник по метафайлу Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





