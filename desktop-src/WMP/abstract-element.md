---
title: АБСТРАКТный элемент
description: АБСТРАКТный элемент содержит текст, описывающий связанный элемент ASX, BANNER или ENTRY.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- АБСТРАКТный элемент Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698854"
---
# <a name="abstract-element"></a>АБСТРАКТный элемент

**Абстрактный** элемент содержит текст, описывающий связанный элемент **ASX**, **Banner** или **entry** .

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                       |
|-----------|--------------------------------|
| Parent    | **ASX**, **запись**, **баннер** |
| Дочерний     | None                           |



 

## <a name="remarks"></a>Remarks

Если этот элемент встречается в элементе **ASX** , то текст отображается как подсказка при наведении курсора мыши на заголовок показать.

Если этот элемент встречается в элементе **entry** , текст отображается в виде подсказки при наведении указателя мыши на заголовок клипа.

Если этот элемент встречается в элементе **баннера** , текст отображается в виде подсказки для изображения баннера.

Используйте только один **абстрактный** элемент для области. При обработке файла метафайла используется только первый **абстрактный** элемент в области другого элемента. Все последующие **абстрактные** элементы в этой области игнорируются.

## <a name="examples"></a>Примеры


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
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

 

 





