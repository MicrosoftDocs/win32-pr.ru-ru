---
title: attribute_onchange
description: Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий. Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и \ 0034; OnChange \ 0034;, например \ 0034; значение \_ onChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange проигрыватель Windows Media
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573764"
---
# <a name="attribute_onchange"></a>атрибут \_ onChange

Когда атрибут обложки изменяет значение, возникает событие, которое может быть обработано обработчиком событий. Имя обработчика событий — это имя атрибута, за которым следует символ подчеркивания и "OnChange", например "значение \_ onChange".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Примеры


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 70 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Обработчики событий окружения**](ambient-event-handlers.md)
</dt> </dl>

 

 





