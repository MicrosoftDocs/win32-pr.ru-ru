---
title: STARTTIME, элемент
description: элемент STARTTIME определяет индекс времени, на основе которого проигрыватель Windows Media начнет отрисовку потока.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- элемент STARTTIME проигрыватель Windows Media
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9138b05b949098c59996c69143059de5cb5b25cafcd8da7d922de120d586b356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568796"
---
# <a name="starttime-element"></a>STARTTIME, элемент

элемент **STARTTIME** определяет индекс времени, на основе которого проигрыватель Windows Media начнет отрисовку потока.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Атрибуты

**Значение** (обязательно)

индекс времени (в часах, минутах, секундах и сотых долях секунды), с которого проигрыватель Windows Media начинает воспроизводить поток, определенный в связанном элементе.

## <a name="parentchild-elements"></a>Родительские и дочерние элементы



| Иерархия       | Элементы           |
|-----------------|--------------------|
| Родительские элементы | **entry**, **ref** |
| Дочерние элементы  | Нет               |



 

## <a name="remarks"></a>Remarks

этот элемент определяет индекс времени в содержимом, где проигрыватель Windows Media — начать отрисовку потока. Этот элемент может использоваться только с сохраненным содержимым по запросу, которое было проиндексировано.

## <a name="examples"></a>Примеры


```XML
<STARTTIME VALUE="1:30.0" />
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

 

 





