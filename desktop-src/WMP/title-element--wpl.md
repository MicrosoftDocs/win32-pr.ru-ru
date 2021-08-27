---
title: Элемент title (WPL)
description: Элемент Title указывает название списка воспроизведения.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- элемент title (WPL) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1de2679d5f78b48ceef569491ef21998fc13faf7126e61f76ad31959bdc2ac6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122784"
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

при выборе заголовка для списка воспроизведения Windows Media (WPL) следует учесть, что содержимое списка воспроизведения может быть динамическим. Хорошим подходом является основа заголовка логики в элементах **Argument** , так как именно это определяет содержимое списка воспроизведения. В качестве примера можно привести «мой любимый рок — песни из 1966» или «Dance песни, которые я не воспроизводил».

## <a name="examples"></a>Примеры


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент Argument**](argument-element.md)
</dt> <dt>

[**Элемент head**](head-element.md)
</dt> <dt>

[**Windows Справочник по элементам списка воспроизведения мультимедиа**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





