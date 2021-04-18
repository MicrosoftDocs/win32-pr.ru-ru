---
title: Элемент title (WPL)
description: Элемент Title указывает название списка воспроизведения.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Элемент title (WPL) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704503"
---
# <a name="title-element-wpl"></a>Элемент title (WPL)

Элемент **Title** указывает название списка воспроизведения.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Атрибуты

Этот элемент не содержит атрибуты.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия | Элементы                 |
|-----------|--------------------------|
| Parent    | [Глава](head-element.md) |
| Дочерний     | None                     |



 

## <a name="remarks"></a>Remarks

При выборе заголовка для списка воспроизведения Windows Media (WPL) следует учесть, что содержимое списка воспроизведения может быть динамическим. Хорошим подходом является основа заголовка логики в элементах **Argument** , так как именно это определяет содержимое списка воспроизведения. В качестве примера можно привести «мой любимый рок — песни из 1966» или «Dance песни, которые я не воспроизводил».

## <a name="examples"></a>Примеры


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент Argument**](argument-element.md)
</dt> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Справочник по элементам списка воспроизведения Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





