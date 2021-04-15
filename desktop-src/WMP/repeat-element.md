---
title: Элемент REPEAT
description: Элемент REPEAT определяет, сколько раз проигрыватель Windows Media повторяет один или несколько элементов ENTRY или ЕНТРИРЕФ.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- ПОВТОРЯЮЩИйся элемент проигрыватель Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648963"
---
# <a name="repeat-element"></a>Элемент REPEAT

Элемент **Repeat** определяет, сколько раз проигрыватель Windows Media повторяет один или несколько элементов **entry** или **ентриреф** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Атрибуты

**COUNT**

Целое число, представляющее количество повторов в проигрывателе Windows Media элементов **entry** и **ентриреф** в области действия этого элемента.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы                |
|-----------------|-------------------------|
| Родительские элементы | **ASX**                 |
| Дочерние элементы  | **запись**, **ентриреф** |



 

## <a name="remarks"></a>Комментарии

Этот элемент определяет число повторов в проигрывателе Windows Media Player или цикл по элементам, которые задаются элементами **entry** и **ентриреф** в области действия этого элемента. Допустим только первый элемент **Repeat** в метафайле; последующие элементы **Repeat** игнорируются.

Если атрибут **Count** не определен, содержимое связанных элементов **entry** и **ентриреф** повторяется бесконечное число раз. Нулевое значение приводит к тому, что проигрыватель Windows Media игнорирует элемент **Repeat** и воспроизводит содержимое один раз.

## <a name="examples"></a>Примеры


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
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

 

 





