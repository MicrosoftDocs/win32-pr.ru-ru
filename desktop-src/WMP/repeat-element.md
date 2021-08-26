---
title: Элемент REPEAT
description: элемент repeat определяет количество раз, проигрыватель Windows Media повторяет один или несколько элементов ENTRY или ентриреф.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- повторяющийся элемент проигрыватель Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 330eda0757acb29b48ed10636d8f479b6ebb1395d088020876c717a78f41ae6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002544"
---
# <a name="repeat-element"></a>Элемент REPEAT

элемент **repeat** определяет количество раз, проигрыватель Windows Media повторяет один или несколько элементов **ENTRY** или **ентриреф** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Атрибуты

**COUNT**

целое число, представляющее количество раз, когда проигрыватель Windows Media повторяет элементы **записи** и **ентриреф** в области действия этого элемента.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы                |
|-----------------|-------------------------|
| Родительские элементы | **ASX**                 |
| Дочерние элементы  | **запись**, **ентриреф** |



 

## <a name="remarks"></a>Remarks

этот элемент определяет количество повторов проигрыватель Windows Media повторений или циклов по, клипов, определенных элементами **ENTRY** и **ентриреф** в области действия этого элемента. Допустим только первый элемент **Repeat** в метафайле; последующие элементы **Repeat** игнорируются.

Если атрибут **Count** не определен, содержимое связанных элементов **entry** и **ентриреф** повторяется бесконечное число раз. нулевое значение приводит к тому, что проигрыватель Windows Media пропускать элемент **REPEAT** и воспроизводить содержимое один раз.

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
| Версия<br/> | проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Windows Справочник по элементам метафайлов мультимедиа**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Ссылка на метафайл мультимедиа**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





