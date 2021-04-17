---
title: STARTTIME, элемент
description: Элемент STARTTIME определяет индекс времени, с которого проигрыватель Windows Media начнет отрисовку потока.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Проигрыватель Windows Media, элемент STARTTIME
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694804"
---
# <a name="starttime-element"></a>STARTTIME, элемент

Элемент **StartTime** определяет индекс времени, с которого проигрыватель Windows Media начнет отрисовку потока.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Атрибуты

**Значение** (обязательно)

Индекс времени (в часах, минутах, секундах и сотых долях секунды), с которого проигрыватель Windows Media начинает воспроизводить поток, определенный в связанном элементе.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы           |
|-----------------|--------------------|
| Родительские элементы | **entry**, **ref** |
| Дочерние элементы  | Нет               |



 

## <a name="remarks"></a>Remarks

Этот элемент определяет индекс времени в содержимом, где проигрыватель Windows Media начинает отрисовку потока. Этот элемент может использоваться только с сохраненным содержимым по запросу, которое было проиндексировано.

## <a name="examples"></a>Примеры


```XML
<STARTTIME VALUE="1:30.0" />
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

 

 





